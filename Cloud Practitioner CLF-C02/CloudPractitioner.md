AWS Artifact: You can locate AWS compliance report and access agreements made with AWS.

Reviewing the full history of change made to your application's data is done using Amazon Quantum Legder Database (QLDB) provides cryptographically verifiable transaction log which is fully transparent and immutable.

S3 Glacier was created for a retieval time that is 3-5 hours and for data that is infrequently accessed.

AWS Firewall Manager is a service for security management and enables you to perform configuration and management of firewall rules centrally across accounts and applicaitons in AWS organization. You can also enforce  a set of security rules to keep new resources and applications in complaince. You can also deploy Network firewall using AWS firewall manager. AWS Network Firewall enables securing virtual networks at a large scale. It allows for traffic filtering at the perimeter of a VPC.

Amazon macie is fully managed service providing data security and privacy. It utilizes machine learning and pattern matching for monitoring and protecting sensitive data on AWS system. Macie provides automation for discovering sensitive data in S3 buckets This data can include both PII and financial data.

AWS Resource Access Manager(AWS RAM) This is an AWS Service used for sharing resources securely accross multiple AWS accounts and within organizaitonal units and organizations. AWS RAM enables respire sharing with AWS IAM usersa nd roles for various resource types, allowing you to create a resource once and then use AWS RAM  to share that resource with other accounts.

AWS Trusted Advisor gives you the ability to validate service limits using the performance category. This section shows you the different types of limits and usage information related to the AWS resource you are currently using. For example, if you are using an application programming interface (API) gateway, then you can modify the throttle rate based on your account Region. Here you can increase the throttle rate by ten thousand requests per second. You can also increase Auto Scaling limits and discovery service limits. This resource allows you to increase performance while following best practices within the industry.

AWS Personal Health Dashboard only focuses on the health of AWS resources, such as hardware checks.

The Effects section of an AWS Identity and Access Management (IAM) policy determines the behaviors and actions of what the policy will allow. You have to understand the effects of what occurs when a user might request access by either allowing or denying the request. Because the default option is to deny everything within the first type of requests, you have to grant specific permissions that you might need.

Amazon CloudFront is a great AWS solution that increases the speed at which data is distributed to multiple data centers called edge locations. A user requests dynamic or static content from their closest geographic edge location with the smallest network delays. This process dramatically decreases the time at which customers wait on their data.

AWS Data Exchange allows you to locate and use third-party information that is related to sustainability. This provides you access to data sets which are accessible through the Open Data Sponsorship Program and Amazon Sustainability Data Initiative. AWS works with companies for making Environmental, Social & Governance (ESG), weather, satellite imagery, and air quality data accessible to clients.

AWS Trusted Advisor is a tool that indicates how you should provision your AWS resources as per AWS best practices. It performs real-time monitoring of your AWS resources and recommends actions accordingly.

AWS Outposts allow a company to use AWS services inside of their own data center or company building. Outposts create a miniature Region inside of a data center, providing all AWS services in an isolated private location. This is an example of a hybrid cloud approach.

AWS Storage Gateway provides secure and seamless access for on-premises systems and applications to unlimited storage on AWS.


An Amazon DynamoDB database provides a NoSQL database service that delivers millisecond returns on data to the end user or application. You can fully manage the production within the cloud infrastructure. This database supports key-value and document store models, and is a good fit for web, gaming, mobile, and ad tech systems. It also supports replication across multiple masters and multiple Regions using its global tables option. It has self-managed backups utilizing its native database protection option with on-demand and continuous backup solutions.

Amazon Aurora is a relational database that offers PostgreSQL- and MySQL-compatible database solutions. It is fully managed by Amazon Relational Database Service (RDS). Amazon Aurora is not considered a NoSQL database service.

Amazon Relational Database Service (RDS) is a database cloud solution for applications that require Oracle, PostgreSQL, MariaDB, MySQL, Microsoft SQL Server, or Amazon Aurora. This is not considered a NoSQL database option.

Amazon Redshift is a petabyte-scaled infrastructure that is considered a data warehouse solution. This is not a NoSQL database.


