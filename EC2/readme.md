# Intro
EC2 = Elastic Compute Cloud
- EC2: VM
- EBS: Data Storage
- ELB: Distribute load
- ASG: Scaling setvices

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

# EC2 Instance Connect
Create a temporary web interface connected to the instance.
Note: Should have SSH access rule.
