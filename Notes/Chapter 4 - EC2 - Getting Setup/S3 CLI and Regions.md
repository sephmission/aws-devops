# Create a new role in IAM with the following
1. Role Name: MyS3AdminAccess
2. S3FullAccess
3. Create three buckets in S3
4. Upload any file in each buckets

# Create a new EC2 then link the role to the instance
1. Actions -> Instance Settings -> Attach/Replace IAM Role
2. Attach the MyS3Admin Access

# Access the instance in SSH
```
ec2-user
sudo su
aws s3 ls
aws s3 cp --recursive s3://awsdev-sg1 /home/ec2-user --region ap-southeast-1
ls
```
> This will copy the files in the buckets to the ec2 instance directory /home/ec2-user
