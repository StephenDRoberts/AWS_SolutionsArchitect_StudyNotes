# Miscellaneous

#### Finance

AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amoutn.

Cost Explorer allows you to visualize and manage your AWS costs and usages over time - not for budgetting.
In Cost Explorer you can view data for the last 13 months.

# Networking Misc

A *Route Origin Authorization (ROA)* is a document that you can create through your reginal internet registry (RIR) that contains the address range, the ASNs that are allowed to advertise the address rance, adn teh expiration date.

The ROA authorizes Amazon to advertise an address range under a specific AS number. However it does not authorize your AWS account to bring the address range to AWS.

#### CloudTrail

CloudTrail is the record of an activity in an AWS account. This activity can be an action taken by a user, role or service that is monitorable by CloudTrail. CloudTrail events provide a history of both API and non-API account activity made through the Mgt Console, SDKs, CLI and other AWS services.

there are two types of events that can be logged in CoudTrails:
1. management events
2. data events

By default, trails log management evens but *not* data events.
