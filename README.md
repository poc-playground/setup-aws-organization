# AWS Organization Setup Guide

This guide provides step-by-step instructions to create an AWS Organization, set up Organizational Units (OUs), and provision new AWS accounts using the AWS Management Console.

---

## 🧰 Prerequisites

- Access to an email account with support for dynamic alias.
- A valid credit card.
- A virtual MFA device (1Password has been used in this setup)


---

## 🏗️ Step-by-Step Instructions



<details>
<summary><strong>Step 1: Create an AWS Management (General) Account</strong></summary>

<br>

| Step |
|:-----|
| **1. Sign up for a general AWS account**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/01-sign-up-general-account.jpg) |
| **2. Verify your email address**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/02-verify-email.jpg) |
| **3. Set up the root password**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/03-setup-root-password.jpg) |
| **4. Provide contact information**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/04-provide-contact-info.jpg) |
| **5.Provide billing information**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/05-provide-billing-information.jpg) |
| **6.Confirm identity**<br>![Step 6](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/06-confirm-identity.jpg) |
| **7.Provide verification code**<br>![Step 7](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/07-provide-verification-code.jpg) |
| **8.Select a support plan**<br>![Step 8](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/08-select-support-plan.jpg) |
| **9.Confirm account creation**<br>![Step 9](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/09-account-creation-successful.jpg) |
| **10.Login to the root account**<br>![Step 10](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/10-login-to-root-account.jpg) |
| **11.Set up contact details**<br>![Step 11](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/11-setup-contact-details.jpg) |
| **12.Grant billing info access to IAM user**<br>![Step 12](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/12-billing-info-access-to-iam-user.jpg) |
| **13.Add MFA to the root user (part 1)**<br>![Step 13](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/13-add-mfa-to-root-user.jpg) |
| **14.Add MFA to the root user (part 2)**<br>![Step 14](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/14-add-mfa-to-root-user.jpg) |
| **15.Create an account alias**<br>![Step 15](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/15-create-account-alias.jpg) |
| **16. Bookmark the sign-in URL**<br>![Step 16](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/16-easy-to-remember-sign-in-url.jpg) |
| **17. Sign in as root user (part 1)**<br>![Step 17](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/17-sign-in-as-root-user.jpg) |
| **18. Sign in as root user (part 2)**<br>![Step 18](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/18-sign-in-as-root-user.jpg) |
| **19. Sign in as root user (part 3)**<br>![Step 19](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/19-sign-in-as-root-user.jpg) |
| **20. Sign in as root user (part 4)**<br>![Step 20](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/20-sign-in-as-root-user.jpg) |
| **21. Confirm you are logged in as root user**<br>![Step 21](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/21-logged-in-as-root-user.jpg) |
| **22. Create a spending budget<br>**![Step 22](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/22-create-a-spending-budget.jpg) |
| **23. Configure monthly cost budget (part 1)**<br>![Step 23](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/23-create-monthly-cost-budget.jpg) |
| **24. Configure monthly cost budget (part 2)**<br>![Step 24](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/24-create-monthly-cost-budget.jpg) |
| **25. Create an IAM user (part 1)**<br>![Step 25](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/25-create-iam-user.jpg) |
| **26. Create an IAM user (part 2)**<br>![Step 26](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/26-create-iam-user.jpg) |
| **27. Attach IAM policies**<br>![Step 27](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/27-attach-policy-to-iam-user.jpg) |
| **28. Finalize IAM admin user creation**<br>![Step 28](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/28-create-iam-admin-user.jpg) |
| **29. Login as the new IAM admin user**<br>![Step 29](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/29-logged-in-as-iamadmin-user.jpg) |
| **30. Add MFA to IAM admin user**<br>![Step 30](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/30-add-mfa-for-iamadmin-user.jpg) |

</details>

<details>
<summary><strong>Step 2: Create an AWS Management (Development) Account</strong></summary>

<br>

| Step |
|:-----|
| **1 . Sign up for a general AWS account**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/31-sign-up-for-development-account.jpg) |
| **2 . Create IAM Admin user and setup MFA**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/32-create-iam-admin-user-for-development-account.jpg)|

  
</details>

