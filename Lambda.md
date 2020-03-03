# Lambda

AWS Lambda supports synchronous and asynchronous invocation of a Lambda function. You can control the invocation type only when you invoke a Lambda function. When you use an AWS service as a trigger, the invocation type is predetermined for each service. You have no control over the invocation type that these event sources use when they invoke your Lambda function. 

#### Security

When you create or update Lambda functions that use environment variables, AWS Lambda encrypts them using the AWS KMS. When your function is invoked, those values are decrypted and made available to the lambda code.

The first time you create or update Lambda functions that use env variables in a region, a defual service key is created for you automatically within AWS KMS. This key is used to encrypt env variables.

However, if you wish to use encryption helpers and use KMS to encrypt env variables ***after your Lambda function is created***, you must create your own AWS KMS key and choose it instead of the default key. 

Creating your own key gives you more flexibility, including the ability to create, rotate, disable, and define access controls, and to audit the encryption keys used to protect your data.

#### Deployment Configurations

You must choose one of the following deployment configration types to specify how traffic is shifted from the original AWS Lambda function version to the new AWS Lambda function version:

1. **Canary** - Traffic is shifted in two increments. You can choose from predefined canary options that specify the percentage of traffic shifted to your updated Lambda function version in the 1st increment and the interval, in minutes, before the remaining traffic is shifted in the 2nd increment.

2. **Linear** - Traffic is shifted in equal increments with an equal number of minutes between each increment.

3. **All-at-once**

 #### CloudWatch & Lambda
 
 AWS Lambda automatically monitors functions on your behalf, reporting metrics through Amazon CloudWatch. Thes metrics include total invocation request, latency, and error rates. The throttles, Dead Letter Queues errors an d Iterator age for stream-based invocations are also monitored. You can monitor metrics for lambda and view logs by using the Lambda console, the CloudWatch console, the AWS CLI, or the CloudWatch API.
