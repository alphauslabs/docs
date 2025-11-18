# Setting-up API Access in Octo

This CloudFormation template provisions the IAM roles required for **Alphaus Octo** to securely access resources in AWS accounts for:

- Cost optimization recommendations
- Automated change execution
- Cost and usage reporting
- Trusted Advisor and Compute Optimizer analysis
- SSM Automation integration
- End-to-end cost optimization workflows

This template is intended for deployment in **AWS accounts**.

---

# 1. Parameters

## 1.1 `Principal`
- **Type:** String  
- **Description:** Alphaus AWS account ID allowed to assume roles.
- **Pattern:** Only digits (`^[0-9]*$`)

## 1.2 `ExternalId`
- **Type:** String  
- **Description:** External identifier used during `sts:AssumeRole` for cross-account security.

Both parameters protect against the *confused deputy problem*.

---

# 2. IAM Roles Created

The template provisions **five IAM roles**, each serving a dedicated purpose.

---

# 2.1 OctoRecommendationSearcherRole

### Purpose
Allows Alphaus to **collect read-only resource information** needed for cost and optimization recommendations.

### Capabilities
- Compute Optimizer data
- Trusted Advisor checks
- CloudWatch metrics
- Describe/List for EC2, EBS, RDS, Lambda, Redshift, DynamoDB, etc.
- CloudTrail lookup
- S3 bucket metadata
- Route53 hosted zones
- Pricing data
- Organizations metadata
- Backup data
- Resource Groups information

### Security
- **Strictly read-only**
- No modify or delete actions

---

# 2.2 OctoChangeExecutorRole

### Purpose
Executes **approved SSM Change Manager workflows** that perform modifications on AWS resources.

### Assumed By
- `ssm.amazonaws.com`
- The AWS account’s root principal

### Capabilities
- AWS managed policy: **AdministratorAccess**
- Executes SSM Automation runbooks triggered by the customer

### Security
- **Alphaus cannot assume this role directly.**
- Only the customer’s SSM workflows can use it.

---

# 2.3 OctoSSMUpdaterRole

### Purpose
Allows Alphaus to **manage SSM Automation documents** and initiate change requests.

### Assumed By
- Alphaus account via `Principal` + `ExternalId`

### Capabilities
- Manage (Create/Update/Delete) SSM documents
- Trigger Automation executions
- PassRole to OctoChangeExecutorRole
- Add tags, update service settings
- Stop, resume, and query SSM automations

### Security
- Cannot modify AWS resources directly
- All changes still route through SSM + OctoChangeExecutorRole

---

# 2.4 OctoChangeTemplateApproverRole

### Purpose
Allows **customer-side approval** of Change Manager templates.

### Assumed By
- The customer AWS account only

### Capabilities
- View SSM documents
- Approve, revise, or submit change templates
- Provide automation execution signals

### Security
- Alphaus has **no access** to this role.

---

# 2.5 AlphausAcctAccessRole

### Purpose
Provides Alphaus with the ability to read account-level cost and usage metadata.

### Capabilities
- Cost Explorer (`ce:*`)
- CUR (`cur:Describe*`)
- Savings Plan and Reserved Instance recommendations
- CloudWatch metrics
- Describe access to RDS, Redshift, ElastiCache for RI inventory
- AWS Organization metadata
- IAM ListRoles
- CloudFormation read-only access

### Additional IAM Permissions
- Can update inline policies for:
  - `AlphausAcctAccessRole`
  - `OctoRecommendationSearcherRole`
- Can update the stack **that created this role** (used for template upgrades)
- Can create required service-linked roles for:
  - Trusted Advisor
  - Cost Optimization Hub

---

# 3. Security Architecture

### Cross-Account Access Protection
- Uses `Principal` (Alphaus AWS account ID)
- Uses `ExternalId`
- Roles have scoped, minimal permissions
- No unnecessary write capabilities

### Role Separation of Duties

| Role | Access Level | Purpose |
|------|--------------|---------|
| OctoRecommendationSearcherRole | Read-only | Collect optimization data |
| OctoSSMUpdaterRole | SSM write | Manage automation documents |
| OctoChangeExecutorRole | Admin | Execute approved changes |
| OctoChangeTemplateApproverRole | Approval | Approve workflows |
| AlphausAcctAccessRole | Read-only | Billing, CUR, CE, and metadata access |

This prevents privilege escalation and ensures customer control.

---

# 4. Deployment Notes

### Recommended Deployment Method
- **AWS CloudFormation StackSets**
  - Deploy to all **member accounts**
  - Exclude management account if desired
  - Exclude accounts without CUR enabled

### Update Safety
Roles are allowed to update the CloudFormation stack that created them, ensuring:
- Non-breaking template upgrades
- Automated policy updates

---

# 5. Summary

This CloudFormation template enables:

| Capability | Role Handling It |
|------------|------------------|
| Resource data collection | OctoRecommendationSearcherRole |
| Executing change workflows | OctoChangeExecutorRole |
| Managing SSM automation | OctoSSMUpdaterRole |
| Customer workflow approvals | OctoChangeTemplateApproverRole |
| Cost, billing, CUR, CE access | AlphausAcctAccessRole |
| Secure cross-account authentication | Principal + ExternalId |

The template provides all permissions necessary for **Alphaus Octo** to perform cost optimization recommendations and automation while maintaining **strong customer-side control and security boundaries**.