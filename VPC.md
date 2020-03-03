# Virtual Private Clouds (VPCs)

Security Groups usually control the list of ports that are allowed to be used by your EC2 instances and the NACLs control which network or list of IP addresses can connect to your whole VPC.

#### Security Groups

Act as a virtual firewall for your instance to control inbound and outbound traffic.
You can assign up to five security groups to the instance.
Security groups act at an ***instance level***, not the subnet level. Therefore, each instance in a subnet in your VPC could be assinged to a different set of security groups. If you don't specify a particular group at launch time, the instance is automatically assigned to the default security group of the VPC. 

Security groups are **stateful** -> return traffic is automatically allowed, regardless of any rules.

By default , Security Groups do not allow incoming traffic - a rule will need to be setup to allow inbound traffic. However, Security Groups allow all outbound traffic by default.

#### NACLs

To control the traffic in and out of your VPC network, you can use the Network Access Controls List.

It is an optional layer of security for your VPC and acts as a firewall for controlling traffic in and out of one or more subnets. You might set up a network ACL with rules similar to your security groups in order to add an additional layer of security to your VPC.

NACLs are **stateless** -> return traffic must be explicitly allowed by rules.

Network ACL Rules are evaluated by rule number, from lowest to highest, and executed immediately when a matching allow/deny rule is found.

By default NACLs allow **all** inbound and outbound IPv4 traffic.

#### Peering

A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, with a VPC in another AWS account, or with a VPC in a different Region.

AWS uses the existing infrastructure of a VPC to create a VPC peering connection; it is neither a gateway nor a VPN connection and does not rely on a separate piece of physical hardware. There is no single point of failure for communciation or a bandwith bottleneck.
