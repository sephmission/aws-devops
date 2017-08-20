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
