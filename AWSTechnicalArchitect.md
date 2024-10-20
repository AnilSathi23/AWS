https://aws.amazon.com/about-aws/global-infrastructure/

Day 1:
Cloud Computing
AWS
Why AWS
Solution Archiect C03
Learning Management system
Over View
Regions
Core services 
Account Setup
AWS Console
Billing
Delegation to users and roles

Day 2:

IAM (AWS identity and access Management)

Provies Access control to aws resources. That is who can access what.

Create a user
A role

PCI (Payment Card Industry)

STS


CLI
Compute
Benefits
EC2 Storage
Instace Types
AMI: Amazon machine image 
Information about EC2 instance that we are going to launch

OS
Software
Instance
EBS

Placement Group
Metadata


Day 3

EC2 purchasing options
Hibernation
EBS & Encryption
Elastic Load Balancer
Autoscaling


![alt text](image-1.png)

![alt text](image-2.png)




Crating a S3 bucket and uploading a file using cloudshell

[cloudshell-user@ip-10-134-45-239 ~]$ aws --version
aws-cli/2.18.4 Python/3.12.6 Linux/6.1.109-118.189.amzn2023.x86_64 exec-env/CloudShell exe/x86_64.amzn.2023
[cloudshell-user@ip-10-134-45-239 ~]$ aws s3 mb s3://mybuckt-anilkuamarsathi
make_bucket: mybuckt-anilkuamarsathi
[cloudshell-user@ip-10-134-45-239 ~]$ aws s3 ls
2024-10-17 12:45:27 mybuckt-anilkuamarsathi
[cloudshell-user@ip-10-134-45-239 ~]$ echo "My New File" >> file.txt
[cloudshell-user@ip-10-134-45-239 ~]$ ls
file.txt
[cloudshell-user@ip-10-134-45-239 ~]$ cat file.txt
My New File
[cloudshell-user@ip-10-134-45-239 ~]$ aws s3 cp file.txt s3://mybuckt-anilkumarsathi
[cloudshell-user@ip-10-134-45-239 ~]$ aws s3 cp file.txt s3://mybuckt-anilkuamarsathi
upload: ./file.txt to s3://mybuckt-anilkuamarsathi/file.txt       
[cloudshell-user@ip-10-134-45-239 ~]$ aws s3 ls s3://mybuckt-anilkuamarsathi
2024-10-17 12:49:34         12 file.txt


Day 4:

Auto Scaling and its types

    Scheudule Scaling (During peek season)
    Dynamic Scaling ()
    Predictive Scaling (Using Histrorical Data)

Storage
Intro S3
Components of S3
S3 storage classes
Versioning
Cross Region Replication
S3 Life Cycle management
S3 Encryption
Storage gateway




