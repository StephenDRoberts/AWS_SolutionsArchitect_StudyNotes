# Route53

The prerequisites for routing traffic to a website that is hosted in an S3 Bucket:

1. An S3 bucket that is configured to host a static website. The bucket must have the same nameas your domain or subdomain. For example, if you want to use the subdomain portal.tutorialsdojo.com, the name of the bucket must be portal.tutorialsdojo.com

2. A registered domain name. You can use Route 53 as your domain registrar, or you can use a different registrar.

3. Route 53 as the DNS service for the domain. If you register your domain name by using Route 53, we automatically configure Route 53 as the DNS service for the domain.

To route domain traffic to an ELB load balancer, use Amazon Route 53 to create an alias record that poinst to your load balancer. An alias record is a Route 53 extension to DNS. It's similar to a CNAME record, but you can create an alias recordd both for the root domain, such as tutorialsdojo.com, and for subdomains, such as portal.tutorialsdojo.com. (You can create CNAME records **only for subdomains**). To enable IPv6 resolution, you would need a second resource record, tutorialsdojo.com ALIAS AAAA -> myelb.us-west-2.elb.amazonaws.com, this is assuming your ELB has Ipv6 support.

You can create a new Route 53 with the failover option to a static S3 website bucket or CloudFront distribution as an alternative.
