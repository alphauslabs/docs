# Setting-up CUR and S3 bucket in Octo
This template sets up an AWS Cost and Usage Report (CUR) export to S3 and provisions an IAM role that allows Alphaus to securely access the exported CUR files and related billing data.

## Template Information

- Format Version: 2010-09-09
- Description: Setup CUR export, cross account IAM role for Alphaus access to your account's cost-related information.

## Parameters
The template requires two parameters during deployment:

| Parameter          | Type     | Description                                                     | Default            | Notes                                      |
| ------------------ | -------- | --------------------------------------------------------------- | ------------------ | ------------------------------------------ |
| CurS3BucketOption  | String   | Choose whether to create a new S3 bucket or use an existing one.| CREATE_NEW         | Allowed values: CREATE_NEW, USE_EXISTING.  |
| CurS3BucketName    | String   | Name of the S3 bucket to store CUR.                             | alphaus-cur-export | Must exist if USE_EXISTING is chosen.      |
| CurS3BucketRegion  | String   | Region for the S3 bucket.                                       | us-east-1          | Default used if creating new bucket.       |
| CurS3Prefix        | String   | Folder prefix for CUR reports.                                  | pre                | No spaces allowed.                         |
| CurReportName      | String   | The CUR report name.                                            | curreport          | Must be unique, case-sensitive, no spaces. |
| Principal          | String   | The Alphaus AWS account ID that will access CUR data.           | —                  | Must be numeric.                           |

## Conditions

- CreateBucket – Evaluates to true if CurS3BucketOption = CREATE_NEW, triggering bucket creation.

## Resources

S3Bucket (optional)

- Type: AWS::S3::Bucket
- Created only if CurS3BucketOption = CREATE_NEW.
- Stores the exported CUR files.

S3BucketPolicy

- Grants billingreports.amazonaws.com service access to:
    - Read bucket ACL and policy (s3:GetBucketAcl, s3:GetBucketPolicy).
    - Write CUR files into the bucket (s3:PutObject).

CUR Definition (CurDef)

- Type: AWS::CUR::ReportDefinition
- Defines the CUR export properties:
    - Format: textORcsv
    - Compression: ZIP
    - Granularity: HOURLY
    - Additional Data: Includes resource-level details (RESOURCES).
    - Versioning: OVERWRITE_REPORT (new reports overwrite old ones).
    - Exports to the specified bucket/prefix.

IAM Role: AlphausAcctAccessCurRole

- Type: AWS::IAM::Role
- Role Name: AlphausAcctAccessCurRole
- Trust Policy:
    - Trusted by the Alphaus AWS account (Principal parameter).
- Max Session Duration: 12 hours (43,200 seconds).

Attached Policy (inline)

1. S3 Access

    - s3:Get*, s3:List* on the CUR bucket and objects.

2. Cost & Billing Data

    - organizations:List*, organizations:Describe*
    - ec2:DescribeReservedInstances, rds:DescribeReservedDBInstances, elasticache:DescribeReservedCacheNodes, es:DescribeReservedElasticsearchInstances, redshift:DescribeReservedNodes
    - savingsplans:Describe*
    - cur:Describe*, budgets:Describe*
    - ce:Get*, ce:List*, ce:Describe*
    - billingconductor:List*

3. IAM Role Management (scoped)

    - iam:GetRole*, iam:PutRolePolicy restricted to AlphausAcctAccessCurRole.

4. CloudFormation Integration

    - cloudformation:DescribeStack*, cloudformation:UpdateStack* limited to the stack itself.

## Security Considerations

- Scoped Access:

    - S3 permissions are restricted to the specified bucket and objects.
    - IAM actions are restricted to the AlphausAcctAccessCurRole only.

- No Delete Permissions:

    - Unlike the API Access role template, this role does not have destructive permissions (e.g., delete EC2, RDS).

- External Access Control:
    - Alphaus access is controlled via Principal AWS Account ID.