# CloudWatch

CloudWatch is a monitoring and management service that provides data and actionable insights for AWS, hybrid, and on-premise applications and infrastructure resource. You can collect and access all your performance and operational data in the form of logs and metrics from a single platform.

CloudWatch covers metrics like CPU Utilization, Network Utilization and Disk Reads. 
However, it does not cover things like memory utilization, disk space utilization and many others which can be collected by setting up a custom metric.

Custom metrics can be set up using CloudWatch Monitoring Scripts which is written in Perl.

You can also install CloudWatch Agent to collect more system-level metrics from EC2 instances.

Custom metrics than can be set up:
* Memory utilization
* Disk swap utilization
* Disk space utilization
* Page file utilization
* Log collection

#### CloudWatch & Lambda

AWS Lambda automatically monitors functions on your behalf, reporting metrics through Amazon CloudWatch. These metrics include total invocation request, latency, and error rates. The throttles, Dead Letter Queues errors and Iterator age for stream-based invocations are also monitored.

You can monitor metrics for lambda and view logs by using the Lambda console, the CloudWatch console, the AWS CLI, or the CloudWatch API.
