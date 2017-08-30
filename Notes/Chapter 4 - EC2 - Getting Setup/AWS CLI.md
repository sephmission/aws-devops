# AWS CLI labs

1. Login to the instance via SSH using `ec2-user` then raise to privilege to root

```
sudo su
```

2. Check AWS s3 service. *No s3 buckets configured*

```
aws s3 ls
```

3. Configure AWS

```
aws configure
```

4. Then enter the following:
* AWS Access Key ID
* AWS Secret Key
* Region Name: *check reference below*
* Default output format: *Leave blank*

> Access and Secret Key can be located from the .csv file downloaded from **IAM**. For default region name reference: [https://docs.aws.amazon.com/general/latest/gr/rande.html](https://docs.aws.amazon.com/general/latest/gr/rande.html)

5. Check again the AWS s3 service, if any

```
aws s3 ls
```

6. Check help commands

```
aws s3 help
```

7. Go to the bottom to see the available commands, for example:
* cp - copy
* ls - list
* mb - make bucket
* mv - move files

8. To check where the credentials are stored, to to home directory

```
cd ~
ls
cd .aws
ls
nano credentials
```

9.  To self-descruct an ec2 instance

*Check information of the instances*

```
aws ec2 describe-instances
```

10. Copy InstanceID then terminate instance

```
aws ec2 terminate-instances --instance-ids [instance_id]
```
