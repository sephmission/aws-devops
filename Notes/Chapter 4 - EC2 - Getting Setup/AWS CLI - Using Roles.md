# AWS CLI using Roles - Lab

1. Go to IAM service
2. Create new role
3. Select: **Amazon EC2**
4. Type in the filter: **s3**
5. Select **AmazonS3FullAccess**
6. Input Role Name: **S3-Admin-Access**
7. Create an EC2 Instance with IAM role: **S3-Admin-Access**
8. Login into the instance via SSH using `ec2-user` and check amazon s3
```
sudo su
aws s3 ls
```

#### Reminders:
- All roles are global.

#### Resources:
* [AWS switching Roles using CLI](https://aws.amazon.com/blogs/security/new-attach-an-aws-iam-role-to-an-existing-amazon-ec2-instance-by-using-the-aws-cli/)
* [AWS switching Roles using console](https://aws.amazon.com/blogs/security/easily-replace-or-attach-an-iam-role-to-an-existing-ec2-instance-by-using-the-ec2-console/)
