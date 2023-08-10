# Intro
EC2 = Elastic Compute Cloud
- EC2: VM
- EBS: Data Storage
- ELB: Distribute load
- ASG: Scaling setvices

# Menu

- [EC2 Instance](#chapter-one)
- [Security Groups](#chapter-two)
- [EC2 Instance Connect](#chapter-three)



<br>

# EC2 Instance
- EC2 -> Launch Instance
- New Instance Hello World User Data:
```
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```
- public IPv4 address may shift, prive will not


# Security Groups
- Firewall with policy restraining accesses to instances
- You can edit inbound and outbound rules according to ports
- Roles can be applied to Instances

<br>

# EC2 Instance Connect
Create a temporary web interface connected to the instance.
Note: Should have SSH access rule.

<br>

# Placement Groups

## Cluster
Same Rack, same AZ
- Great Network
- Rack fail -> all fail

## Spread
Span across Availability Zones
- Limited to 7 instances per AZ per placement group
- Low risk

## Partition
Up to 7 partitions per AZ. Can span across multiple AZs in the same region. Up to 100s of EC2 instances.
- The instances in a partition do not share racks with the instances in the other partitions
- A partition failure can affect many EC2 but won’t affect other partitions

<br>

# Elastic IP
Fix public IP
- Default 5 IPs per account
## Elastic Netwok Interfaces (ENI)
Virtual network card
- An ENI enables easy network failover by attching ENI to another instance.
- Grant an additional private IP.
- Bound to AZ

<br>

# EC2 Hibernate
Freeze the RAM states.
- Less than 150G RAM
- Less than 60 days
- EC2 instance root volume type must be EBS to encrypt content

<br>

# EFS & EBS & Instance Store
## EC2 EFS - Elastic File System
- Shared file system on difference instance
- Only with Linux
- Need a security group
- Can be in multiple zones or one zone
- Different throughput modes and per formance modes

## EC2 EBS Elastic Block Storage
- Attched to one instance
- Locked to one AZ
- Using snap shot can migrate EBS volumes

## EFS vs EBS vs Instance Store
- EFS mounting 100s of instances across AZ
- EFS share website files (WordPress)
- EFS only for Linux Instances (POSIX)
- Instance store has short-life-cycle atteched to instance
