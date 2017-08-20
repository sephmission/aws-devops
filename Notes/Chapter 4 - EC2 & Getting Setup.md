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

## Snapshot

Unmount the volume from the directory then create a new snapshot.
```
cd /
umount /dev/xvdb
```
1. Right-click the volume then create new snapshot
2. Go to the snapshot menu then create new volume with volume type of **Provisioned IOPS SSD (IO1)**.
3. Attach the new volume to the instance.

> Make sure you create the new volume from the snapshot in the same Availability Zone (AZ) as the instance you want to attach to.

Access the instance via SSH then check if the new volume has been attached. Then check the file system if there are any files.
```
lsblk
file -s /dev/xvdf
```

Mount the new volume to the `/awsdev` directory and check if the file *index.html* is in the directory.
```
mount /dev/xvdf /awsdev
cd /awsdev
ls
```

# Exam Tips
- EBS Volumes can be changed on the fly (except for magnetic standard).
- Best practice to stop the EC2 instance and then change the volume
- You can change volume types by taking a snapshot and then using the snapshot to create a new volume
- If you can change a volume on the fly you must wait for 6 hours before making another change
- You can scale EBS Volumes up only
- Volumes must be in the same AZ as the EC2 instances



