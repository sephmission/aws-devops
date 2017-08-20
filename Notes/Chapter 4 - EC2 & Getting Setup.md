# Create new Instance with additional Magnetic volume

Access the instance via SSH then login then check the existing volumes. If there's no file system yet, create new file system in the *magnetic* volume called `/dev/xvdb`.

```
lsblk
ec2-user
lsblk
mkfs -t ext4 /dev/xvdb
```

Create new directory called *awsdev* then mount the magnetic volume `/dev/xvdb` to the directory.
```
mkdir /awsdev
mount /dev/xvdb /awsdev
```

Check the volumes if the new directory has been attached to the magnetic volume. Then access the `/awsdev` directory and check all files listed. Create a new file called *index.html* in the current directory.
```
lsblk
cd /awsdev
ls
nano index.html
ls
```
