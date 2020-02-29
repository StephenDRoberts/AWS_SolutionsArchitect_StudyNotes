# Lambda

AWS Lambda supports synchronous and asynchronous invocation of a Lambda function. You can control the invocation type only when you invoke a Lambda function. When you use an AWS service as a trigger, the invocation type is predetermined for each service. You have no control over the invocation type that these event sources use when they invoke your Lambda function. 

#### Security

When you create or update Lambda functions that use environment variables, AWS Lambda encrypts them using the AWS KMS. When your function is invoked, those values are decrypted and made available to the lambda code.

The first time you create or update Lambda functions that use env variables in a region, a defual service key is created for you automatically within AWS KMS. This key is used to encrypt env variables.

However, if you wish to use encryption helpers and use KMS to encrypt env variables ***after your Lambda function is created***, you must create your own AWS KMS key and choose it instead of the default key. 

Creating your own key gives you more flexibility, including the ability to create, rotate, disable, and define access controls, and to audit the encryption keys used to protect your data.