Customer-specific controls are very specific in that the overall controls and responsibilities fall to the customer. They are responsible for support in all manners, which includes the creation, installation, and development of applications that reside on top of an Amazon Elastic Compute Cloud (EC2) infrastructure. Customers are also responsible for patching, configuration, and training, but these are considered shared by both Amazon and customers. Customer-specific controls are network traffic, data identity and integrity, client and server-side data, encryption, and authentication.

Patch Management controls is not correct because this is a shared control, which means that AWS is responsible for patching the underlying AWS platform and the customer is responsible for patching software that resides on top of the AWS EC2 instance.

Configuration Management controls is not correct because this is also a shared control, which means that AWS is responsible for configuration infrastructure devices associated with the network and the customer is responsible for supporting their own operating systems and applications that they use on the AWS platform.

Awareness and Training controls is not correct because this is not a customer-specific control but a shared control. This means that customers are responsible for learning and training their own people and AWS is responsible for the awareness and training of AWS resources.

A Convertible Reserved Instance can be exchanged within the same term and you can easily select new instance attributes such as instance type and platform. You can also change the instance family scope and tenancy. There are no limitations on the number of times you exchange your instance. The only requirement is that the instance type you are changing to has to be of higher or equal value to the original instance.

Spot Instances are primarily viable for batch type processing environments, but are considered an instance that could be interrupted. Therefore, they would not be a good fit for an application that requires 24/7 uptime.

On-Demand Instances are primarily used for temporary areas of increased workloads and processing, and are not available 24/7.

Cost Optimization is a framework pillar that supports the improvement and efficiencies of an AWS infrastructure over its complete lifecycle. The purpose of cost optimization is to meet functional requirements while achieving the smallest price point available. From a design perspective, its principles are overall efficiency, consumption modeling, not spending money on data centers, analyzing expenditures, and using managed services.

Performance Efficiency is a framework pillar that supports computing resources to maintain and meet business requirements as technologies change over time within the AWS infrastructure. The focus is on performance rather than improvement and refinement.

Storage is a sub-component found under the performance efficiency pillar. Storage refers to the different types of storage relating to file, block, and object-level storage. This is not related to the improvement and refinement pillar.

Reliability is focused on the stability of AWS systems and their ability to support business value with long uptimes and durable systems. This pillar is not focused on improvement and refinement but rather the durability and uptime of an AWS resource.


You would use DynamoDB when using a serverless database system and when catering to up to 45 million requests per second. You do not need to install or patch any software for it. Being highly scalable, DynamoDB has a millisecond response time and can handle 45 million requests per second. DynamoDB is a non-relational database, which means that data is stored in tables as key value pairs. You can update the attributes of the items in these tables. Each attribute can be viewed as a feature of the data. Non-relational databases are also called NoSQL databases.

You would not utilize the Amazon DynamoDB database when utilizing SQL for data organization. To utilize SQL for data organization, you need a relational database solution, which can include Amazon’s Relational Database Service (RDS). RDS is a fully managed service where AWS handles all the administrative support related to the database like provisioning hardware, patching, and performing backups. This is in contrast to a situation where you would install databases manually on Amazon Elastic Compute Cloud (EC2) instances which would be time consuming and entail a lot of additional overhead of maintaining the database. RDS offers encryption at rest and in transit for several of its supported database engines. RDS is available for database engines like Amazon Aurora, MySQL, PostgreSQL, MariaDB, Oracle Database, and Microsoft SQL Server.

You would not utilize the Amazon DynamoDB database when creating a scalable data warehousing solution. To create a scalable data warehousing solution, you would need to use Amazon Redshift. It helps perform big data analytics and has the capability to collect data from multiple sources. This way you can analyze trends and relationships within your data. Redshift offers very high performance tailored for business intelligence workloads. Redshift nodes routinely run into petabyte sizes. You can use Redshift Spectrum to run SQL queries on exabytes of data residing in data lakes.

You would not utilize the Amazon DynamoDB database when storing data using Amazon Aurora. To store data using Amazon Aurora, you would not use DynamoDB. Amazon Aurora is a relational database that operates at the enterprise level. It is five times quicker than MySQL and three times quicker than PostgreSQL. Amazon Aurora helps reduce the operating costs of your database by reducing redundant IO operations and ensures the high availability and reliability of the database. Amazon Aurora replicates six copies of data across three Availability Zones (AZs) and backs up data to Amazon S3.

