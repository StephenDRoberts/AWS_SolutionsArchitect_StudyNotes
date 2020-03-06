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

#### VPN

An Amazon VPC offers you the flexibility to fully manage both sides of your Amazon VPC connectivity by creating a VPN connection between your remote network and a software VPN appliance running in your Amazon VPC network. This option is recommended if you must manage both ends of the VPN connection either for compliance purposes or for leveraging gateway devices that are not currently supported by Amazon VPCs VPN solution.

You can create an IPsec VPN connection between your VPC and your remote network. On the AWS side of the VPN connection, a virtual private gateway provides two VPN endpoints (tunnels) for automatic failover. You configure your customer gateway on the remote side of the VPN connection. If you have more than one remote network (for example, multiple branch offices), you can create multiple AWS managed VPN connections via your virtual private gateway to enable communication between these netowrks.

With AWS Site-to-Site VPN, you can connect to an Amazon VPC in the cloud the same way you connect to your branches. AWS Site-toSite VPN establishes secure and private sessions with IPSec and TLS tunnels.

*NB VPN is different to AWS Direct Connect!!!*

