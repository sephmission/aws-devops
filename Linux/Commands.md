# Most Frequently Used UNIX / Linux Commands (With Examples)
Reference: [http://www.thegeekstuff.com/2010/11/50-linux-commands/?utm_source=feedburner](http://www.thegeekstuff.com/2010/11/50-linux-commands/?utm_source=feedburner)

### Tar command examples
```
# Create a new tar archive
$ tar cvf archive_name.tar dirname/

# Extract from an existing tar archive.
$ tar xvf archive_name.tar

# View an existing tar archive
$ tar tvf archive_name.tar
```
[The Ultimate Tar Command Tutorial with 10 Practical Examples](http://www.thegeekstuff.com/2010/04/unix-tar-command-examples/)

### grep command examples
```
# Search for a given string in a file (case in-sensitive search).
$ grep -i "the" demo_file

# Print the matched line, along with the 3 lines after it.
$ grep -A 3 -i "example" demo_text

# Search for a given string in all files recursively
$ grep -r "ramesh" *
```
[Get a Grip on the Grep! – 15 Practical Grep Command Examples](http://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)

### find command examples
```
# Find files using file-name ( case in-sensitve find)
$ find -iname "MyCProgram.c"

# Execute commands on files found by the find command
$ find -iname "MyCProgram.c" -exec md5sum {} \;

# Find all empty files in home directory
$ find ~ -empty
```
[Mommy, I found it! — 15 Practical Linux Find Command Examples](http://www.thegeekstuff.com/2009/03/15-practical-linux-find-command-examples/)

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
[http://www.thegeekstuff.com/2008/05/5-basic-linux-ssh-client-commands/](http://www.thegeekstuff.com/2008/05/5-basic-linux-ssh-client-commands/)

### vim command examples
```
# Go to the 143rd line of file
$ vim +143 filename.txt

# Go to the first match of the specified
$ vim +/search-term filename.txt

# Open the file in read only mode.
$ vim -R /etc/passwd
```

### awk command examples
```
# Remove duplicate lines using awk
$ awk '!($0 in array) { array[$0]; print }' temp

# Print all lines from /etc/passwd that has the same uid and gid
$awk -F ':' '$3==$4' passwd.txt

# Print only specific field from a file.
$ awk '{print $2,$5;}' employee.txt
```
[8 Powerful Awk Built-in Variables – FS, OFS, RS, ORS, NR, NF, FILENAME, FNR](http://www.thegeekstuff.com/2010/01/8-powerful-awk-built-in-variables-fs-ofs-rs-ors-nr-nf-filename-fnr/)

### vim command examples
```
# Go to the 143rd line of file
$ vim +143 filename.txt

# Go to the first match of the specified
$ vim +/search-term filename.txt

# Open the file in read only mode.
$ vim -R /etc/passwd
```
[How To Record and Play in Vim Editor](http://www.thegeekstuff.com/2009/01/vi-and-vim-macro-tutorial-how-to-record-and-play/)

### diff command examples
```
# Ignore white space while comparing.
diff -w name_list.txt name_list_new.txt

2c2,3
< John Doe --- > John M Doe
> Jason Bourne
```
[Top 4 File Difference Tools on UNIX / Linux – Diff, Colordiff, Wdiff, Vimdiff](http://www.thegeekstuff.com/2010/06/linux-file-diff-utilities/)

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
[Unix LS Command: 15 Practical Examples](http://www.thegeekstuff.com/2009/07/linux-ls-command-examples/)

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
[BZ is Eazy! bzip2, bzgrep, bzcmp, bzdiff, bzcat, bzless, bzmore examples](http://www.thegeekstuff.com/2010/10/bzcommand-examples/)

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

### ftp command examples
```
# Both ftp and secure ftp (sftp) has similar commands. To connect to a remote server and download multiple files, do the following.
$ ftp IP/hostname
ftp> mget *.html

# To view the file names located on the remote server before downloading, mls ftp command as shown below.
ftp> mls *.html -
/ftptest/features.html
/ftptest/index.html
/ftptest/othertools.html
/ftptest/samplereport.html
/ftptest/usage.html
```
[FTP and SFTP Beginners Guide with 10 Examples](http://www.thegeekstuff.com/2010/06/ftp-sftp-tutorial/)

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

### kill command examples
```
# Use kill command to terminate a process. First get the process id using ps -ef command, then use kill -9 to kill the running Linux process as shown below. You can also use killall, pkill, xkill to terminate a unix process.
$ ps -ef | grep vim
ramesh    7243  7222  9 22:43 pts/2    00:00:00 vim

$ kill -9 7243
```
[4 Ways to Kill a Process – kill, killall, pkill, xkill](http://www.thegeekstuff.com/2009/12/4-ways-to-kill-a-process-kill-killall-pkill-xkill/)

### top command examples
```
# top command displays the top processes in the system ( by default sorted by cpu usage ). To sort top output by any column, Press O (upper-case O) , which will display all the possible columns that you can sort by as shown below.

Current Sort Field:  P  for window 1:Def
Select sort field via field letter, type any other key to return

  a: PID        = Process Id              v: nDRT       = Dirty Pages count
  d: UID        = User Id                 y: WCHAN      = Sleeping in Function
  e: USER       = User Name               z: Flags      = Task Flags
  ........

# To displays only the processes that belong to a particular user use -u option. The following will show only the top processes that belongs to oracle user.

$ top -u oracle
```
[Can You Top This? 15 Practical Linux Top Command Examples](http://www.thegeekstuff.com/2010/01/15-practical-unix-linux-top-command-examples/)

### crontab command examples
```
# View crontab entry for a specific user
crontab -u john -l

# Schedule a cron job every 10 minutes.
*/10 * * * * /home/ramesh/check-disk-space
```
[Linux Crontab: 15 Awesome Cron Job Examples](http://www.thegeekstuff.com/2009/06/15-practical-crontab-examples/)

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
[7 Chmod Command Examples for Beginners](http://www.thegeekstuff.com/2010/06/chmod-command-examples/)

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
[Ifconfig: 7 Examples To Configure Network Interface](http://www.thegeekstuff.com/2009/03/ifconfig-7-examples-to-configure-network-interface/)

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

### locate command examples
```
# Using locate command you can quickly search for the location of a specific file (or group of files). Locate command uses the database created by updatedb. The example below shows all files in the system that contains the word crontab in it.

$ locate crontab
/etc/anacrontab
/etc/crontab
/usr/bin/crontab
/usr/share/doc/cron/examples/crontab2english.pl.gz
/usr/share/man/man1/crontab.1.gz
/usr/share/man/man5/anacrontab.5.gz
/usr/share/man/man5/crontab.5.gz
/usr/share/vim/vim72/syntax/crontab.vim
```

### man command examples
```
# Display the man page of a specific command.
$ man crontab

# When a man page for a command is located under more than one section, you can view the man page for that command from a specific section as shown below.
$ man SECTION-NUMBER commandname

# Following 8 sections are available in the man page.
# 1. General commands
# 2. System calls
# 3. C library functions
# 4. Special files (usually devices, those found in /dev) and drivers
# 5. File formats and conventions
# 6. Games and screensavers
# 7. Micellaneous
# 8. System administration commands and daemons

# For example, when you do whatis crontab, you’ll notice that crontab has two man pages (section 1 and section 5). To view section 5 of crontab man page, do the following.

$ whatis crontab
crontab (1)          - maintain crontab files for individual users (V3)
crontab (5)          - tables for driving cron

$ man 5 crontab
```

###  less command examples
```
# less is very efficient while viewing huge log files, as it doesn’t need to load the full file while opening.
$ less huge-log-file.log

# One you open a file using less command, following two keys are very helpful.
# CTRL+F – forward one window
# CTRL+B – backward one window
```
[Unix Less Command: 10 Tips for Effective Navigation](http://www.thegeekstuff.com/2010/02/unix-less-command-10-tips-for-effective-navigation/)

### su command examples
```
# Switch to a different user account using su command. Super user can switch to any other user without entering their password.
$ su - USERNAME

# Execute a single command from a different account name. In the following example, john can execute the ls command as raj username. Once the command is executed, it will come back to john’s account.
[john@dev-server]$ su - raj -c 'ls'
[john@dev-server]$

#Login to a specified user account, and execute the specified shell instead of the default shell.
$ su -s 'SHELLNAME' USERNAME
```

### mysql command examples
```
# mysql is probably the most widely used open source database on Linux. Even if you don’t run a mysql database on your server, you might end-up using the mysql command ( client ) to connect to a mysql database running on the remote server.
# To connect to a remote mysql database. This will prompt for a password.
$ mysql -u root -p -h 192.168.1.2

# To connect to a local mysql database.
$ mysql -u root -p

# If you want to specify the mysql root password in the command line itself, enter it immediately after -p (without any space).
```

### yum command examples
```
# To install apache using yum.
$ yum install httpd

# To upgrade apache using yum.
$ yum update httpd

# To uninstall/remove apache using yum.
$ yum remove httpd
```

### ping command examples
```
# Ping a remote host by sending only 5 packets.

$ ping -c 5 gmail.com
$ yum remove httpd
```
[Ping Tutorial: 15 Effective Ping Command Examples](http://www.thegeekstuff.com/2009/11/ping-tutorial-13-effective-ping-command-examples/)

### date command examples
```
# Set the system date:
$ date -s "01/31/2010 23:59:53"

# Once you’ve changed the system date, you should syncronize the hardware clock with the system date as shown below.
$ hwclock –systohc
$ hwclock --systohc –utc
```

### wget command examples
```
# The quick and effective method to download software, music, video from internet is using wget command.
$ wget http://prdownloads.sourceforge.net/sourceforge/nagios/nagios-3.2.1.tar.gz

# Download and store it with a different name.
$ wget -O taglist.zip http://www.vim.org/scripts/download_script.php?src_id=7701
```
[The Ultimate Wget Download Guide With 15 Awesome Examples](http://www.thegeekstuff.com/2009/09/the-ultimate-wget-download-guide-with-15-awesome-examples/)
