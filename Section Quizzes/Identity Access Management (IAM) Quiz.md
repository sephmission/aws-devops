# Questions

**1. When using Web Identity Federation to allow a user to access an AWS service (such as an S3 bucket), which of the following is the correct order of step?**

    a. Users cannot use Facebook credentials to access the AWS platform.
    b. A user makes the AssumeRoleWithWebIdentity API Call. The user is then redirected to facebook to authenticate. Once authenticated, the user is given an ID token. The user is then granted temporary access to the AWS platform.
    c. A user authenticates with facebook first. They are then given an ID token by facebook. An API call, AssumeRoleWithWebIdentity, is then used in conjuction with the ID token. A user is then granted temporary security credentials.
    d. A user logs in to the AWS platform using their facebook credentials. AWS authenticate with facebook to check the credentials. Temporary Security Access is granted to AWS.

**2. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).**

    a. False
    b. True

**3. When authenticating using Web Identity Federation, which of the following is the API call used to obtain temporary security credentials?**

    a. AssumeRole
    b. GetRoleWithWebIdentity
    c. AssumeRoleWithWebIdentity
    d. GetRole

**4. The AWS sign-in endpoint for SAML is https://signin.aws.amazon.com/saml.**

    a. False
    b. True

**5. When using Active Directory to authenticate to AWS, which of the following answers contains the correct steps, in the correct order?**

    a. Federating with Active Directory is not possible with AWS.
    b. The user navigates to the AWS console. The user enter in their active directory single sign on credentials in to AWS. The user's web browser receives a SAML assertion from AWS. The user is then able to access the AWS Console.
    c. The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the AssumeRoleWithSAML API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.
    d. The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the GiveUserSAMLAccess API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.

**6. What is the name of the API call used to request temporary security credentials from the AWS platform when federating with Active Directory?**

    a. GetSAMLRole
    b. ShowMeTheSAML
    c. AssumeRoleWithSAML
    d. CovertRoleToSAML

**7. SAML stands for Security Assertion Markup Language.**

    a. True
    b. False

**8. Which statement best describes IAM?**

    a. IAM allows you to manage permissions for AWS resources only.
    b. IAM allows you to manage users' passwords only. AWS staff must create new users for your organisation. This is done by raising a ticket.
    c. IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.
    d. IAM stands for Improvised Application Management, and it allows you to deploy and manage applications in the AWS Cloud.

**9. Which of the following is NOT a feature of IAM?**

    a. Fine-grained access control to AWS resources
    b. Centralised control of your AWS account
    c. Allows you to setup biometric authentication, so that no passwords are required
    d. Integrates with existing active directory account allowing single sign on

**10. What is the name of the service that allows users to use their social media account to gain temporary access to the AWS platform?**

    a. Active Directory Authentication Services
    b. Facebook Sign In Service
    c. Web Identity Federation
    d. Web Confederation Services

# Answers

**1. When using Web Identity Federation to allow a user to access an AWS service (such as an S3 bucket), which of the following is the correct order of step?**

    Correct Answer: 
    A user authenticates with facebook first. They are then given an ID token by facebook. An API call, AssumeRoleWithWebIdentity, is then used in conjuction with the ID token. A user is then granted temporary security credentials.

**2. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).**

    Correct Answer: 
    False

**3. When authenticating using Web Identity Federation, which of the following is the API call used to obtain temporary security credentials?**

    Correct Answer: 
    AssumeRoleWithWebIdentity

**4. The AWS sign-in endpoint for SAML is https://signin.aws.amazon.com/saml.**

    Correct Answer: 
    True

**5. When using Active Directory to authenticate to AWS, which of the following answers contains the correct steps, in the correct order?**

    Correct Answer: 
    The user navigates to ADFS webserver. The user enter in their single sign on credentials. The user's web browser receives a SAML assertion from the AD server. The user's browser then posts the SAML assertion to the AWS SAML end point for SAML and the AssumeRoleWithSAML API request is used to request temporary security credentials. 5) The user is then able to access the AWS Console.

**6. What is the name of the API call used to request temporary security credentials from the AWS platform when federating with Active Directory?**

    Correct Answer: 
    AssumeRoleWithSAML

**7. SAML stands for Security Assertion Markup Language.**

    Correct Answer: 
    True

**8. Which statement best describes IAM?**

    Correct Answer: 
    IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.

**9. Which of the following is NOT a feature of IAM?**

    Correct Answer: 
    Allows you to setup biometric authentication, so that no passwords are required.

**10. What is the name of the service that allows users to use their social media account to gain temporary access to the AWS platform?**

    Correct Answer: 
    Web Identity Federation
