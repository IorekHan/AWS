# Table of Contents
- [Intro](#intro)
- [Create IAM User](#create-iam-user)
- [IAM User Login](#iam-user-login)
- [MFA](#mfa)
- [Password Policy](#password-policy)
- [Role](#role)
- [Security Tools](#security-tools)
  - [IAM Credentials Report](#iam-credentials-report)
  - [IAM Access Advisor](#iam-access-advisor)


# Intro
IAM is Identity and Access Management, this is a global service, not regional.

A Root Account is created automatically which is not able to be changed or used by others.

IAM provides users, groups and policy applied to them.

# Create IAM User
- Go to IAM console by search in AWS
- Go to User
- Create Use


# IAM User Login
- Use the URL under "Sign-in URL for IAM users in this account" in the root account IAM console under
- Use the IAM account and account ID to login.

# MFA
- Multi Factor Authentication
- Password + security device (virtual, physical)
- Root user can use Security credentials to Assign MFA devices

# Password Policy
- In IAM Account Settings

# Role
- Services in AWS suppots role with self-defined policy.
- IAM -> Role -> Create Role to create own roles.

# Security Tools
- IAM Credentials Report (account-level): Users
- IAM Access Advisor (user-level): Permissions
- IAM -> Credential reports