The most effective solutions is to use AWS Organizations and service control policies because you can use an AWS Organization account to manage all of your AWS accounts. You would then create a service control policy that controls the actions and services of users or roles. These policies allow you to easily manage AWS accounts and their different functions as it relates to users’ job roles.

The AWS corporation is not responsible for the management of AWS accounts, so you would not contact AWS to configure your initial AWS Identity and Access Management (IAM) roles and users.

You cannot create a new IAM policy role for users on the east coast and user accounts for the west coast. You need to create AWS user accounts for all users. You would then determine which roles should have specific authorizations and assign those roles to the respective AWS users, regardless of their location.

You should not create one ID for the east coast users and one ID for the west coast users. You should never allow groups of users to share the same account to log in to any type of production or even non-production system.

Terminating unused Elastic IPs is the most sustainable option. Elastic IPs are public static IP addresses that you allocate to your resources. By terminating unused Elastic IPs, you are avoiding unnecessary charges and the associated environmental impact of running those resources.

Scaling up an EC2 instance increases the resource consumption of the instance. While it might be necessary for handling increased load, it's not the most sustainable approach in the context of this question where we're looking to minimize resource usage.

Enabling detailed billing reports might help you identify areas for cost optimization but it does not directly reduce resource usage itself.

Implementing a vulnerability scanning tool for security does not directly address resource usage or environmental impact in the context of the sustainability pillar.


You would use AWS License Manager which is an AWS service that simplifies the management of software licenses from multiple vendors, including IBM, Oracle, SAP, and Microsoft, through a centralized system. It covers both your AWS and on-premises systems. AWS License Manager also lets you change license types between bring your own license (BYOL) and AWS-provided licenses with your licensed media. Using BYOL opportunities can help you save costs on cloud infrastructure.

You would not use Amazon Rekognition. Amazon Rekognition allows you to have video and image analysis capabilities in your applications.

You would not use Amazon Forecast. Amazon Forecast provides accurate, time-series forecasts using ML and statistical algorithms.

You would not use AWS X-Ray. AWS X-Ray provides detailed data on requests that your application serves.


Bootstrapping is the name for a set of common applications that apply service packs, security patches, and security updates, and has the ability to register Amazon Elastic Compute Cloud (EC2) instances to execute security monitoring remotely and to manage other systems. Some bootstrapping applications include Cfn-Init, Cloud-Ini, Capistrano, Chef, and Puppet. When you deploy AWS Cloud Development Kit (CDK) apps into an AWS account and Region (collectively called an environment), you need to provision resources that AWS CDK needs for making deployments. Bootstrapping is the process of provisioning initial resources for deployment which include an Amazon Simple Storage Service (S3) bucket and Identity and Access Management (IAM) roles.

The Trusted Advisor tool checks the compliance on AWS Identity and Access Management (IAM) configurations to make sure they have secure access to respective AWS resources. It also validates ports such as 22, 3389, and 5500, and multiple database ports such as 1433, 3306, and 1521. It is not a tool that installs security updates on an EC2 system.

IAM policies are a way of defining permissions for a user or resource by attaching this component. This component is then evaluated as allowed or denied. This is not a tool used for installing security patches.

Amazon DynamoDB Accelerator (DAX) is an AWS feature that implements an in-memory acceleration component used by DynamoDB application programming interface (API) that creates up to ten times faster response times. This caching feature lets you dynamically scale to the demand of the application workload. This is incorrect because it is not a tool used to install service packs or security patches.


Amazon Relational Database Service (RDS) can scale, operate, and configure several different types of relational databases within the Amazon cloud infrastructure. It allows you to easily provision database selection, hardware setup, backups, and even patching.

Database Migration Service is a product used to easily migrate or replicate data to an Amazon RDS infrastructure. This service does not allow you to create databases.

Amazon DynamoDB is a NoSQL database solution within the Amazon infrastructure that is inexpensive and has unlimited storage capacity. Amazon DynamoDB is a specific relational database and does not allow you to create other database solutions.

Amazon RedShift is an Amazon warehouse solution for managing up to petabytes of data. It increases performance using columnar storage technology by increasing IO blocks across a multi-node solution. This product does not allow you to create other relational database solutions.

