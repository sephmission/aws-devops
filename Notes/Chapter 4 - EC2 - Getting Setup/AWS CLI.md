# AWS CLI

Login to the instance via SSH using `ec2-user` then raise to privilege to root
`sudo su`

## AWS CLI

Check AWS s3 service. *No s3 buckets configured*
```
aws s3 ls
```

Configure AWS
```
aws configure
```

Then enter the following:
* AWS Access Key ID
* AWS Secret Key
* Region Name: *check reference below*
* Default output format: *Leave blank*

> Access and Secret Key can be located from the .csv file downloaded from **IAM**. For default region name reference: [https://docs.aws.amazon.com/general/latest/gr/rande.html](https://docs.aws.amazon.com/general/latest/gr/rande.html)

Check again the AWS s3 service, if any
`aws s3 ls`

Check help commands
`aws s3 help`

Go to the bottom to see the available commands, for example:
* cp - copy
* ls - list
* mb - make bucket
* mv - move files

To check where the credentials are stored, to to home directory
```
cd ~
ls
cd .aws
ls
nano credentials
```
### To self-descruct an ec2 instance
Check information of the instances
```
aws ec2 describe-instances
```

Copy InstanceID then terminate instance
```
aws ec2 terminate-instances --instance-ids [instance_id]
```
