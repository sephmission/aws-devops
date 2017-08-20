# Create new Instance with additional Magnetic volume

1. Access via SSH then login as `ec2-user`
2. Check disk volumes
``
lsblk
``
3. Create new file system in the new volume `xvdb`
```
mkfs -t ext4 /dev/xvdb
mkdir /awsdev
```
4. Mount volume to the directory
``
mount /dev/xvdb /awsdev
``
