# What is EBS?
Amazon EBS allows you to create storage volumes and attach them to Amazon EC2 instances. Once attached, you can create a file system on top of these volumes, run a database, or use them in any other way you would use a block device. Amazon EBS volumes are placed in a specific Availability Zone, where they are automatically replicated to protect you from the failure of a single component.

## EBS Volume Types
* **General Purpose SSD (GP2)**
  * General purpose, balances both price and performance
  * Ratio of 3 IOPS per GB with up to 10,000 IOPS and the ability to burst up to 3000 IOPS for extended periods of time for volumes under 1Gib.
* **Provisioned IOPS SSD (IO1)**
  * Designed for I/O intensive applications such as large relational or NoSQL databases.
  * Use if you need more than 10,000 IOPS.
  * Can provision up to 20,000 IOPS per volume
* **Throughput Optimized HDD (ST1)**
  * Big data
  * Data Warehouses
  * Log processing
  * Cannot be a boot volume
* **Cold HDD (SC1)**
  * Lowest Cost Storage for infrequently accessed workloads
  * File Server
  * Cannot be a boot volume
* **Magnetic (Standard)**
  * Lowest cost per gigabyte of all EBS volume types that is bootable. Magnetic volumes are ideal for workloads where data is accessed infrequently, and applications where the lowest storage cost is important.

## Exam Tips in EC2
* Know the difference between:
  * On Demand
  * Spot
  * Reserved
  * Dedicated Hosts
* Remember with spots instances:
  * If you terminate the instance, you pay for the hour
  * If AWS terminates the spot instance, you get the hour it was terminated in for free.
  
## Exam Tips in EBS
* EBS Consist of:
  * SSD, General Purpose - GP2 - (Up to 10,000 IOPS)
  * SSD, Provisioned IOPS - IO1 - (More than 10,000 IOPS)
  * HDD, Throughput Optimized - ST1 - frequently accessed workloads
  * HDD, Cold - SC1 - less frequently accessed data
  * HDD, Magnetic - Standard - cheap, infrequently accessed storage
* You cannot mount 1 EBS volume to multiple EC2 instances, instead use EFS.
* Termination Protection is turned off by default, you must turn it on.
* On an EBS-backed instance, the default action is for the root EBS volume to be deleted when the instance is terminated.
* EBS Root Volumes of your DEFAULT AMI's cannot be encrypted. You can also use a third party tool (such as bit locker, etc.) to encrypt the root volume, or this can be done when creating AMI's in the AWS console or using the API.
* Additional volumes can be encrypted.
* EBS Volumes can be changed on the fly (except for magnetic standard).
* Best practice to stop the EC2 instance and then change the volume
* You can change volume types by taking a snapshot and then using the snapshot to create a new volume
* If you can change a volume on the fly you must wait for 6 hours before making another change
* You can scale EBS Volumes up only
* Volumes must be in the same AZ as the EC2 instances
