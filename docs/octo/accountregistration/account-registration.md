# Account Registration

Octo's cost and usage data rely on the registered cloud service provider's account. On the Account Registration page, you can register, view, edit, or delete your CSP accounts.

![Account Registration](https://lh3.googleusercontent.com/d/1E5-S2QGRbpABwhwEA3N4kKClCTgTbmLY)

## Registering an Account

Account registration allows users to connect their cloud provider accounts to Octo. Supported vendors include AWS, Azure, and GCP. Only admin users can perform account registration.

After registration, it may take up to one day for data to populate in Octo.

### Register AWS Account

To view detailed steps for registering an AWS account,  
 **[Click here to view the AWS Registration Guide](account-registration-aws.md)**

### Register Azure CSP Account

To view detailed steps for registering a Microsoft Azure CSP account,  
 **[Click here to view the Azure Registration Guide](account-registration-azure.md)**

### Register GCP Account

To view detailed steps for registering a Google Cloud account,  
 **[Click here to view the GCP Registration Guide](account-registration-gcp.md)**


---

## Account List

All registered accounts are displayed on the Account Registration page, along with their registration status and account type.  
To access the list, click `More` in the sidebar and select `Account Registration`.

**Account Statuses (AWS Only):**

- `API` – API access is established (Payer and Linked accounts).
- `PAYER` – Indicates a linked account has a payer associated.
- `CUR` – Cost and Usage Report (CUR) and S3 bucket are successfully set up (Payer only).
- `STACKSET` – StackSet for multi-account API access is deployed (Payer only).

---

## Add Sub-account

To add a sub-account to a cloud provider account:

1. Click on the account you wish to add a sub-account to.
2. Click the kebab menu (three dots) on the right side.
3. Select `Add Sub-account`.

---

## Edit Settings

To edit a cloud provider account:

1. Click on the account you wish to edit.
2. Click the kebab menu (three dots) on the right side.
3. Select `Edit Settings`.

### Editable Fields

- In **Basic Details**, you can update the account name.
- The next steps will depend on the cloud vendor and mirror the registration process.

---

## Delete Account

To delete a cloud account from Octo:

1. Click on the account you want to delete.
2. Click the kebab menu (three dots) on the right side.
3. Select `Delete Account`.

> ⚠️ Deleting an account will remove all associated data from our database.
