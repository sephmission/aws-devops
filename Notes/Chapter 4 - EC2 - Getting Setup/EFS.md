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
4. Login to the instances via SSH
