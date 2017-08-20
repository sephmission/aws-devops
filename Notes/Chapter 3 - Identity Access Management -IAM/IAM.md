# Security Token Service (STS)
Grants users limited and temporary access to AWS resources. Users can come from three sources:

- **Federation (typically Active Directory)**
-- Uses Security Assertion Markup Language (SAML)
-- Grants temporary access based off the users Active Directory credentials. Does not need to be a user in IAM
-- Single sign on (SSO) allows users to log in to AWS console without assigning IAM credentials
- **Federation with Mobile Apps**
-- Use Facebook/Amazon/Google or other OpenID providers to log in.
- **Cross Account Access**
-- Let's users from one AWS account resources in another

## Understanding Key Terms
- **Federation**: combining or joining a list of users in one domain (such as IAM) with a list of users in another domain (such as Active Directory, Facebook, etc)
- **Identity Broker**: a service that allows you to take an identity from point A and join it (federate it) to point B
- **Identity Store**: Services like Active Directory, Facebook, Google, etc
- **Identities**: a user of a service like Facebook, etc

## What we have learnt so far?
- IAM is universal. It does not apply to regions at this time.
- The "root account" is simple the account created when first setup your AWS account. It has complete Admin access.
- New Users have NO permissions when first created.
- New Users are assigned **Access Key ID & Secret Access Keys** when first created.
- These are not the same as a password, and you cannot use the Access Key ID & Secret Access Key to Login in to the console. You can use this to access AWS via the APIs and Command Line however.
- You only get to view these once. If you lose them, you have to regenerate them. So save them in a secure location.
- Always setup Multifactor Authentication on your root account.
- You can create and customise your own password rotation policies.
