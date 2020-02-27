# Redshift

When you create a parameter group, the default workload management (WLM) configuration contians one queue that can run up to five queries concurrently. You can add additional queues and configure WLM properties in each of them if you want more control over query processing. Each queue that you add has the same default WLM configuration until you configure its properties. When you add additional queues, the last queue in the configuration is the default queue. Unless a query is routed to another queue based on criteria in the WLM configuration, it is processed by the default queue. You cannot specify user groups or query groups for the default queue.

As with other parameters, you cannot modify the WLM configuration in the default parameter group. Clusters associatied with the default parameter group alwaus use the default WLM configuration. If you want to modify the WLM configuration, you must create a parameter group and then associate that parameter group with any clusters that rquire your custom WLM configuration.

#### Enhanced VPC Routing

Amazon Redshift Enhanced VPC Routing forces all COP and UNLOAD traffic between your cluster and your data repositories through your Amazon VPC.
By using Enhanced VPC Routing, you can use standard VPC features such as VPC security groups, NACLs, VPC endpoints, VPC endoint policies, internet gateways, and DNS servers.
You use these features to tightly manage the flow of data between your Amazon Redshift cluster and other resources.
