# AWS Account Registration

Octo supports registering AWS accounts through either the AWS Console or Terraform. This registration enables Octo to retrieve usage and billing data, perform API operations, and optionally register linked accounts under a payer account.

---

Currently we have 2 steps in registering AWS account in Octo. First is through AWS console, which requires you to sign-in to you account and involves deploying stacks or stackset in your AWS account. Second option is using Terraform module, you can use our  terraform module to deploy the necessary resources in your AWS account. 

**Via AWS Console**

1. **Select Registration Method.** Choose Connect via AWS Console.

   ![AWS Console](https://lh3.googleusercontent.com/d/1yFJbu44o1ue1nR6wZxGcr_IdHllZ6oL4)

2. **Basic Details.** This step will save your account's Id and name if provided.

    a. Input your AWS Account Id (12 digits).

    b. Input Account Name (Optional).

    c. Click Register Account.

    d. If there is no error, then click Next.

   ![Basic details](https://lh3.googleusercontent.com/d/1dicts2_cUrwFxWZBx2dwa2Qvtr9Y2UQH)

3. **Setup API Access.** In this step it will deploy a stack in your AWS account, this will setup needed permission to allow Octo to perfome API Operation in your account.

    a. Click Open AWS create stack page. This will bring you create stack page in your currently signed-in AWS account, make sure you deploy the stack in your intended account, default region would be `us-east-1`.

   ![Stack page](https://lh3.googleusercontent.com/d/1_z9qtqv9qWG7pWvtGVEt2Ucvin8jgDfM)

    b. Please check default values when creating stack:

    - Stack name (You can retain the value or input your desired stack name.)
    - ExternalId (Do not change.)
    - Principal (Do not change.)

   ![Stack values](https://lh3.googleusercontent.com/d/1rDS68nmxXFB_BdnHJpM6qGtowtfqAU08)

    c. Tick the checkbox to agree the I acknowledge that AWS CloudFormation might create IAM resources with custom names. message.

    d. After checking the stack details, click Create stack button. If create stack is success, go back to Octo.

   ![Agreement](https://lh3.googleusercontent.com/d/1kcZPqOxhzWpEyx2Z0OYRt_1ROmpMFgxB)

    e. Click Check and Confirm to verify the deployment.


    f. If verification is success, it would check whether your account is a linked or payer account. If it is linked, you can click the Confirm and Finish button to finish the registration. If payer then click next to proceed with additional steps for payer accounts.

    Linked Account
  ![Linked Account](https://lh3.googleusercontent.com/d/1GCvA890E7KTwQje_2rOGs3AU9aDWNBM8)

   Payer Account
  ![Payer Acc](https://lh3.googleusercontent.com/d/10Vzj9ZFmfG_kAK7XxSNx9diO_E8cuWDF)

4. **Setup Multiple API Access - Optional** (Payer Only). This step will use stackset to deploy API Access in all linked accounts under the payer account. This is useful if your organization have many linked accounts that you want to register to Octo.

    a. Click Open AWS create stackset page. This will bring you to create stackset page in your currently signed-in AWS account, make sure you deploy the stackset in your intended account.

   ![stack page](https://lh3.googleusercontent.com/d/1dicts2_cUrwFxWZBx2dwa2Qvtr9Y2UQH)

    b. In the create stackset page, follow this guide: [Setup multiple account API Access using stackset](https://labs.alphaus.cloud/docs/octo/multiple-account-setup/)

    c. Click check and confirm. This will verify you stackset deployment.

    d. If success, you can click Next.

   ![Payer Acc](https://lh3.googleusercontent.com/d/10Vzj9ZFmfG_kAK7XxSNx9diO_E8cuWDF)

5. **Setup CUR and S3 bucket** (Payer Only). This will deploy stacks for setting up CUR definition in your account, it will also setup a bucket to store your CUR data. You can choose whether to proceed with the default configuration or target S3 bucket in a different region. Another guide can be found [here](https://labs.alphaus.cloud/docs/octo/curs3payer/)

    a. Click AWS create stack page. This will bring you create stack page in your currently signed-in AWS account, make sure you deploy the stack in your intended account.

   ![stack page](https://lh3.googleusercontent.com/d/1dicts2_cUrwFxWZBx2dwa2Qvtr9Y2UQH)

    b. Click check and confirm. This will verify you stack deployments.

    d. If success, you can click Confirm and finish.

**Via Terraform**

Note: You must have terraform installed in your local machine to proceed. You can follow this [guide](https://www.terraform.io/downloads.html).  
(Optional) If you prefer to use AWS CLI for authenticating your AWS account, you can follow this [guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

1. **Select Registration Methodd.** Click Via other options, choose terraform.

   ![Terraform](https://lh3.googleusercontent.com/d/1BVuBUqy9Eju8IWnc3M1wQ7G8I2LlzZQ_)

2. **Basic Details.** This step will save your account's Id and name if provided.

    a. Input your AWS Account Id (12 digit).

    b. Input Account Name (Optional).

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
