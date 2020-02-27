# Virtual Private Clouds (VPCs)

#### Security Groups

Act as a virtual firewall for your instance to control inbound and outbound traffic.
You can assign up to five security groups to the instance.
Security groups act at an ***instance level***, not the subnet level. Therefore, each instance in a subnet in your VPC could be assinged to a different set of security groups. If you don't specify a particular group at launc time, the instance is automatically assigned to the default security group of the VPC. 

#### NACLs

To control the traffic in and out of your VPC network, you can use the Network Access Controls List.

It is an optional layer of security for your VPC and acts as a firewal for controlling traffic in and out of one or more subnets.
