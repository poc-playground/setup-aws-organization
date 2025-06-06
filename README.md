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

| Step | Description                                   | Screenshot |
|:-----|:----------------------------------------------|:-----------|
| 1    | Sign up for a general AWS account             |![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/01-sign-up-general-account.jpg) |
| 2    | Verify your email address                     |![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/02-verify-email.jpg) |
| 3    | Set up the root password                      |![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/03-setup-root-password.jpg) |
| 4    | Provide contact information                   |![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/04-provide-contact-info.jpg) |
| 5    | Provide billing information                   |![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/05-provide-billing-information.jpg) |
| 6    | Confirm identity                              |![Step 6](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/06-confirm-identity.jpg) |
| 7    | Provide verification code                     |![Step 7](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/07-provide-verification-code.jpg) |
| 8    | Select a support plan                         |![Step 8](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/08-select-support-plan.jpg) |
| 9    | Confirm account creation                      |![Step 9](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/09-account-creation-successful.jpg) |
| 10   | Login to the root account                     |![Step 10](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/10-login-to-root-account.jpg) |
| 11   | Set up contact details                        |![Step 11](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/11-setup-contact-details.jpg) |
| 12   | Grant billing info access to IAM user         |![Step 12](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/12-billing-info-access-to-iam-user.jpg) |
| 13   | Add MFA to the root user (part 1)             |![Step 13](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/13-add-mfa-to-root-user.jpg) |
| 14   | Add MFA to the root user (part 2)             |![Step 14](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/14-add-mfa-to-root-user.jpg) |
| 15   | Create an account alias                       |![Step 15](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/15-create-account-alias.jpg) |
| 16   | Bookmark the sign-in URL                      |![Step 16](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/16-easy-to-remember-sign-in-url.jpg) |
| 17   | Sign in as root user (part 1)                 |![Step 17](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/17-sign-in-as-root-user.jpg) |
| 18   | Sign in as root user (part 2)                 |![Step 18](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/18-sign-in-as-root-user.jpg) |
| 19   | Sign in as root user (part 3)                 |![Step 19](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/19-sign-in-as-root-user.jpg) |
| 20   | Sign in as root user (part 4)                 |![Step 20](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/20-sign-in-as-root-user.jpg) |
| 21   | Confirm you are logged in as root user        |![Step 21](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/21-logged-in-as-root-user.jpg) |
| 22   | Create a spending budget                      |![Step 22](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/22-create-a-spending-budget.jpg) |
| 23   | Configure monthly cost budget (part 1)        |![Step 23](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/23-create-monthly-cost-budget.jpg) |
| 24   | Configure monthly cost budget (part 2)        |![Step 24](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/24-create-monthly-cost-budget.jpg) |
| 25   | Create an IAM user (part 1)                   |![Step 25](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/25-create-iam-user.jpg) |
| 26   | Create an IAM user (part 2)                   |![Step 26](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/26-create-iam-user.jpg) |
| 27   | Attach IAM policies                           |![Step 27](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/27-attach-policy-to-iam-user.jpg) |
| 28   | Finalize IAM admin user creation              |![Step 28](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/28-create-iam-admin-user.jpg) |
| 29   | Login as the new IAM admin user               |![Step 29](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/29-logged-in-as-iamadmin-user.jpg) |
| 30   | Add MFA to IAM admin user                     |![Step 30](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/30-add-mfa-for-iamadmin-user.jpg) |

</details>

<details>
<summary><strong>Step 2: Create an AWS Management (Development) Account</strong></summary>

<br>

| Step | Description                                   | Screenshot |
|:-----|:----------------------------------------------|:-----------|
| 1    | Sign up for a general AWS account             |![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/31-sign-up-for-development-account.jpg) |
| 2    | Create IAM Admin user and setup MFA           |![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/32-create-iam-admin-user-for-development-account.jpg)|

  
</details>

<details>
<summary><strong>Step 3: Create an AWS Organization using Management account</strong></summary>

<br>

| Step | Description                                                                  | Screenshot |
|:-----|:-----------------------------------------------------------------------------|:-----------|
| 1    | Log in to General AWS Account as IAM User (Administrator Access)             |![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/33-log-in-to-general-action-as-iam-user.jpg) |
| 2    | Accept the disclairmer and create the organization                           |![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/34-create-aws-organization.jpg)|
| 3    | An organization gets created with the management account as the root account |![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/35-aws-organization-created.jpg)|

</details>

<details>
<summary><strong>Step 4: Invite Development account to join the organization</strong></summary>
</details>

<details>
<summary><strong>Step 5: Create Staging and Production accounts within the Organization</strong></summary>
</details>

<details>
<summary><strong>Step 6: Create two organization units (Dev-Test) and Prod</strong></summary>
</details>

<details>
<summary><strong>Step 7: Configure Service Control Policy</strong></summary>
</details>

<details>
<summary><strong>Step 8: Configure Tag Policy</strong></summary>
</details>