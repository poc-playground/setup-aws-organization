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

- **Sign up for a general AWS account**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/01-sign-up-general-account.jpg) |
- **Verify your email address**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/02-verify-email.jpg) |
- **Set up the root password**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/03-setup-root-password.jpg) |
- **Provide contact information**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/04-provide-contact-info.jpg) |
- **Provide billing information**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/05-provide-billing-information.jpg) |
- **Confirm identity**<br>![Step 6](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/06-confirm-identity.jpg) |
- **Provide verification code**<br>![Step 7](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/07-provide-verification-code.jpg) |
- **Select a support plan**<br>![Step 8](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/08-select-support-plan.jpg) |
- **Confirm account creation**<br>![Step 9](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/09-account-creation-successful.jpg) |
- **Login to the root account**<br>![Step 10](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/10-login-to-root-account.jpg) |
- **Set up contact details**<br>![Step 11](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/11-setup-contact-details.jpg) |
- **Grant billing info access to IAM user**<br>![Step 12](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/12-billing-info-access-to-iam-user.jpg) |
- **Add MFA to the root user (part 1)**<br>![Step 13](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/13-add-mfa-to-root-user.jpg) |
- **Add MFA to the root user (part 2)**<br>![Step 14](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/14-add-mfa-to-root-user.jpg) |
- **Create an account alias**<br>![Step 15](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/15-create-account-alias.jpg) |
- **Bookmark the sign-in URL**<br>![Step 16](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/16-easy-to-remember-sign-in-url.jpg) |
- **Sign in as root user (part 1)**<br>![Step 17](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/17-sign-in-as-root-user.jpg) |
- **Sign in as root user (part 2)**<br>![Step 18](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/18-sign-in-as-root-user.jpg) |
- **Sign in as root user (part 3)**<br>![Step 19](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/19-sign-in-as-root-user.jpg) |
- **Sign in as root user (part 4)**<br>![Step 20](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/20-sign-in-as-root-user.jpg) |
- **Confirm you are logged in as root user**<br>![Step 21](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/21-logged-in-as-root-user.jpg) |
- **Create a spending budget<br>**![Step 22](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/22-create-a-spending-budget.jpg) |
- **Configure monthly cost budget (part 1)**<br>![Step 23](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/23-create-monthly-cost-budget.jpg) |
- **Configure monthly cost budget (part 2)**<br>![Step 24](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/24-create-monthly-cost-budget.jpg) |
- **Create an IAM user (part 1)**<br>![Step 25](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/25-create-iam-user.jpg) |
- **Create an IAM user (part 2)**<br>![Step 26](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/26-create-iam-user.jpg) |
- **Attach IAM policies**<br>![Step 27](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/27-attach-policy-to-iam-user.jpg) |
- **Finalize IAM admin user creation**<br>![Step 28](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/28-create-iam-admin-user.jpg) |
- **Login as the new IAM admin user**<br>![Step 29](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/29-logged-in-as-iamadmin-user.jpg) |
- **Add MFA to IAM admin user**<br>![Step 30](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/30-add-mfa-for-iamadmin-user.jpg) |

</details>

<details>
<summary><strong>Step 2: Create an AWS Management (Development) Account</strong></summary>

<br>

- **Sign up for a general AWS account**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/31-sign-up-for-development-account.jpg) |
- **Create IAM Admin user and setup MFA**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/32-create-iam-admin-user-for-development-account.jpg)|

  
</details>

<details>
<summary><strong>Step 3: Create an AWS Organization using Management account</strong></summary>

<br>

- **Log in to General AWS Account as IAM User (Administrator Access)**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/33-log-in-to-general-action-as-iam-user.jpg) |
- **Accept the disclairmer and create the organization.**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/34-create-aws-organization.jpg)|
- **An organization gets created with the management account as the root account**.<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/35-aws-organization-created.jpg)|

</details>

<details>
<summary><strong>Step 4: Invite Development account to join the organization</strong></summary>

<br>

- **Log in to General AWS Account as IAM User, go to `AWS Organization`** <br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/36-invite-development-account.jpg) |
- **Select the option to create a new account**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/37-send-an-invitation.jpg)|
- **Log into development account and view the invitation**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/38-view-invitation.jpg)|
- **Accept the invitation to join the organization**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/39-accept-invitation.jpg)|
- **A conformation is displayed**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/40-confirmation-displayed.jpg)|
- **The development account is shown as a member account in the organization**<br>![Step 6](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/41-development-accounts-joins-the-org.jpg)|


</details>

<details>
<summary><strong>Step 5: Create Staging and Production accounts within the Organization</strong></summary>

<br>

- **Log in to General AWS Account as IAM User, go to `AWS Organization`**.<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/42-create-a-staging-aws-account.jpg) |
- **Select the option to create a `Test` (Staging) AWS Account, fill in the details and create the account.**<br>![Step 2](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/43-create-a-staging-aws-account.jpg)|
- **A new account gets created and added to the organization.**<br>![Step 3](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/44-create-a-staging-aws-account.jpg)|
- **Repeat the step to create a `Production` AWS account.**<br>![Step 4](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/45-create-a-production-aws-account.jpg)|
- **The AWS organization is setup with management, development, staging and production accounts**<br>![Step 5](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/46-aws-organization-structure.jpg)|

</details>

<details>
<summary><strong>Step 6: Create two two Organization Units and three additional AWS Accounts</strong></summary>

<br>

- **Log in to General AWS Account as IAM User, go to `AWS Organization` select the root organization and create a two Organizational Units named `Sanbox` and `Production`. Move the Development and Test accounts under Sanbox org unit. Create three additional accounts for `Audit`, '`Identity` and `Log Archive`.**<br>![Step 1](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/47-create-dev-test-org-unit.jpg)|
- **The outline of the AWS Organization will be as follows.** <br>
```mermaid
graph TD
  OrgRoot["AWS Organization Root"]

  OrgRoot --> Security["OU: Security"]
  OrgRoot --> Sandbox["OU: Sandbox"]
  OrgRoot --> Prod["OU: Prod"]

  OrgRoot --> Audit["Account: Audit"]
  OrgRoot --> Billing["Account: Billing / General"]
  OrgRoot --> Identity["Account: Identity"]
  OrgRoot --> LogArchive["Account: Log Archive"]

  Sandbox --> Development["Account: Development"]
  Sandbox --> Test["Account: Test"]
  Prod --> Production["Account: Production"]

````
- **Final Org Structure** <br>![Final Org Structure](https://subhamay-github-images-devl-us-east-1.s3.us-east-1.amazonaws.com/aws-organization-setup/52-final-org-structure.jpg)
</details>

<details>
<summary><strong>Step 7: Setup Landing Zone using AWS Control Tower</strong></summary>
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