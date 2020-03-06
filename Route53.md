# Route53

The prerequisites for routing traffic to a website that is hosted in an S3 Bucket:

1. An S3 bucket that is configured to host a static website. The bucket must have the same nameas your domain or subdomain. For example, if you want to use the subdomain portal.tutorialsdojo.com, the name of the bucket must be portal.tutorialsdojo.com

2. A registered domain name. You can use Route 53 as your domain registrar, or you can use a different registrar.

3. Route 53 as the DNS service for the domain. If you register your domain name by using Route 53, we automatically configure Route 53 as the DNS service for the domain.

To route domain traffic to an ELB load balancer, use Amazon Route 53 to create an alias record that poinst to your load balancer. An alias record is a Route 53 extension to DNS. It's similar to a CNAME record, but you can create an alias recordd both for the root domain, such as tutorialsdojo.com, and for subdomains, such as portal.tutorialsdojo.com. (You can create CNAME records **only for subdomains**). To enable IPv6 resolution, you would need a second resource record, tutorialsdojo.com ALIAS AAAA -> myelb.us-west-2.elb.amazonaws.com, this is assuming your ELB has Ipv6 support.

You can create a new Route 53 with the failover option to a static S3 website bucket or CloudFront distribution as an alternative.

You can use Route 53 health checking to configure active-active and active-passive failover configurations. You configure active-active failover using any routing policy (or combination of routing policies) other than failover, and you configure active-passive failover using the failover routing policy.

#### Active-Active Failover

Use this failover configuration when you want all of your resources to be available the majority of the time. When a resource becomes unavailable, Route 52 can detect that it's unhealthy and stop including it when responding to queries.

In active-active failover, all the records that have the same name, same type (such as A or AAAA), and the same routing policy (such as weighted or latency) are active unless Route 53 considers them unhealthy. Route 53 can respond to a DNS query using any healthy record.

#### Active-Passive Failover

Use an active-passive failover configuration when you want a primary resource or group of resources to be available the majority of the time and you want a secondary resource or group of resources to be on standby in case all the primary resources become unavailable. When responding to queries, Route 53 includes only the healthy primary resources. If all the primary resources are unhealthy, Route 53 begins to includee only the healthy secondary resources in response to DNS queries.
