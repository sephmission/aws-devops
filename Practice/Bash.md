## Daily AWS CLI/Bash Practice

1. Update files
1. Install and update apache
2. Run apache and set apache to be available once instance has started from shutdown
3. Create new file called **index.html** file in html directory with **Hello world**
4. Create new directory called **assets**
5. Check all s3 buckets and select one 
6. Copy .jpg from a s3 bucket to the **assets** directory
6. Add new line in **index.html** with current date/time
7. Make the permissions of the file index.html user **read-only** (from rw-r--r-- to r--------)
8. Make a tar achive file of the **assets** directory then delete **assets folder**
9. Create new directory called **Backup**
10. Move the tar file to the Backup directory
11. Extract tar file
12. Delete tar file
13. Make a new directory called **website** in the var/www/html directory
14. Move all files from the html directory to the **website**
15. Check all EBS volumes
16. Create new file system in the available EBS volume
17. Check if there are any files in the EBS volume
18. Mount the EBS volume to the **website** directory
19. Check the **website** directory
20. Unmount EBS volume

## Commands

```

ec2-user
sudo su
yum update -y
yum install httpd -y
service start httpd
cd /var/www/html
nano index.html
mkdir assets
cd /var/www/html/assets
aws s3 ls
aws s3 cp *.jpg --recursive s3://aws /var/www/html/assets --region ap-southeast-1
cd /var/www/html
nano index.html
mkdir backup
tar cvf backup.tar ./backup
mv backup.tar ./backup
cd /var/www/html/backup
tar xvf backup.tar
cd /var/www/html
mkdir website
lsblk
file -s /dev/xvdf
mkfs -t ext4 /dev/xvdb
mount /dev/xvdb /website
cd /var/www/html/website
umount /dev/xvdb

```
