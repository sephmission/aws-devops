# What is EFS?
Amazon Elastic File System (Amazon EFS) is a file storage service for Amazon Elastic Compute Cloud (Amazon EC2) instances. Amazon EFS is easy to use and provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon EFS, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your application have the storage they need, when they need it.

## EFS Features
* Supports the Network File System version 4 (NFSv4) protocol
* You only pay for the storage you use (no pre-provisioning required)
* Can scale up to the petabytes
* Can support thousands of concurrent NFS connections
* Data is stored across multiple AZ's within a region
* Read After White Consistency
* Block by Storage

# EFS Lab
1. Create two (2) EC2 instances in Sydney where EFS is supported with different Subnets (a and b).
2. Provision Classic Load Balancers with security group. Change the health check interval to **10 seconds** and threshold to **3**. Then assign the load balancers to the 2 instances.
3. Note the public IP address of the EC2 instances for login.
> Make sure that the instances are with the same Security Group of the EFS. *Add the default security group*.
4. Login to **BOTH** instances via SSH, use `ec2-user`
5. Raise the privelges to root.

```
sudo su
```

6. Install apache, start service then go to the root directory

```
yum install httpd -y
service httpd start
cd /
```

7. Go to EFS then check **EC2 mount instructions**, Example: 

```
sudo mount -t nfs4 -o *************************** efs` but change `efs` to the html folder. Use `sudo mount -t nfs4 -o *************************** /var/www/html
```

8. Apply mount instructions to CLI of the first instance then check html folder then create a file

```
sudo mount -t nfs4 -o *************************** /var/www/html
cd html
nano index.html
```

9. On the second instance, check the html folder if it has the file file from the first instance. It should be there.
10. Check the load balancers if the status is now *InService*.
