# EC2 Lab
Create a webpage using CLI

Create a new instance in EC2 then login (use `ec2-user`) via SSH then run the following commands:

```
sudo su
yum update -y
yum install httpd -y
cd /var/www/html
nano index.html
service httpd start
```

Go the public URL of the instance to see the created file, index.html.
