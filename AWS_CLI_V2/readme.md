# Create Access Key for CLI
- IAM -> User -> select a user
- Security Credential -> Create Access Key -> CLI

- You can also do cmd lines in Cloud Shell


# Login
```cmd
aws configure
AWS Access Key ID [None]: ***Access key ID***
AWS Secter Access Key [None]: ***Secter Access key***
Default region name [None]: ***us-east-1***
Default output format [None]: *** ***
``` 

# Commands
- Get all users
```cmd
~ aws iam list-users

{
    "Users": [
        {
            "Path": "/",
            "UserName": "admin0",
            "UserId": "AIDAUEHCLRIAJDNOQV2E2",
            "Arn": "arn:aws:iam::283942554112:user/admin0",
            "CreateDate": "2023-08-01T03:44:42+00:00"
        }
    ]
}
```
