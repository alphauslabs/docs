# AWS Account Registration

Octo supports registering AWS accounts through AWS Console and Terraform. 

- **AWS console**: requires you sign-in to your AWS account and deploy stacks or stackset in your AWS account.
- **Terraform**: deploy the necessary resources in your AWS account using our terraform module

These registreation methods enable Octo to retrieve usage and billing data, perform API operations, and optionally register linked accounts under a payer account.

## Via AWS Console
### Step 1: Select Registration Method  
   Choose Connect via AWS Console.
   ![AWS Console](https://lh3.googleusercontent.com/d/1yFJbu44o1ue1nR6wZxGcr_IdHllZ6oL4)

### Step 2: Basic Details
!!! note "Recommended to register billing account (AWS payer account)"
    We recommend registering your AWS billing account (payer account) instead of the sub-accounts (linked accounts) as you can have the option to easily include the sub-accounts at the end of this process             

a. Input your AWS Account ID (12 digits)

b. Input Account Name

c. Click Register Account  
   Octo will double check whether existing account has already existed in the system. If the account name or the AWS account ID exist in Octo it will prompt a error banner.

d. If there is no error, then click Next

![Basic details](https://lh3.googleusercontent.com/d/1dicts2_cUrwFxWZBx2dwa2Qvtr9Y2UQH)

### Step 3: Setup API Access  
In this step it will deploy a stack in your AWS account, this will setup needed permission to allow Octo to perfome API Operation in your account. You can learn more about how this is done with CloudFormation template [here]

a. *Click Open AWS create stack page*
   This will bring you create stack page in your currently signed-in AWS account, make sure you deploy the stack in your intended account, default region would be `us-east-1`.

   ![Stack page](https://lh3.googleusercontent.com/d/1_z9qtqv9qWG7pWvtGVEt2Ucvin8jgDfM)

b. In the stack form page in AWS, please check default values when creating stack:

   - Stack name (You can retain the value or input your desired stack name.)
   - ExternalId (Do not change.)
   - Principal (Do not change.)
   ![stack values](https://lh3.googleusercontent.com/d/17NcnsEjKvQX_tzNR_Uj9JbU6JPB5eRSx)

c. Check the stack details and at the end of the page *Tick the checkbox to agree* that says "I acknowledge that AWS CloudFormation might create IAM resources with custom names. message."

d. Click *Create stack button*. If create stack is success, go back to Octo.

   ![Agreement](https://lh3.googleusercontent.com/d/1kcZPqOxhzWpEyx2Z0OYRt_1ROmpMFgxB)

e. Back in Octo, *Click Check and Confirm* to verify the deployment.

f. The verification will check whether your AWS account is a billing (payer account) or a sub-account (linked account)

   **Sub-account (Linked account)**  
   If the account is a sublinked, you can *click the Confirm and Finish* button to finish the registration. 
   ![Linked Account](https://lh3.googleusercontent.com/d/1GCvA890E7KTwQje_2rOGs3AU9aDWNBM8)

   **Biling account (Payer Account)**  
   If payer then *click Next* to proceed with additional steps for payer accounts.
   ![Payer Acc](https://lh3.googleusercontent.com/d/10Vzj9ZFmfG_kAK7XxSNx9diO_E8cuWDF)

### Step 4: Setup CUR and S3 bucket (Payer account only)
If you initially connected to Payer account in the previous step. You will see this step. To pull your AWS data to Octo, there is a need to setup the CUR and S3 bucket for payer accounts. You have two options to choose either **New CUR setup** or **Use existing CUR setup**.

![New or Existing](https://lh3.googleusercontent.com/d/1kMawyTJyjzPHtEAZI_lLG6901TV-za5Z)

#### Setup CloudFormation using default configuration
The CUR export settings and the target S3 bucket will be deployed to us-east-1 region.

1. Select `Default configuration`
![default](https://lh3.googleusercontent.com/d/16cDOmSnK0NHtiPz9FsEI_ldcQ4S5P7qi)

2. Click `Open AWS Create Stack Page`
![Stack page](https://lh3.googleusercontent.com/d/1an-wADEAFCia0CMUzVWJeSVzjFBIBTlS)

3. Clicking the button above will take you to your CloudFormation console

4. Please make sure that it is deployed on the default `us-east-1` region
![Default](https://lh3.googleusercontent.com/d/1bfW_M-ZyXeE8SMRIRAZoNY5zRbfhw2Bk)

5. Once you're done, go back to Octo and click `Check and Confirm` to start the verification process
![Verify New Setup](https://lh3.googleusercontent.com/d/11AfRVtOWofM4BmJCwUPaOwVRS5MFE8H2)

6. If the verification is successful, you'll have the option to add a sub-account. You can either add and click `Check and Confirm` again to finish, or simply skip the sub-account step
![Sub account](https://lh3.googleusercontent.com/d/1w9szAN4XWo0-8I-jdN5wXuCteX7gOkBY)

##### Setup target S3 bucket in a different region.
S3 bucket is setup on a desired region aside from us-east-1 region.

1. Select `Target S3 bucket in a different region`
![Custom region](https://lh3.googleusercontent.com/d/1_09rpltAugn5Ger_Pw0MhL4k84k4-SvC)

2. Under S3 Bucket, click `Open AWS Create Stack Page`

3. Clicking the button above will take you to your CloudFormation console

4. Under CUR, click `Open AWS Create Stack Page`

5. Clicking the button above will take you to your CloudFormation console
![Stack page Custom](https://lh3.googleusercontent.com/d/1IN1hgqiK3_EAWVenbWlLieQ76jivUIPu)

6. Provide a stack name.(You can retain the value or input your desired stack name.) Then set the `CurS3BucketOption` parameter to `USE_EXISTING`, then set your `CurS3BucketName` and `CurS3BucketRegion` accordingly
![Custom region](https://lh3.googleusercontent.com/d/1wjE6LxoaEkdhUH4NtyRuvg6EiDcjNgcx)

7. Once done, come back to this page and click `Check and Confirm` to start the verification process
![Success Check and Confirm](https://lh3.googleusercontent.com/d/1Q0xSP4JqUKKjL0uEz__OJYVXwBMFqxMp)

8. After that, you have an option to add a sub account, you can click the `Open AWS Create Stack Page` and then click the `Check and Confirm` button to finish.
![sub account](https://lh3.googleusercontent.com/d/1AAMLWjX2RyVkKmH_EWBH5E5uswawSHo8)

If you prefer not to add a sub-account, simply click `Skip and finish`

#### Setting up the CUR and S3 bucket using existing CUR setup:

![Existing Setup](https://lh3.googleusercontent.com/d/1Qsxx2Su3442rIwTXsX6EmdcE5aH9S6MZ)

1. Click `Open AWS Create Stack Page`
![Stack page](https://lh3.googleusercontent.com/d/1mOWwGh60MtMp4Eehg_EWMI12ygJe419x)

2. Clicking the button above will take you to your CloudFormation console

3. Provide a stack name.(You can retain the value or input your desired stack name.) Then set your `CurS3BucketName` and `CurS3BucketRegion` accordingly to create stack.
Note, do not change the `Principal`
![Existing CUR](https://lh3.googleusercontent.com/d/1g2ZoHzuO6sP3Gpl3OE_TQBF3hD5S1e_K)

4. Once done, come back to this page and click `Check and Confirm` to start the verification process
![Verify Existing](https://lh3.googleusercontent.com/d/1kqdycA8Oy2bCJX-nPTbcLWnakzR0fDUm)

6. After that, you have an option to add a sub account, you can click the `Open AWS Create Stack Page` and then click the `Check and Confirm` button to finish
![sub account](https://lh3.googleusercontent.com/d/1AAMLWjX2RyVkKmH_EWBH5E5uswawSHo8)

If you prefer not to add a sub-account, simply click `Skip and finish`

### Step 5: Adding sub-accounts (linked accounts)
This step uses stackset to deploy API Access in all sub-accounts (linked accounts) under the billing account (payer account). This is useful if your organization have many linked accounts that you want to register to Octo. 

!!! note "Optional to add sub-accounts immediately"
    You can skip this step and add the sub-accounts later in the billing account details page in Octo.

a. Click Open AWS create stackset page. This will bring you to create stackset page in your currently signed-in AWS account, make sure you deploy the stackset in your intended account.
![Stack page](https://lh3.googleusercontent.com/d/1_z9qtqv9qWG7pWvtGVEt2Ucvin8jgDfM)

    b. In the create stackset page, follow this guide: [Setup multiple account API Access using stackset](https://labs.alphaus.cloud/docs/octo/multiple-account-setup/)

    c. Click check and confirm. This will verify you stackset deployment.

    d. If success, you can click Next.

   ![Payer Acc](https://lh3.googleusercontent.com/d/10Vzj9ZFmfG_kAK7XxSNx9diO_E8cuWDF)

5. **Setup CUR and S3 bucket** (Payer Only). This will deploy stacks for setting up CUR definition in your account, it will also setup a bucket to store your CUR data. You can choose whether to proceed with the default configuration or target S3 bucket in a different region. Another guide can be found [here](../curs3payer.md)


## Via Terraform

Note: You must have terraform installed in your local machine to proceed. You can follow this [guide](https://www.terraform.io/downloads.html).  
(Optional) If you prefer to use AWS CLI for authenticating your AWS account, you can follow this [guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

1. **Select Registration Methodd.** Click Via other options, choose terraform.

   ![Terraform](https://lh3.googleusercontent.com/d/1BVuBUqy9Eju8IWnc3M1wQ7G8I2LlzZQ_)

2. **Basic Details.** This step will save your account's Id and name if provided.

    a. Input your AWS Account Id (12 digit).

    b. Input Account Name.

    c. Click Register Account.

    d. If there is no error, then click Next.

   ![Basic Details](https://lh3.googleusercontent.com/d/1w1wob0ikOhoK42oigOCWxkd6jbRFAUsw)

3. Check this [terraform module](https://registry.terraform.io/modules/alphauslabs/octo/aws/latest), from there you can read it's README section for more detailed information about the module and the required inputs.

4. Run **terraform init**, this initializes a working directory containing Terraform configuration files, **terraform plan** to check what resources will be created, and **terraform apply** to create those resources. You can also check [here](https://developer.hashicorp.com/terraform/cli) for more information about the Terraform CLI.

5. After running those commands above, check if the deployments are successful, if so, click **Check and confirm** to verify. You can also check in your AWS account console to see if the resources are properly created.

6. On Octo, you can see the status of the deployments for API Access, CUR and S3 bucket (For payer account only), and multiple account API access - optional (For payer account only).

7. If API Access is success, you can click **Confirm and Finish**.

   ![Terraform Finish](https://lh3.googleusercontent.com/d/1HqhAppraKZ_-mmNGRxsMiotNf1XPOf6x)

For Payer accounts, if it's registered without using stackset, you can still enable it by doing the steps above, just make sure you set the **use_stackset** to true in the terraform module, it will update the resources and automatically register all your linked account to Octo, there is no need to delete your payer account and register again.
