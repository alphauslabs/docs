# Setting-up API Access in Octo
This template provisions a cross-account IAM role that grants Octo secure access to AWS account cost-related information. The role is assumed by Alphaus using an external ID for security, allowing automated access to billing, cost optimization, and related services.

## Template Information

- Format Version: 2010-09-09
- Description: Template to setup cross account IAM role for Alphaus access to your account's cost-related information.

## Parameters
The template requires two parameters during deployment:

| Parameter    | Type     | Description                                              | Notes                                       |
| ------------ | -------- | -------------------------------------------------------- | ------------------------------------------- |
| Principal    | String   | The Alphaus AWS account ID that will assume this role.   | Must be numeric (^[0-9]*$). Do not change.  |
| ExternalId   | String   | The external ID Alphaus uses when assuming this role.    | Do not change.                              |

## Resources

IAM Role: AlphausAcctAccessRole

- Type: AWS::IAM::Role
- Role Name: AlphausAcctAccessRole
- Max Session Duration: 12 hours (43,200 seconds)
- Trust Policy (AssumeRole):
    - Allows the Principal AWS account (Alphaus) to assume the role.
    - Requires ExternalId match for enhanced security.

## IAM Policies

The role attaches two managed inline policies:

Policy 1: root

Grants Alphaus read/list access to cost-related and optimization APIs, as well as limited role and stack management.

Key Permissions:

- Cost & Billing Data
    - cur:Describe* (Cost & Usage Reports)
    - ce:Get*, ce:List* (Cost Explorer)
    - billingconductor:List* (Billing Conductor)
    - savingsplans:Describe*

- AWS Service Usage & Recommendations
    - organizations:List*
    - rds, elasticache, es, redshift (reserved instance details)
    - compute-optimizer:Get*, compute-optimizer:Export*

- CloudFormation
    - cloudformation:Get*, cloudformation:List*, cloudformation:BatchDescribe*
    - Limited stack update on the deployed stack only

- IAM
    - iam:GetRole*, iam:PutRolePolicy (restricted to AlphausAcctAccessRole)
    - iam:CreateServiceLinkedRole (for cost optimization services like Trusted Advisor)

Policy 2: octo-optimization-recommendation

Provides broader access for optimization recommendations, automation, and remediation actions.

Key Permissions:

- Cost Optimization & Trusted Advisor
    - trustedadvisor:Get*, trustedadvisor:List*
    - support:Describe*
    - cost-optimization-hub:*

- Resource Management (with potential cost savings impact)
    - EC2: DeleteVolume, ModifyVolume, CreateSnapshot, CreateImage, RebootInstances, etc.
    - RDS: DeleteDBInstance, CreateDBSnapshot
    - Redshift, Elasticsearch: DeleteCluster, DeleteDomain
    - S3: PutLifecycleConfiguration, GetLifecycleConfiguration
    - ECS: RegisterTaskDefinition, UpdateService
    - Lambda: DeleteFunction, UpdateFunctionConfiguration
    - ELB: DeleteLoadBalancer

- IAM & Instance Profile Management
    - iam:CreateRole, iam:AttachRolePolicy, iam:CreateInstanceProfile, iam:PassRole, etc.

- Automation & Systems Manager
    - ssm:*, ssmmessages:*, ec2messages:*
    - ssm:SendCommand

- Other AWS Services
    - secretsmanager:*
    - cloudtrail:LookupEvents
    - pricing:Get*, pricing:ListPriceLists, pricing:DescribeServices
    - quicksight:List*
    - kendra:List*, kendra:Describe*
    - bedrock:List*, bedrock:Get*

## Security Considerations

- High-Privilege Actions: The role has delete and modification permissions (EC2, RDS, Redshift, etc.). This is necessary for cost optimization automation but with additional setup on [Change Template](../recommendations/executerecommendation.md).

- ExternalId Requirement: Protect permissions to access certain resources or perform certain actions.

- Scoped IAM Role Policy: Some IAM actions are restricted to the AlphausAcctAccessRole itself.