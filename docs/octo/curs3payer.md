# CUR and S3 Bucket Setup for Payer Accounts

To pull your AWS data to Octo, there is a need to setup the CUR and S3 bucket for payer accounts. You have two options to choose either **New CUR setup** or **Use existing CUR setup**.

![Option](https://lh3.googleusercontent.com/d/1pbHVkDZ5usS9k3cEq_VEFi5gLZJDn7ZR)
![New or Existing](https://lh3.googleusercontent.com/d/1kMawyTJyjzPHtEAZI_lLG6901TV-za5Z)


## Two deployment ways when setting up the CUR and S3 bucket in New CUR Setup:

![New CUR Setup](https://lh3.googleusercontent.com/d/1kyxqsPK096OCUOzylY3fhgJQ3ynJAmAR)

### Setup CloudFormation using default configuration.
The CUR export settings and the target S3 bucket will be deployed to us-east-1 region.

1. Select `Default configuration`.

![default](https://lh3.googleusercontent.com/d/16cDOmSnK0NHtiPz9FsEI_ldcQ4S5P7qi)

2. Click `Open AWS Create Stack Page`.

![Stack page](https://lh3.googleusercontent.com/d/1an-wADEAFCia0CMUzVWJeSVzjFBIBTlS)

3. Clicking the button above will take you to your CloudFormation console.

4. Please make sure that it is deployed on the default `us-east-1` region.

![Default](https://lh3.googleusercontent.com/d/1bfW_M-ZyXeE8SMRIRAZoNY5zRbfhw2Bk)

5. Once done, come back to Octo and click `Check and Confirm` to start the verification process. If success, you have an option to add a sub account and after that click `Check and Confirm` again and then finish. You have an option also to skip it.

 ![Sub account](https://lh3.googleusercontent.com/d/1w9szAN4XWo0-8I-jdN5wXuCteX7gOkBY)

### Setup target S3 bucket in a different region.
S3 bucket is setup on a desired region aside from us-east-1 region.

1. Select `Target S3 bucket in a different region`.

![Custom region](https://lh3.googleusercontent.com/d/1_09rpltAugn5Ger_Pw0MhL4k84k4-SvC)

2. Under S3 Bucket, click `Open AWS Create Stack Page`.

3. Clicking the button above will take you to your CloudFormation console.

4. Under CUR, click `Open AWS Create Stack Page`.

5. Clicking the link above will take you to your CloudFormation console.

![Stack Page](https://lh3.googleusercontent.com/d/1X0YdJ9bZb_OV_stZvQj0IYVJsD2ctVsH)

6. Provide a stack name.(You can retain the value or input your desired stack name.) Then set the `CurS3BucketOption` parameter to `USE_EXISTING`, then set your `CurS3BucketName` and `CurS3BucketRegion` accordingly.

![Custom region](https://lh3.googleusercontent.com/d/1wjE6LxoaEkdhUH4NtyRuvg6EiDcjNgcx)

7. Once done, come back to this page and click `Check and Confirm` to start the verification process.

![Success Check and Confirm](https://lh3.googleusercontent.com/d/1Q0xSP4JqUKKjL0uEz__OJYVXwBMFqxMp)

8. After that, you have an option to add a sub account, you can click the `Open AWS Create Stack Page` and then click the `Check and Confirm` button to finish.

![Sub Account](https://lh3.googleusercontent.com/d/1FDySMDNz8_rqlE2AtrIVdwa5yR7v1V_P)

If you prefer not to add a sub-account, simply click Skip and finish.

## Setting up the CUR and S3 bucket using existing CUR setup:

![Existing Setup](https://lh3.googleusercontent.com/d/1Qsxx2Su3442rIwTXsX6EmdcE5aH9S6MZ)

1. Click `Open AWS Create Stack Page`.

![Stack Page](https://lh3.googleusercontent.com/d/YOUR_FILE_ID)

2. Clicking the button above will take you to your CloudFormation console.

3. Provide a stack name.(You can retain the value or input your desired stack name.) Then set your `CurS3BucketName` and `CurS3BucketRegion` accordingly to create stack. Note, do not change the `Principal`.

![Existing CUR](https://lh3.googleusercontent.com/d/1g2ZoHzuO6sP3Gpl3OE_TQBF3hD5S1e_K)

4. Once done, come back to this page and click `Check and Confirm` to start the verification process.

![Verify Existing](https://lh3.googleusercontent.com/d/1kqdycA8Oy2bCJX-nPTbcLWnakzR0fDUm)

6. After that, you have an option to add a sub account, you can click the `Open AWS Create Stack Page` and then click the `Check and Confirm` button to finish.

![Sub Account](https://lh3.googleusercontent.com/d/1FDySMDNz8_rqlE2AtrIVdwa5yR7v1V_P)

If you prefer not to add a sub-account, simply click Skip and finish.