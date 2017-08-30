# Most Frequently Used UNIX / Linux Commands (With Examples)

### Tar command examples
```
# Create a new tar archive
$ tar cvf archive_name.tar dirname/

# Extract from an existing tar archive.
$ tar xvf archive_name.tar

# View an existing tar archive
$ tar tvf archive_name.tar
```

### grep command examples
```
# Search for a given string in a file (case in-sensitive search).
$ grep -i "the" demo_file

# Print the matched line, along with the 3 lines after it.
$ grep -A 3 -i "example" demo_text

# Search for a given string in all files recursively
$ grep -r "ramesh" *
```

### find command examples
```
# Find files using file-name ( case in-sensitve find)
$ find -iname "MyCProgram.c"

# Execute commands on files found by the find command
$ find -iname "MyCProgram.c" -exec md5sum {} \;

# Find all empty files in home directory
$ find ~ -empty
```

### ssh command examples
```
# Login to remote host
ssh -l jsmith remotehost.example.com

# Debug ssh client
ssh -v -l jsmith remotehost.example.com

# Display ssh client version
$ ssh -V
OpenSSH_3.9p1, OpenSSL 0.9.7a Feb 19 2003
```

### vim command examples
```
# Go to the 143rd line of file
$ vim +143 filename.txt

# Go to the first match of the specified
$ vim +/search-term filename.txt

# Open the file in read only mode.
$ vim -R /etc/passwd
```

### ls command examples
```
# Display filesize in human readable format (e.g. KB, MB etc.,)
$ ls -lh
-rw-r----- 1 ramesh team-dev 8.9M Jun 12 15:27 arch-linux.txt.gz

# Order Files Based on Last Modified Time (In Reverse Order) Using ls -ltr
$ ls -ltr

# Visual Classification of Files With Special Characters Using ls -F
$ ls -F
```

### gzip command examples
```
# To create a *.gz compressed file:
$ gzip test.txt

# To uncompress a *.gz file:
$ gzip -d test.txt.gz

# Display compression ratio of the compressed file using gzip -l
$ gzip -l *.gz
         compressed        uncompressed  ratio uncompressed_name
              23709               97975  75.8% asp-patch-rpms.txt
```

### bzip2 command examples
```
# To create a *.bz2 compressed file:
$ bzip2 test.txt

# To uncompress a *.bz2 file:
bzip2 -d test.txt.bz2
```

### unzip command examples
```
# To extract a *.zip compressed file:
$ unzip test.zip

# View the contents of *.zip file (Without unzipping it):
$ unzip -l jasper.zip
Archive:  jasper.zip
  Length     Date   Time    Name
 --------    ----   ----    ----
    40995  11-30-98 23:50   META-INF/MANIFEST.MF
    32169  08-25-98 21:07   classes_
    15964  08-25-98 21:07   classes_names
    10542  08-25-98 21:07   classes_ncomp
```

### shutdown command examples
```
# Shutdown the system and turn the power off immediately.
$ shutdown -h now

# Shutdown the system after 10 minutes.
$ shutdown -h +10

# Reboot the system using shutdown command.
$ shutdown -r now

# Force the filesystem check during reboot.
$ shutdown -Fr now
```

### ps command examples
```
# ps command is used to display information about the processes that are running in the system.
# While there are lot of arguments that could be passed to a ps command, following are some of the common ones.
# To view current running processes.
$ ps -ef | more

# To view current running processes in a tree structure. H option stands for process hierarchy.
$ ps -efH | more
```

### rm command examples
```
# Get confirmation before removing the file.
$ rm -i filename.txt

# It is very useful while giving shell metacharacters in the file name argument.
# Print the filename and get confirmation before removing the file.
$ rm -i file*

# Following example recursively removes all files and directories under the example directory. This also removes the example directory itself.
$ rm -r example
```

### cp command examples
```
# Copy file1 to file2 preserving the mode, ownership and timestamp.
$ cp -p file1 file2

# Copy file1 to file2. if file2 exists prompt for confirmation before overwritting it.
$ cp -i file1 file2
```

### mv command examples
```
# Rename file1 to file2. if file2 exists prompt for confirmation before overwritting it.
$ mv -i file1 file2
Note: mv -f is just the opposite, which will overwrite file2 without prompting.

# mv -v will print what is happening during file rename, which is useful while specifying shell metacharacters in the file name argument.
$ mv -v file1 file2
```

### cat command examples
```
# You can view multiple files at the same time. Following example prints the content of file1 followed by file2 to stdout.
$ cat file1 file2

# While displaying the file, following cat -n command will prepend the line number to each line of the output.
$ cat -n /etc/logrotate.conf
    1	/var/log/btmp {
    2	    missingok
    3	    monthly
    4	    create 0660 root utmp
    5	    rotate 1
    6	}
```

### chmod command examples
```
# chmod command is used to change the permissions for a file or directory.
# Give full access to user and group (i.e read, write and execute ) on a specific file.
$ chmod ug+rwx file.txt

# Revoke all access for the group (i.e read, write and execute ) on a specific file.
$ chmod g-rwx file.txt

# Apply the file permissions recursively to all the files in the sub-directories.
$ chmod -R ug+rwx file.txt
```

### mkdir command examples
```
# Following example creates a directory called temp under your home directory.
$ mkdir ~/temp

# Create nested directories using one mkdir command. If any of these directories exist already, it will not display any error. If any of these directories doesn’t exist, it will create them.
$ mkdir -p dir1/dir2/dir3/dir4/
```

### ifconfig command examples
```
# Use ifconfig command to view or configure a network interface on the Linux system.
# View all the interfaces along with status.
$ ifconfig -a

# Start or stop a specific interface using up and down command as shown below.

$ ifconfig eth0 up
$ ifconfig eth0 down
```

### uname command examples
```
# Uname command displays important information about the system such as — Kernel name, Host name, Kernel release number, Processor type, etc.,
# Sample uname output from a Ubuntu laptop is shown below.

$ uname -a
Linux john-laptop 2.6.32-24-generic #41-Ubuntu SMP Thu Aug 19 01:12:52 UTC 2010 i686 GNU/Linux
```

### whatis command examples
```
# Whatis command displays a single line description about a command.
$ whatis ls
ls		(1)  - list directory contents

$ whatis ifconfig
ifconfig (8)         - configure a network interface
```
