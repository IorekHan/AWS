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
- Policy restrain accesses to instances
