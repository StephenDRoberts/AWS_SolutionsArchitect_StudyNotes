# Security

#### Encryption

You can secure the privacy of your data in AWS, both at rest and in-transit, through encryption. If your data is stored in EBS volumes you can enable EBS encryption and if it is stored on Amazon S3, you can enable client-side and server-side encryption.

**Client-side Encryption**

Client-side encryption is the act of encrypting data before sending it to Amazon S3. To enable client-side encryption, you have the following options:

* Use an AWS KMS-managed master key
* Use a client-side master key

When using KMS, a KMS cusotmer master key ID (CMK ID) is sent to AWS.
When using a client-side master key, your client-side master keys and your unencrypted data are never sent to AWS.

**Server-side Encryption**

You have 3 options for managing encryption keys:
1. Use Amazon S3-Managed Keys (SSE-S3)
2. Use AWS KMS-Managed Keys (SSE-KMS)
3. Use Customer-Provided Keys (SSE-C)

Server-side encryption only provides AES-256.

---

All data transferred between any type of gateway applicance and AWS storage is encrypted using SSL. By default, all data stored by AWS Storage Gateway in S3 is encrypted server-side with Amazon S3-Managed Encryption Keys (SSE-S3). Also, when using the file gateway, you can optionally configure each file share to have your objects encrypted with AWS KMS-Managed Keys using SSE-KMS.

*(**NB:** AWS Storage Gateway connects an on-premises software applicance with cloud-based storage to provide seamless integration with data security features between your on-premises IT environment and the AWS storage infrastructure.*

Data stored in **Amazon Glacier** is protected by default; only vault owners have access to the Amazon Glacier resources they creates. Amazon Glacier encrypts your data at rest by default and supports secure data transit with SSL.
