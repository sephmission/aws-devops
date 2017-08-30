# CLI commands for the Developer Exam

**1. Create a new Role in IAM**
   - Set Role Name: **MyEC2Role**
   - Select Role Type: **Amazon EC2**
   - Attach Policy: **AdministratorAccess**
   
**2. Create a new EC2 instance**
   - Launch and access the instance in SSH
   
**3. Set the following**

```
aws configure
AWS Access Key ID [None]: skip
AWS Secret Accsess Key [None]: skip
Default region name [None]: ap-southeast-1
Default output format [None]: skip
```

## Important AWS Commands in the exam

   - **How to describe instances?** 
   
   ```
   describe-instances
   ```
   
   - **How to describe instances that available to us?** 
   
   ```
   describe-images
   ```
   
   - **Create an instance?** 
   
   ```
   aws ec2 run-instances --image-id ami-abc12345 --count 1 --instance-type t2.micro --key-name MyKeyPair --security-group-ids sg-903004f8 --subnet-id subnet-6e7f829e
   ```
   
   - **Check available images?** 
   
   ```
   describe-images` or `aws ec2 describe-images --owners amazon --filters "Name=platform,Values=windows" "Name=root-device-type,Values=ebs"
   ```
   
   - **Terminate an instance?** 
   
   ```
   aws ec2 terminate-instances --instance-ids [instance id]
   ```

## Exam Tips
* Use
  * AWS EC2 DESCRIBE-INSTANCES
  * AWS EC2 DESCRIBE-IMAGES
  * AWS EC2 RUN-INSTANCES
* Do not confuse START-INSTANCES with RUN-INSTANCES


> Reference: [AWS EC2 Available Commands](https://docs.aws.amazon.com/cli/latest/reference/ec2/index.html)
