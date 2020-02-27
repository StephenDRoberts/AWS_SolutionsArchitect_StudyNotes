# Security

#### Encryption

You can secure the privacy of your data in AWS, both at rest and in-transit, through encryption. If your data is stored in EBS volumes you can enable EBS encryption and if it is stored on Amazon S3, you can enable client-side and server-side encryption.

Client-side encryption is the act of encrypting data before sending it to Amazon S3. To enable client-side encryption, you have the following options:

* Use an AWS KMS-managed master key
* Use a client-side master key

When using KMS, a KMS cusotmer master key ID (CMK ID) is sent to AWS.
When using a client-side master key, your client-side master keys and your unencrypted data are never sent to AWS.

