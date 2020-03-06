# EC2

#### Connection

If you're ussing PuTTY to connect and get the following errors:

`Error: Server refused our key` ; or
`Error: No supported authentication methods available`

1. Verify you are connecting with the appropriate user name for your AMI (eg ec2-user, root, admin etc, depending on your box).
2. Verify that your provate key (.pem) file has been correctly converted tot he format recognised by PuTTY (.ppk).

#### EC2 & Databases

To improve the write performance of the DB hosted in an EC2 instance, you can achieve this by either:
* setting up a standard RAID 0 configuration or simply by increasing the size of the EC2 instance


*What is Raid 0 configuration?*

Raid 0 (disk striping) is the process of dividing a body of data into blocks and spreading the data blocks across multiple storage devices, such as HDDs or SSDs.
With EBS, you can use any of the standard Raid configurations that you can use with a traditional bare metal server, as long as that paarticular Raid configuration is accomplished at the software level. 
For greate I/O performance than you can achieve iwth a simgle volume, Raid 0 can stripe multiple volumes together.
Raid 0 is used when I/O performance is more important than fault tolerance, eg in a heavily used DB where data replication is already set up separately. Performance of the stripe is limited to the worst performing volume in the set. Loss of a single volume results in a complete data loss for the array.

#### EBS Volumes

An Amazon EBS volume is a durable, block-level storage device that you can attach to a single EC2 instance. You can use EBS volumes as a primary storage for data that requires frequent updates, such as thesystem drive for an instance or storagefor a DB application. You can also use them for throughput-intensive applications that perform continuous disk scans. EBS volumes persis independently from the running life of an EC2 instance.

When you create an EBS volume in an AZ, it is automatically replicated **within that zone** to prevent data loss due to a failure of any single hardware component.

An EBS volume can only be attached to one EC2 instance at a time.

After you create a volume, you can attach it to any EC2 instance in the same AZ.

An EBS volume is off-instance storage that can persist independently from the life of an instance. You can specify not to terminate the EBS volume when you terminate the EC2 instance during instance creation.

EBS volumes support live configuration changes while in production which means that you can modify the volume type, volume size and IOPS capacity without service interruptions.

Amazon EBS encryptions uses 256-bit Advanced Encryption Standard algorithms (AES-256).

EBS volumes offer 99.999% SLA.

EBS Snapshots occur asynchronously so you can use the EBS volume as normal while a snapshot is in progress.

This means that the point-in-time snapshot is created immediately but the status of the snapshot is 'pending'. until the snapshot is complete.

You can use Amazon Data Lifecycle Manager (Amazon DLM) to automate the creation, retention and deletion of snapshots taken to back up your Amazon EBS volumes. Automating snapshot management helps you to:
* Protect valuable data by enforcing a regular backup schedule
* Retain backups as required by auditors or internal compliance
* Reduce storage costs by deleting outdated backups

Combined with the monitoring features of Amazon CloudWatch Events and AWS CloudTrail, Amazon DLM provides a complete backup solution for EBS volumes at no additional cost.

Amazon DLM is the fastest and most cost-effective solution that provides an automated way of backing up your EBS volumes.

#### Auto Scaling

**Cooldown** ensures that the Auto Scaling group does not launch or terminate additional EC2 instances before the previous scaling activity takes effect.

Its default value is 300 seconds.

It is a configurable setting for your Auto Scaling group.

#### Pricing

You will be billed when your Reserved Instance is in `terminated` state
You will be billed when your On-Demand instance is preparing to hibernate with a `stopping` state.

#### Groups

You can launch EC2 instances in a placement group, which determines how instances are placed on underlying hardware. When you create a placement group, you specify one of the following strategies for the group:

* **Cluster** - clusters instances into a low-latency group in a single Availability Zone
* **Spread** - spreads instances across underlying hardware
