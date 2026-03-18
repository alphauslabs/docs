# Troubleshooting AWS Account Registration

## Scenario 1: Adding Linked Accounts After Skipping During Payer Registration

This applies if you registered a payer account without providing a `TargetOrganizationId` (or didn't know your Organization ID at the time), and now want to add your linked accounts.

1. Go to **AWS CloudFormation** > **Stacks**, then locate the **AlphausAccountAccess** stack.

2. Click the radio button next to it, then click the **Update stack** button. In the dropdown, select **Make a direct update**.

3. Click **Next**.

4. Locate the **TargetOrganizationId** parameter and supply your OU ID or Root ID. Click **Next**.

5. Check the checkbox under **Capabilities**.

6. Review the change set. You should see an additional action for **AlphausOrgStackset** — this deploys permissions to your linked accounts similar to the payer account stack. Click **Submit**.

---

## Scenario 2: Payer Account Registered with a Wrong Organization ID

1. Click the **AlphausAccountAccess** stack, then click the **Delete stack** button and follow the instructions in the deletion modal.

2. Once deleted, click the **Open AWS Create Stack Page** button again and follow the setup instructions with the correct `TargetOrganizationId`.

---

## Scenario 3: Sub-account Registered Before Its Payer Account

This applies if you registered a sub-account first, then registered its payer account and provided a `TargetOrganizationId`.

!!! warning
    The sub-account name provided in the previous registration will be overwritten.

1. Delete the **AlphausAccountAccess** stack deployed in the sub-account.

2. Delete the **AlphausAccountAccess** stack deployed in the payer account that is showing the error.

3. Click the **Open AWS Create Stack Page** button again and follow the setup instructions.
