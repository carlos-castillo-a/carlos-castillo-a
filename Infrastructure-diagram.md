# AWS Organizations
To start off, my AWS environments are split between a management account, and two lower accounts (dev and prod). This is similar to many real organizations that follow best practice to split environments based on needs. For my purposes, I have simplified the number or environments compared to an enterprise company.

![](2022-03-25-22-45-36.png)

# Access Management
To secure my AWS environment, I have created my identites using Azure Active Directory. These identities each have access to AWS via an Enterprise Application configured to work with AWS SSO. Each user has been given specific permissions with Permission Set policies ensuring granular access.

This diagram is fairly basic and glosses over the way the permissions are distributed to child accounts and how the users are pushed from AAD to AWS. Regardless, it is a good representation of the architecture.

![](2022-03-25-22-37-05.png)

This setup ensures that root access will not be needed unless necessary and secures the access of AWS by using SAML based SSO. In many cloud based companies, user idenities are created in AD or AAD so this shows proper setup and management of access.