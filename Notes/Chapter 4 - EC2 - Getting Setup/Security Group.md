# Security Group
* All Inbound Traffic is Blocked by Default
* All Outbound Traffic is Allowed
* Changes to Security Groups take effect immediately
* You can have any number of EC2 instances within a security group.
* You can have multiple security groups attached to EC2 Instances
* Security Groups are **STATEFUL**.
  * If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again.
* You cannot block specific IP Address using Security Groups, instead use Network Access Control Lists.
* You can specify allow rules, but not deny rules.
