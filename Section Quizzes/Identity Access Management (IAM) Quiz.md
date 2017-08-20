# Question

**1. When using Web Identity Federation to allow a user to access an AWS service (such as an S3 bucket), which of the following is the correct order of step?**
- Users cannot use Facebook credentials to access the AWS platform.
- A user makes the AssumeRoleWithWebIdentity API Call. The user is then redirected to facebook to authenticate. Once authenticated, the user is given an ID token. The user is then granted temporary access to the AWS platform.
- A user authenticates with facebook first. They are then given an ID token by facebook. An API call, AssumeRoleWithWebIdentity, is then used in conjuction with the ID token. A user is then granted temporary security credentials.
- A user logs in to the AWS platform using their facebook credentials. AWS authenticate with facebook to check the credentials. Temporary Security Access is granted to AWS.

**2. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).**
- False
- True

**3. When authenticating using Web Identity Federation, which of the following is the API call used to obtain temporary security credentials?**
- AssumeRole
- GetRoleWithWebIdentity
- AssumeRoleWithWebIdentity
- GetRole

**4. The AWS sign-in endpoint for SAML is https://signin.aws.amazon.com/saml.**
- False
- True

**5. When using Active Directory to authenticate to AWS, which of the following answers contains the correct steps, in the correct order?*
- Federating with Active Directory is not possible with AWS.
- The user navigates to the AWS console. The user enter in their active directory single sign on credentials in to AWS. The user's web browser receives a SAML assertion from AWS. The user is then able to access the AWS Console.
- The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the AssumeRoleWithSAML API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.
- The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the GiveUserSAMLAccess API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.

**6. What is the name of the API call used to request temporary security credentials from the AWS platform when federating with Active Directory?**
- GetSAMLRole
- ShowMeTheSAML
- AssumeRoleWithSAML
- CovertRoleToSAML

**7. SAML stands for Security Assertion Markup Language.**
- True
- False

**8. Which statement best describes IAM?**
- IAM allows you to manage permissions for AWS resources only.
- IAM allows you to manage users' passwords only. AWS staff must create new users for your organisation. This is done by raising a ticket.
- IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.
- IAM stands for Improvised Application Management, and it allows you to deploy and manage applications in the AWS Cloud.

**9. Which of the following is NOT a feature of IAM?**
- Fine-grained access control to AWS resources
- Centralised control of your AWS account
- Allows you to setup biometric authentication, so that no passwords are required
- Integrates with existing active directory account allowing single sign on

**10. What is the name of the service that allows users to use their social media account to gain temporary access to the AWS platform?**
- Active Directory Authentication Services
- Facebook Sign In Service
- Web Identity Federation
- Web Confederation Services

# Answers

**1. When using Web Identity Federation to allow a user to access an AWS service (such as an S3 bucket), which of the following is the correct order of step?**
- Users cannot use Facebook credentials to access the AWS platform.
- A user makes the AssumeRoleWithWebIdentity API Call. The user is then redirected to facebook to authenticate. Once authenticated, the user is given an ID token. The user is then granted temporary access to the AWS platform.
- :white_check_mark: **`A user authenticates with facebook first. They are then given an ID token by facebook. An API call, AssumeRoleWithWebIdentity, is then used in conjuction with the ID token. A user is then granted temporary security credentials.``**
- A user logs in to the AWS platform using their facebook credentials. AWS authenticate with facebook to check the credentials. Temporary Security Access is granted to AWS.

**2. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).**
- :white_check_mark: **`False`**
- True

**3. When authenticating using Web Identity Federation, which of the following is the API call used to obtain temporary security credentials?**
- AssumeRole
- GetRoleWithWebIdentity
- :white_check_mark: **`AssumeRoleWithWebIdentity`**
- GetRole

**4. The AWS sign-in endpoint for SAML is https://signin.aws.amazon.com/saml.**
- False
- :white_check_mark: **`True`**

**5. When using Active Directory to authenticate to AWS, which of the following answers contains the correct steps, in the correct order?*
- Federating with Active Directory is not possible with AWS.
- The user navigates to the AWS console. The user enter in their active directory single sign on credentials in to AWS. The user's web browser receives a SAML assertion from AWS. The user is then able to access the AWS Console.
- :white_check_mark: **`The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the AssumeRoleWithSAML API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.`**
- The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the GiveUserSAMLAccess API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.

**6. What is the name of the API call used to request temporary security credentials from the AWS platform when federating with Active Directory?**
- GetSAMLRole
- ShowMeTheSAML
- :white_check_mark: **`AssumeRoleWithSAML`**
- CovertRoleToSAML

**7. SAML stands for Security Assertion Markup Language.**
- :white_check_mark: **`True`**
- False

**8. Which statement best describes IAM?**
- IAM allows you to manage permissions for AWS resources only.
- IAM allows you to manage users' passwords only. AWS staff must create new users for your organisation. This is done by raising a ticket.
- :white_check_mark: **`IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.`**
- IAM stands for Improvised Application Management, and it allows you to deploy and manage applications in the AWS Cloud.

**9. Which of the following is NOT a feature of IAM?**
- Fine-grained access control to AWS resources
- Centralised control of your AWS account
- :white_check_mark: **`Allows you to setup biometric authentication, so that no passwords are required`**
- Integrates with existing active directory account allowing single sign on

**10. What is the name of the service that allows users to use their social media account to gain temporary access to the AWS platform?**
- Active Directory Authentication Services
- Facebook Sign In Service
- :white_check_mark: **`Web Identity Federation`**
- Web Confederation Services
