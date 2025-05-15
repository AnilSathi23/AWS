# AWS

**read white paper about well archiected framework**

https://aws.amazon.com/
https://infrastructure.aws/

VPC

Virtual Data center: It is a great solution to have a wall between internet and your infrastructure where you can decided to expose only part of your infrastructure.

It is a public cloud that allows a company to create its own provate cloud like computing environment on a shared public cloud infrastructure.

VPC Main Concepts

What is an IPaddress?

Subnet
A subnet, or subnetwork, is a logical subdivision of an IP network. The process of dividing a network into subnets is called subnetting. Subnets are used to make networks more efficient by reducing the distance that network traffic has to travel

Route Table
In computer networking, a routing table, or routing information base, is a data table stored in a router or a network host that lists the routes to particular network destinations, and in some cases, metrics associated with those routes.

A set of rules called routes is used to decided network traffic direction

DCP option sets
A DHCP option set is a group of network settings used by resources in your VPC, such as EC2 instances, to communicate over your virtual network.

Security Groups
Virtual Firewall. The moment you add the inbound rules the outbound rule is applied

Network access control
Internet Gateway
A gateway to allow interaction between VPC  resoures and the internet

NAT Gateway
Entity that allows your private instances to talk to the internet.

VPC endpoint
An endpoint to connect to a service

Elastic IP Address

CIDR Range

Subnet

ways to access AWS or VPCs

AWS management console
AWS SDKs
CLI
API query

VPC peering -- connecting 2 different networks

DNS : is used ot translate readable human domain names to IP addreses



sudo su
yum update -y
yum install httpd
systemctl start httpd
systemctl enable httpd
echo "Hello World" > /var/www/html/index.html
 
curl http://169.254.169.254/latest/meta-data
curl http://169.254.169.254/latest/meta-data/ami-id
curl http://169.254.169.254/latest/meta-data/hostname
curl http://169.254.169.254/latest/meta-data/instance-id
curl http://169.254.169.254/latest/meta-data/instance-type
 
curl http://169.254.169.254/latest/dynamic
curl http://169.254.169.254/latest/dynamic/instance-identity
curl http://169.254.169.254/latest/dynamic/instance-identity/document
 
curl -s http://169.254.169.254/latest/dynamic/instance-identity/document > /var/www/html/index.html


Course Update for Step 05: Getting Meta data and Dynamic data
To improve security, Instance Metadata Service v2 (IMDSv2), now needs authentication token to get meta-data or dynamic data

Step 1: Get the token

TOKEN=$(curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600")

Step 2a: Use the token to call meta-data

curl -H "X-aws-ec2-metadata-token: $TOKEN" -v http://169.254.169.254/latest/meta-data/

OR Step 2b: Use the token to call dynamic data

TOKEN=$(curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600")
curl -H "X-aws-ec2-metadata-token: $TOKEN" -v http://169.254.169.254/latest/dynamic/instance-identity/

TOKEN=$(curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600")
curl -H "X-aws-ec2-metadata-token: $TOKEN" -v http://169.254.169.254/latest/dynamic/instance-identity/ > /var/www/html/index.html


User-Data

#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
curl -s http://169.254.169.254/latest/dynamic/instance-identity/document > /var/www/html/index.html


#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
curl -s http://169.254.169.254/latest/dynamic/instance-identity/document > /var/www/html/index.html

#!/bin/bash
curl -s http://169.254.169.254/latest/dynamic/instance-identity/document > /var/www/html/index.html
mkdir /var/www/html/a
echo “Microservice A” > /var/www/html/a/test.html
