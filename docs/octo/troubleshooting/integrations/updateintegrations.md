# Updating Your AWS Account API Access

This guide walks you through updating the **AlphausAccountAccess** CloudFormation stack for your AWS billing account. Follow the steps below, and refer to the [Troubleshooting](#troubleshooting) section if you encounter any issues. Contact customer support by clicking the **Contact Support** button in the Octo UI if the error you are experiencing isn’t documented here. 

---

## Step 1: Delete the Existing Stack in AWS

1. Click **Open AWS stack page** in Octo. Ensure you are signed in to the correct AWS billing account.
![stack console](https://lh3.googleusercontent.com/d/1YXddPFO8fdYE7U0MQuK0LODSVJDgGeoc)
2. In the Stacks page, locate and select **AlphausAccountAccess**, then click **Delete**.
![stack console](https://lh3.googleusercontent.com/d/1rAn_bM1Lmg5gt9R1O3cRBj22V2HQAgDQ)
3. Confirm the deletion and wait for it to complete.
![delete](https://lh3.googleusercontent.com/d/1yXej6lMZqP5w0YgAH2E18DWhPJDyhKpB)
4. If you have a StackSet deployed, delete it as well before proceeding.
![delete stackset](https://lh3.googleusercontent.com/d/1ciBL_71jmUtw2T0-65USiwpwRzzNI4E-)
![active](https://lh3.googleusercontent.com/d/1RGFwMtKEHpp00qEFOP32mxpG_5kBVqPj)
Here is the step by step process of deleting the stack.
- Select the stackset. Click Actions and click delete stacks from stacke set. *This is done to delete initially the deployed stacks per linked accounts*.
![step1](https://lh3.googleusercontent.com/d/1MsTBbra38MJ3h5i_XVsmsWkFRFtvENGv)
- Provide the root Id and select the Region. Click Next.
![step2](https://lh3.googleusercontent.com/d/1hWeR6llSvhBeyfjDBp3qMW9jXzasahAX)
- Review and click Submit.
![step3](https://lh3.googleusercontent.com/d/1bF5PFvczkVE4WIWjhDOaF_dwBM72hUCp)
- Go back to the listing page. Click the stackset, click Actions and click Delete stack set.
![step4](https://lh3.googleusercontent.com/d/1XmmiZV18-9ZEvRkFt-Yy6xNG9TdRk2c-)

---

## Step 2: Deploy the New Stack

1. Click **Open AWS Create Stack Page** in Octo. Ensure you are signed in to the correct AWS billing account.
![deploy new](https://lh3.googleusercontent.com/d/1x6Ilaj-jkiiKdQhlxX8t9FUneZ-mZ16g)
2. Review the pre-filled parameters. For **TargetOrganizationId**:
    - Enter your AWS Organization Unit ID (e.g. `ou-xxxx-xxxx`) or Root ID (e.g. `r-xxxx`) to automatically include all linked accounts.
    - Leave it **blank** to set up linked account access later, or if you are updating a sub-account.
![stack values](https://lh3.googleusercontent.com/d/1ZzPpl0v50cGqHoHT9Wqm7r1eOluTty5j)
3. Click **Create stack** and wait 1–3 minutes for deployment to complete.

!!! info
    If you provided a `TargetOrganizationId`, a StackSet granting access to all linked accounts will also be deployed automatically.

---

## Step 3: Confirm Access in Octo

Once the stack is deployed, return to Octo:

- Click **Check and confirm API access** — Octo will verify the stack was deployed correctly and that API access is active.
- *(Payer accounts only)* Click **Check and confirm sub-accounts access** to verify the StackSet is active. If you left `TargetOrganizationId` blank, you can enable this at any time from the account details page.

---

## Troubleshooting

### I entered the wrong Organization ID

1. Delete the **AlphausAccountAccess** stack (see [Step 1](#step-1-delete-the-existing-stack-in-aws)).
2. Redeploy using [Step 2](#step-2-deploy-the-new-stack) with the correct `TargetOrganizationId`.

---

### I registered a sub-account before its payer account

When you later register the payer account with a `TargetOrganizationId`, it may conflict with the sub-account's existing stack.

!!! warning
    The sub-account name from the previous registration will be overwritten.

1. Delete the **AlphausAccountAccess** stack in the **sub-account**.
![failed state](https://lh3.googleusercontent.com/d/13OPEtokt1vvSnkGa94jsKdjsGLJ-tmfq)
2. Delete the **AlphausAccountAccess** stack in the **payer account** that is showing the error.
![stack console](https://lh3.googleusercontent.com/d/1rAn_bM1Lmg5gt9R1O3cRBj22V2HQAgDQ)
![delete](https://lh3.googleusercontent.com/d/1yXej6lMZqP5w0YgAH2E18DWhPJDyhKpB)
3. Redeploy using [Step 2](#step-2-deploy-the-new-stack).


---

### I opened the AWS stack page but I'm signed in to the wrong AWS account

The **Open AWS stack page** and **Open AWS Create Stack Page** buttons open directly in whichever AWS account is currently active in your browser. If you are signed in to the wrong account, the **AlphausAccountAccess** stack will not be found, or changes will be applied to the wrong account.

To fix this:

1. In the AWS Console, click your account name in the top-right corner and select **Sign out**.
2. Sign in to the correct AWS billing account.
3. Return to Octo and click the button again to reopen the page under the correct account.

!!! tip
    You can verify you are in the right account by checking that the 12-digit **Account ID** shown in the AWS Console top-right matches the AWS Account ID registered in Octo.