
---

## **Step-by-Step AWS S3 Archival Setup with CLI**
### **1. Create a New AWS Account & IAM Users**
1. Sign up at [AWS Console](https://aws.amazon.com) and create an AWS account.
2. Go to IAM and create:
   - **Administrator Role** with full control.
   - **User Role** with limited permissions (read-only, list bucket).
3. Attach the necessary policies (`AdministratorAccess` for admin, `AmazonS3ReadOnlyAccess` for user).

### **2. Create a VPC, Security Groups, Elastic IP & Private Subnet**
```bash
aws ec2 create-vpc --cidr-block 10.0.0.0/16 --region us-east-1
aws ec2 create-subnet --vpc-id <VPC_ID> --cidr-block 10.0.1.0/24 --region us-east-1
aws ec2 allocate-address --domain vpc
aws ec2 create-security-group --group-name dsl-security-group --description "Your security group description here" --vpc-id <VPC_ID>
aws ec2 authorize-security-group-ingress --group-id <SG_ID> --protocol tcp --port 22 --cidr YOUR_IP/32
```

### **3. Create an S3 Bucket & Enable Replication**
```bash
aws s3api create-bucket --bucket my-archive-bucket --region us-east-1
aws s3api create-bucket --bucket my-replica-bucket --region us-east-1
```
Enable replication policy (JSON format) using `aws s3api put-bucket-replication`.

### **4. Configure Firewall Rules for Specific IP Access**
Use **VPC Security Groups** or **AWS S3 Bucket Policy** for restricting access:
```bash
aws s3api put-bucket-policy --bucket my-archive-bucket --policy file://policy.json
```
Example **policy.json**:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Principal": "*",
      "Action": "s3:*",
      "Resource": "arn:aws:s3:::my-archive-bucket/*",
      "Condition": {
        "NotIpAddress": {"aws:SourceIp": "192.168.1.1/24"}
      }
    }
  ]
}
```

### **5. Auto-Delete Data After Retention Period**
Use **S3 Lifecycle Policies**:
```bash
aws s3api put-bucket-lifecycle-configuration --bucket my-archive-bucket --lifecycle-configuration file://lifecycle.json
```
Example **lifecycle.json**:
```json
{
  "Rules": [
    {"Expiration": {"Days": 365}, "Filter": {"Prefix": "year1/"}},
    {"Expiration": {"Days": 1095}, "Filter": {"Prefix": "year3/"}},
    {"Expiration": {"Days": 2555}, "Filter": {"Prefix": "year7/"}},
    {"Expiration": {"Days": 3650}, "Filter": {"Prefix": "year10/"}}
  ]
}
```

### **6. Securely Transfer On-Prem Data (~10 TB)**
Use **AWS DataSync** or **AWS Snowball** for large transfers.

### **7. Encrypt Data & Enable Key Rotation**
Set **S3 default encryption** and use **AWS KMS** with yearly rotation:
```bash
aws s3api put-bucket-encryption --bucket my-archive-bucket --server-side-encryption-configuration file://encryption.json
```

### **8. Enable Versioning for Audit & Compliance**
```bash
aws s3api put-bucket-versioning --bucket my-archive-bucket --versioning-configuration Status=Enabled
```

### **9. Enable Monitoring with CloudTrail & CloudWatch**
```bash
aws cloudtrail create-trail --name my-cloud-trail --s3-bucket-name my-archive-bucket
aws cloudwatch put-metric-alarm --alarm-name "S3-Access-Monitor" --metric-name "GetObjectRequests"
```

### **10. Set Notifications for Expiry & Security Events**
Use **AWS SNS & SES** for alerts:
```bash
aws sns create-topic --name s3-expiry-alerts
aws sns subscribe --topic-arn <TOPIC_ARN> --protocol email --notification-endpoint admin@company.com
```

### **11. Compute Total Cost of Ownership (TCO)**
Use the **AWS Pricing Calculator** at [AWS Cost Calculator](https://calculator.aws).

### **12. Plan for Environment Tear-Down (Year 10)**
Set **Lambda & CloudWatch Events** to trigger deletion.

---