<details>
<summary><strong>Step 3: Create an AWS Organization using Management account</strong></summary>

<br>

| Step | Description                                                               . Screenshot |
|:-----|:-----------------------------------------------------------------------------|:-----------|
| **1. Log in to General AWS Account as IAM User (Administrator Access)**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/33-log-in-to-general-action-as-iam-user.jpg) |
| **2. Accept the disclairmer and create the organization.**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/34-create-aws-organization.jpg)|
| **3. An organization gets created with the management account as the root account**.<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/35-aws-organization-created.jpg)|

</details>

<details>
<summary><strong>Step 4: Invite Development account to join the organization</strong></summary>

<br>

| Step |
|:-----|
| **1. Log in to General AWS Account as IAM User, go to `AWS Organization`** <br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/36-invite-development-account.jpg) |
| **2. Select the option to create a new account**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/37-send-an-invitation.jpg)|
| **3. Log into development account and view the invitation**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/38-view-invitation.jpg)|
| **4. Accept the invitation to join the organization**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/39-accept-invitation.jpg)|
| **5. A conformation is displayed**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/40-confirmation-displayed.jpg)|
| **6. The development account is shown as a member account in the organization**<br>![Step 6](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/41-development-accounts-joins-the-org.jpg)|


</details>

<details>
<summary><strong>Step 5: Create Staging and Production accounts within the Organization</strong></summary>

<br>

| Step |
|:-----|
| **1. Log in to General AWS Account as IAM User, go to `AWS Organization`** <br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/42-create-a-staging-aws-account.jpg) |
| **2. Select the option to create a staging (test) AWS Account, fill in the details and create the account**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/43-create-a-staging-aws-account.jpg)|
| **3. A new account gets created and added to the organization**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/44-create-a-staging-aws-account.jpg)|
| **4. Repeat the step to create a production AWS account**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/45-create-a-production-aws-account.jpg)|
| **5. The AWS organization is setup with management, development, staging and production accounts**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/46-aws-organization-structure.jpg)|

</details>

<details>
<summary><strong>Step 6: Create two three Organization Units and five AWS Accounts</strong></summary>

<br>

| Step | 
|:-----|
| **1. Log in to General AWS Account as IAM User, go to `AWS Organization` select the root organization and create a new `Organizational Unit` named `Sandboxes`** <br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/47-create-dev-test-org-unit.jpg) |
| **2. Similarly create another organization unit named `Prod`**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/48-create-prod-org-unit.jpg)|
| **3. Move the development and test accounts under `dev-test` org unit and production account under `Prod` org unit**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/49-move-accounts-to-org-unit.jpg)|
| **4. Enable service control and tag policies**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/50-enable-scp-and-tag-policy.jpg)|
| **5. Service control and tag policies enableld**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/51-scp-and-tag-policy-enabled.jpg)|

</details>

<details>
<summary><strong>Step 7: Enhance the Organization Structure by following the best practices</strong></summary>

<br>

```mermaid
graph TD
  OrgRoot["AWS Organization Root"]

  OrgRoot --> Security["OU: Security"]
  OrgRoot --> Sandboxes["OU: Sandboxes"]
  OrgRoot --> Prod["OU: Prod"]

  Security --> Audit["Account: Audit"]
  Security --> Billing["Account: Billing / General"]
  Security --> Identity["Account: Identity"]
  Security --> LogArchive["Account: Log Archive"]

  Sandboxes --> Development["Account: Development"]
  Sandboxes --> Test["Account: Test"]

  Prod --> Production["Account: Production"]


```

![Final Org Structure](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/52-final-org-structure.jpg)
</details>

<details>
<summary><strong>Step 9: Setup Landing Zone using AWS Control Tower</strong></summary>
</details>

<details>
<summary><strong>Step 8: Configure Service Control Policy - Management Account</strong></summary>
</details>

<details>
<summary><strong>Step 9: Configure Service Control Policy - Identity Account</strong></summary>
</details>


<details>
<summary><strong>Step 8: Configure Tag Policy</strong></summary>
</details>