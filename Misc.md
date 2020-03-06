# Miscellaneous

#### Finance

AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amoutn.

Cost Explorer allows you to visualize and manage your AWS costs and usages over time - not for budgetting.
In Cost Explorer you can view data for the last 13 months.

# Networking Misc

A *Route Origin Authorization (ROA)* is a document that you can create through your reginal internet registry (RIR) that contains the address range, the ASNs that are allowed to advertise the address rance, adn teh expiration date.

The ROA authorizes Amazon to advertise an address range under a specific AS number. However it does not authorize your AWS account to bring the address range to AWS.

An **Elastic Network Interface (ENI)** is a logical networking component in a VPC that represents a virtual network card. You can attach a network interface to an EC2 instance in the following ways:
* When it's running (hot attach)
* When it's stopped (warm attach)
* When the instance is being launched (cold attach)


#### CloudTrail

CloudTrail is the record of an activity in an AWS account. This activity can be an action taken by a user, role or service that is monitorable by CloudTrail. CloudTrail events provide a history of both API and non-API account activity made through the Mgt Console, SDKs, CLI and other AWS services.

there are two types of events that can be logged in CoudTrails:
1. management events
2. data events

By default, trails log management evens but *not* data events.

#### Ops Misc

**AWS OpsWorks** is a configuration management service the provides managed instances of Chef and Puppet. OpsWorks lets you use chef and Puppet to automate how servers are configured, deployed and managed across your EC2 instances or on-premises compute environments. OpsWorks has 3 offerings:
1. OpsWorks for Chef Automate
2. OpsWorks for Puppet Enterprise
3. OpsWorks Stacks

#### SWF

A decision task tells the decider the state of the workflow execution.  The decider can be viewed as a special type of worker. Like workers, it can be written in any language and asks Amazon SWF for tasks. However it handles special tasks called decision tasks.

Amazon SWF issues decision tasks whenever a workflow execution has transitions such as an activity task completing or timing out. A decision task contains information on the inuts, outputs, and current state of previously initiated activity tasks. Your decider uses this data to decide the next steps, including any new activity tasks and returns those to Amazon SWF. SWF in turn enacts these decisions, initiating new activity tasks where appropriate and monitoring them.

#### SSL

SNI Custom SLL relies on the SNI extension of the Transport Layer Security protocol, which allows multiple domains to serve SSL traffic over the same IP address by including the hostname which the viewers are trying to connect to.
