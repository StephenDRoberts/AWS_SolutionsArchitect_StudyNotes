# ELB

**Elastic Load Balancing** supports 3 types of load balancers.

If you need flexible application management and TLS termination then you should use an **Application Load Balancer**.

If extreme performance and static IP is needed for your application, then you should use a **Network Load Balancer**.

If your application is built within the EC2 Classic network then you should use a **Classic Load Balancer**.

#### Application Load Balancer

An Application Load Balancer functions at the **application layer**, the 7th layer of the Open Systems Interconnection (OSI) model. After the load balancer receives a equest, it evaluates the listener rules in the priority order to determine which rule to apply, and then selects a target from the target group for the rule action. You can configure listener rules to route requests to different target groups based on the ocntent of the application traffic. Routing is performed independently for each target group, even when a target is registered with multiple target groups.

Application Load Balancers support path-based routing, host-based routing and support for containerized applications.

---

Using an Elastic Load Balancer is an ideal solution for adding elasticity to your application. Alternatively, you can also create a policy in Route 53, such as a Weighted routing policy, to evenly distribute the traffic to 2 or more EC2 instances.

---

ELBs are designed to run in one region only and not accross multiple regions.
