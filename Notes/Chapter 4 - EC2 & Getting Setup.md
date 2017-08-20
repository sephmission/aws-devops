# EBS

Create new instance in EC2 with additional magnetic volume. Access the instance via SSH then login then check the existing volumes. If there's no file system yet, create new file system in the *magnetic* volume called `/dev/xvdb`.

```
lsblk
ec2-user
lsblk
mkfs -t ext4 /dev/xvdb
```

## Mounting a volume

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

## Unmounting a volume

Go back to the root directory then unmount the volume `/dev/xvdb`. Check the `/awsdev` directory and there should be **no files**.
```
cd /
umount /dev/xvdb
cd /awsdev
ls
```

Mount the volume again to the directory and check if the files are now visible.
```
cd /
mount /dev/xvdb /awsdev
ls
```