AWS usage should be focused on building applications spread across multiple Availability Zones (AZ) and Regions. You can always extend your application by adding load balancers and additional AZs to your preconfigured scaling group, but spreading your application workload across different AZs and even Regions will create a level of increased elasticity with expanding application functionality and data integrity.

You never want to focus on reducing costs when expanding the architecture of your application. The key is to separate your primary functions onto different Amazon Elastic Compute Cloud (EC2) instances and add additional AZs and Regions as needed.

AWS usage focused on Amazon S3 components is too finite of an option from an architectural perspective.

You will use security groups for this. A security group is a virtual firewall that protects an EC2 instance. Security groups allow all outbound traffic and deny all inbound traffic by default. You can customize a security group to specify the kinds of traffic that may be permitted or denied.

You will not use a network access control list (NACL). An NACL is a virtual firewall for controlling incoming and outgoing traffic on a subnet. A subnet is a section of a virtual private cloud (VPC) where resources can be grouped based on their security or functional requirements.

You will not use AWS Web Application Firewall (WAF). A WAF controls incoming requests from a network into your web applications. AWS WAF permits or denies traffic based on a web access control list (ACL). AWS WAF works in conjunction with Amazon CloudFront as well as Application Load Balancer.

You will not use AWS Marketplace. This is a digital library that contains thousands of third-party software from across varying applications and industries. You can view detailed data on each software listing, which includes user reviews, pricing options, and support plans. Some of the categories that AWS Marketplace provides software for include: DevOps, business applications, machine learning (ML), Internet of Things (IoT), security, data products, and infrastructure.

You can create theree customer support cases using AWS support

a) Account and billing
b) Service limit increase
c) Technical support

You cannot create technical support cases if you have a Basic support plan. 

To change your support plan, you do not create a customer support case but access Support plans from the AWS Management Console using your root account.

To close your account, you do not create a customer support case but access the Billing and Cost Management console and navigate to the Close Account section.

You do not change the root account email address by creating a customer support case. To change the root account email address, you need to access the Billing and Cost Management console and navigate to the My Account section.

A Botnets infection is like that of a Trojan horse, worm, or virus that attempts to infect a large set of Amazon Elastic Compute Cloud (EC2) instances, such as a fleet of servers. It could be possible that the Botnet infection is comprised of a small network of servers with malicious undetectable code that could bring down an entire network by infecting multiple servers. It is typical with this type of infection that it is controlled remotely or externally by a user with malicious intent.

Multi-factor authentication (MFA) is a security option for validating a user’s identity on a network, based on substantiating two or more pieces of information, and is not related to attacks.

SPAM is where a system can be under siege by having an attacker distribute large amounts of unsolicited mail throughout your network. Amazon EC2 is set up to limit this feature, but it is still the responsibility of the customer to prevent this security concern.

The Trusted Advisor tool checks the compliance on AWS Identity and Access Management (IAM) configurations to make sure it has secure access to respective AWS resources. Overall, the tool looks for security flaws in configuration components and for performance issues in systems, while also looking for underutilized resources. It has nothing to do with malicious attacks.


You would select Spot Instances for any workloads that can withstand interruptions. These can include batch processing workloads. Spot Instances offer up to 90% discount over On-Demand Instance pricing with the caveat that they can be reclaimed at any time by AWS following a two-minute warning.

Savings Plan model is not the right choice for workloads that are interruptible, but this model is more suited for consistent Amazon Elastic Compute Cloud (EC2) usage. This usage can be committed to by a user for one- to three-year terms, and the usage itself is measured in dollars per hour. The Savings Plan model can help save up to 72% on compute usage costs. This model is not limited by the EC2 instance family, tenancy, region, size, or OS. It can also be applied to AWS Lambda and Fargate usage, which are serverless compute systems.

On-Demand Instances are not suitable for interruptible workloads. On-Demand Instances are suited for workloads that are irregular but not interruptible. They are ideal for testing applications. They do not need upfront payments and can be paid for based on usage. 

Dedicated Hosts are not suitable for irregular workloads and are the most expensive of all instance options. These are actual physical servers that have Amazon EC2 instances and completely dedicated to the customer that has purchased them. This allows customers to utilize their existing per-Virtual Machine (VM), per-socket, or per-core licenses that ensures license compliance. You can purchase On-Demand Dedicated Hosts as well as Dedicated Hosts Reservations.

