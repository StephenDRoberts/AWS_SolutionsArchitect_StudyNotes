# Authentication, Authorisation & IAM

#### IAM

**Groups** let you specify permissions for multiple users, which can make it easier to manage the permissions for those users.

**Identity providers** manage your user identities outside of AWS and give these external user identities permission to use AWS resources in your account. You can manage identity providers using IAM dashboard instead of creating IAM users in your AWS account.

Always remember that you should associate IAM roles to EC2 instances and ***not*** an IAM User.

#### Active Directory

If a company uses Microsoft Active Directory, this implmements Security Assertion Markup Lianguage (SAML). Therefore, you can set up a SAML-based Federation for API access to your AWS cloud for users utilising Active Directory. Users can connect to AWS using the login credentials of your on-premise network.

SAML enabled federated single sign-on (SSO) so users can log into the Mgt Console or call the AWS APIs without you having to create an IAM user for everyone in your organisation. 

If a company is using Active Directory, it is best to use the AWS Directory SErvice AD Connectory for easier integration.

You can assign an IAM Role to the users or groups from your Active Directory once it is integrated with your VPC via the AWS Directory Service AD Connector.

AWS Directory SErvice provides multipl ways to use Amazon Cloud Directory and Microsoft Active Directory (AD) with other AWS services. Directories store information about users, groups and devices, and administrators use them to manage access to information and resources. AWS Directory Services provides multiple directory choices for customers who want to use existing Microsoft AD or Lightweight Directory Access Protocol (LDAP)-aware application int he cloud. It also offeres those same choices to developers who need a directory to manage users, groups, devices and access.

#### Web Identity Federation

Web Indentity Federation allows users to sign in via well-known external identity providers such as Amazon, Facebook or Google. It does not utilize Active Directory.

#### Temporary Credentials

Temporary credentials are useful in scenarios that involve identity federation, delegation, cross-account access and IAM roles.

In an enterprise identity federation, you can authenticate users in your organizations network, and then provide those users access to AWS without creating new AWS identities for them and requiring them to sign in with a separate user name and password. This is known as the single sign-on (SSO) approach to temporary access. AWS STS supports open standards like SAML 2.0, with which you can use Microsoft Active Directory Federated Services to leverage your Microsoft AD. You can also use SAML 2.0 to manage your own solution for federating user identities.

You can use **Cognito** to deliver temporary, limited-privilege credentials to your application so that your users can access AWS resources. Amazon Cognito Identity Pools support both authenticated and unauthenticated identities. You can retrieve a unique Cognito identifier (**Identity ID**) for your end user immediately if you're allowing unauthenticated users or after you've set the login tokens in the credentials provider if you're authenticating users.

