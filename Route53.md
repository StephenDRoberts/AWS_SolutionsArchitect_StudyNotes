# Route53

The prerequisites for routing traffic to a website that is hosted in an S3 Bucket:

1. An S3 bucket that is configured to host a static website. The bucket must have the same nameas your domain or subdomain. For example, if you want to use the subdomain portal.tutorialsdojo.com, the name of the bucket must be portal.tutorialsdojo.com

2. A registered domain name. You can use Route 53 as your domain registrar, or you can use a different registrar.

3. Route 53 as the DNS service for the domain. If you register your domain name by using Route 53, we automatically configure Route 53 as the DNS service for the domain.
