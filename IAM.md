
Identity and Access Managment is one of the top services used by AWS clients.

IAM allows you to manage users and their level of acces to the AWS Console. It is important to understand IAM and how it works since it's a very popular and crucial service for all organizations to know to to use.


Features: 

- centralized control of your AWS account
- shared access to your AWS account
- Granular permissions
- ID Federation (Linkedin, Facebook, Active Directory, etc)
- MFA
- Provide temporary access for users/devices and services where made necessary
- Allows you set up your own password rotation policy

IAM Manages:

-users
-Groups
-Roles
-Policies
 By default any user you create in an AWS account has NO permisisons and policies attached.
 
 - All permission policies have an "implicit deny" - no allows= Implicit Deny
 - DENY always overrides any ALLOW
 
 For all users(except the root user), permissions must grant access to AWS services ( this is done through IAM policies)
 - IAM provides ID services - but also coordinates with STS(Security Token Services) allow ID Federation (the use of external IDS)
