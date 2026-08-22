# AWS — Revision Notes

**Category:** Electives · **Focus Area:** AWS CLI · **Level:** Intermediate

---

## Table of Contents

1. [Introduction to AWS Cloud](#1-introduction-to-aws-cloud)
2. [Technology — Core Services](#2-technology--core-services)
3. [AWS Resources for Technology Support](#3-aws-resources-for-technology-support)
4. [Security and Compliance](#4-security-and-compliance)
5. [AWS Cloud Architecture](#5-aws-cloud-architecture)
6. [Billing and Pricing](#6-billing-and-pricing)

---

## 1. Introduction to AWS Cloud

### 1.1 AWS Cloud Practitioner Course Introduction

Basics of cloud computing concepts covered: **Core AWS services**, **Security**, **Architecture**.

**AWS Services (broad categories):**
- Compute
- Storage
- Networking
- Database

**Security:**
- Cloud security concepts
- Access management
- Shared responsibility model
- Multiple services managing compliance
- Management services

### 1.2 How Does AWS Work?

AWS spans a very wide range of service categories, including:

Compute · Quantum Technologies · Security, Identity & Compliance · Containers · Management & Governance · Storage · Database · Media Services · AWS Cost Management · Migration & Transfer · Front-end Web & Mobile · AR & VR · Application Integration · Machine Learning · Networking & Content Delivery · Developer Tools · Customer Engagement · Business Applications · End User Computing · Blockchain · Analytics · IoT · Game Development

### 1.3 The Expense Advantage

| Traditional (CapEx) | AWS (OpEx) |
|---|---|
| Upfront capital costs for data centers | Pay as you consume resources |

### 1.4 AWS Global Infrastructure

| Component | Description |
|---|---|
| **Region** | A geographic area containing multiple, isolated locations |
| **Availability Zone** | An isolated location within a region |
| **Edge Locations** | Sites used for content delivery closer to end users |

**Selecting a Region — factors to consider:**
- Data governance, legal requirements
- Proximity to customers (latency)
- Services available within the region
- Costs (vary by region)

### 1.5 Ways to Interact with AWS

| Method | Description |
|---|---|
| **AWS Management Console** | Easy-to-use graphical interface |
| **Command Line Interface (AWS CLI)** | Access services using the CLI |
| **Software Development Kits (AWS SDKs)** | Access services in application code |

---

## 2. Technology — Core Services

### 2.1 Amazon Simple Storage Service (S3)

- **Object-level storage**
- Unlimited storage — a single object is limited to **5TB**
- Granular access to buckets and objects
- **99.999999999% durable** (11 nines)

**S3 Access Control:**

| Setting | Description |
|---|---|
| S3 (default) | Private |
| S3 Public | Everyone can access |
| S3 Access Policy | Controlled access |

**S3 Bucket Properties:**
- Bucket versioning
- Server access logging
- Tags
- Event notifications
- Encryption
- Transfer acceleration
- Object lock
- Requester pays
- Static website hosting

### 2.2 Amazon Glacier

Low-cost data archival for long-term backup and retrieval.

| Retrieval Option | Time |
|---|---|
| Standard | 3 to 5 hours |
| Bulk | 5 to 12 hours |
| Expedited | 1 to 5 minutes |

- **Archive** — any object such as a photo, video, or document
- **Vault** — a container for storing archives

### 2.3 S3 Storage Classes

| Storage Class | Description |
|---|---|
| **Standard** | Frequently accessed data |
| **Amazon S3 Intelligent-Tiering** | Automatically moves objects between two access tiers of storage |
| **Infrequent Access** | Long-lived, infrequently accessed data |
| **One Zone-Infrequent Access** | Long-lived, infrequently accessed, non-critical data |
| **Glacier** | Archiving rarely accessed data |
| **Deep Archive** | Long-term archive data |

**Example lifecycle transition timing:**
- Amazon S3 Standard → 30 days
- → S3 Standard-Infrequent Access → 60 days
- → S3 Standard-Infrequent Access → 365 days → Delete

### 2.4 Getting Started with AWS Cloud — Amazon EC2

**What is Amazon EC2 used for?**

Application Server · Web Server · Game Server · Mail Server · File Server · Proxy Server · Gateway Server · Media Server

**Benefits of EC2:** Control, Elasticity, Flexibility, Integrated, Reliable, Secure, Inexpensive

**EC2 Instance Type — Model Name Format:**

Example: `c5.large`
- **c** — family name
- **5** — generation number
- **large** — size of the instance

**EC2 Instance Types:**

| Category | Instance Types | Use Case |
|---|---|---|
| **General Purpose** | Mac, T3, T2, M5, M5A, M4 | Good for burstable workloads like websites and web applications |
| **Compute Optimized** | C5, C4 | Optimized for compute-intensive workloads |
| **Memory Optimized** | R5, R4, X1e, X1, z1d, High Memory instances | Optimized for memory-intensive workloads |
| **Accelerated Computing** | P3, P2, G3, F1 | Performance GPU-based instances, commonly used for machine/deep learning |
| **Storage Optimized** | H1, I3, D2 | Distributed filesystems |

> **Note:** Intel and AWS have been partners for more than 16 years. Amazon routinely introduces new Intel processor generations for EC2 instances, such as Intel Xeon CPUs, to give customers high performance and value.

### 2.5 Amazon EC2 and AMI

**AMI (Amazon Machine Image)** includes:
- A template for the root volume
- Launch permissions
- A block device mapping

**Benefits of AMIs:** Repeatability, Reusability, Recoverability, Backups, Marketplace and Solutions

### 2.6 Amazon Elastic Block Store (EBS)

- Multiple EBS volumes can be attached to the same instance, but each volume can be attached to **only one instance at a time**
- **Benefits:** Performance for any workload, highly available and durable, different drive types, virtually unlimited scale

**Solid State Drives (SSD):**
- Provisioned IOPS SSD (io1) Volumes
- General Purpose SSD (gp2) Volumes

**Hard Disk Drives (HDD):**
- Throughput Optimized HDD (st1) Volumes
- Cold HDD (sc1) Volumes

### 2.7 Virtual Private Cloud (VPC)

**What is VPC?**
- Virtual private network space in the AWS Cloud
- Logical isolation for your workload
- Custom security and access control for your resources

**VPC Definitions:**
- A VPC is a virtual network dedicated to an AWS account
- Requires an IPv4 address space (IPv6 address range optional)
- Creates a specific CIDR range for your resources
- Strict access rules for inbound and outbound traffic

**Deploying a VPC:**
- A VPC can launch resources from any Availability Zone within its region
- VPCs deploy into 1 of the 31 AWS regions

**VPC Limitations:**
- You can deploy multiple VPCs in the same region or in different regions
- Service limitation: **5 VPCs per region per account**

**VPC and Subnets:**
- Subnets are a subset of the VPC CIDR block
- Subnet CIDR blocks cannot overlap each other
- Each subnet must reside entirely within one Availability Zone
- An Availability Zone can contain multiple subnets
- AWS reserves **5 IP addresses** from each subnet

**Internet Gateway** — connecting public subnets to the internet:
- Allows communication between resources in your VPC and the internet
- Horizontally scaled, redundant, and highly available by default
- A route table target for internet-routable traffic

**NAT Gateway** — connecting private subnets to the internet:
- Enables instances in the private subnet to initiate outbound traffic to the internet or other AWS services
- Prevents private instances from receiving inbound traffic from the internet

**Elastic Network Interfaces (ENI):**
- A virtual network interface that can be moved across EC2 instances in the same Availability Zone
- Maintains: Private IP address, Elastic IP address, MAC address

**Security Groups (Virtual Firewall):**
- Controls inbound and outbound traffic; traffic can be restricted by protocol, port, or IP
- Rules are **stateful** — allows response traffic from allowed inbound traffic automatically

**Security Groups — Default Values:**
- All inbound traffic **blocked**
- All outbound traffic **allowed**

**Network Access Control Lists (ACLs):**
- Firewalls at the **subnet level**
- By default, allow all inbound and outbound traffic
- Rules are **stateless** — requires explicit rules for both inbound and outbound traffic

### 2.8 Monitoring and Autoscaling

**Amazon CloudWatch:**

**Monitors:**
- AWS resources
- Applications running on AWS

**Collects and tracks:**
- Standard metrics
- Custom metrics

**Alarms:**
- Send notifications
- Automatically make changes based on rules you define

**Dynamic Scaling with Amazon EC2 Auto Scaling:**
- Maintains performance cost-effectively by adjusting the size of the Auto Scaling group dynamically
- Removes instances automatically when demand decreases
- Adds instances automatically when demand increases

**Elastic Load Balancer (ELB):**
Distributes incoming traffic across targets like EC2 instances, IP addresses, and containers.

| Load Balancer | Description |
|---|---|
| **Application Load Balancer** | Distributes HTTP and HTTPS requests to the respective targets (Layer 7 of the OSI model) |
| **Network Load Balancer** | Can handle millions of requests per second; operates at Layer 4 of the OSI model |

### 2.9 Databases

**Amazon RDS:** AWS Relational Database Service enables quickly setting up, operating, and scaling a database in the cloud.

**Amazon Aurora:** A relational database engine offered by AWS.

**Amazon DynamoDB:**
- Fully managed, non-relational
- Single-digit millisecond latency
- Scales horizontally
- Backup and point-in-time recovery

**DynamoDB Use Cases:**
- Serverless web applications
- Microservices data store
- Mobile backends
- Ad tech
- Internet of Things (IoT)

**Other Purpose-Built Database Services:**

| Service | Description |
|---|---|
| **Amazon Redshift** | A fast and scalable data warehouse |
| **Amazon DocumentDB** | A fast and highly available MongoDB-compatible database |
| **Amazon Neptune** | A high-performance graph database |

---

## 3. AWS Resources for Technology Support

### 3.1 AWS CloudFormation

- Allows you to create a collection of related AWS resources in an orderly fashion
- Infrastructure modeled in a text file
- Resource provisioning is done in a safe and repeatable manner
- Infrastructure as Code — write templates using **JSON** or **YAML**

**Flow:** `Template → S3 Bucket → CloudFormation → Stack Creation`

### 3.2 AWS Elastic Beanstalk

Helps quickly deploy applications without worrying about hardware provisioning. Once an application is uploaded, Beanstalk takes care of:

- Resource provisioning
- Load balancing
- Automatic scaling
- Monitoring

**Features:** Application platforms, Application deployment options, Application health, Monitoring, Management and updates, Scaling, Customization, Compliance

### 3.3 AWS Direct Connect

Used to create a dedicated private network between an on-premise data center and the AWS Cloud.

- Reduces bandwidth cost
- Consistent network performance
- Private connectivity to your Amazon VPC
- Easy scalability

**Example:** Connect your corporate data center to AWS Cloud using AWS Direct Connect.

### 3.4 Amazon Route 53

A managed DNS service in AWS. Highly available and scalable.

- Route traffic
- Register domain names
- Health check

### 3.5 Amazon Elastic File System (EFS)

A fully managed service providing shared file system storage for Linux workloads.

- Dynamic elasticity
- Scalable performance
- Shared file storage
- Fully managed
- Cost-effective

**Example:** EC2 instances and on-premise servers sharing EFS for application data.

### 3.6 AWS Lambda

**Benefits of AWS Lambda:**
- Multiple programming languages support
- Automated administration
- Built-in fault tolerance
- Automatic scaling
- Orchestrate multiple functions
- Pay-per-use pricing

### 3.7 Amazon Simple Notification Service (SNS)

A fully managed messaging service for distributed applications.

**Features:**
- Reliability and durability
- Scalability
- Message filtering and routing
- Security

**SNS Overview:** A publisher sends messages to the SNS topic; SNS in turn sends messages to all the subscribers (**Pub/Sub model**).

### 3.8 Amazon CloudFront

A fast Content Delivery Network (CDN) service that securely delivers data to customers globally.

**Advantages:** Faster performance, Secure, Programmable, Cost effective

### 3.9 Amazon ElastiCache

An in-memory database service in the cloud.

---

## 4. Security and Compliance

### 4.1 Security is our Top Priority

- Security
- Monitoring
- High availability
- Automation
- Accreditation

> The AWS infrastructure has been architected to be one of the most flexible, reliable, scalable, and secure cloud computing environments available today.

### 4.2 Security of the Cloud

| Layer | Components |
|---|---|
| **Foundation Services** | Compute, Storage, Database, Network |
| **Global Infrastructure** | Availability Zones, Regions, Edge Locations |

**Security requirements the customer needs to consider:**
- Content they store
- AWS services they use
- Country in which they host data
- Who has access to the content

### 4.3 Managed vs Unmanaged Services

| Managed Services | Unmanaged Services |
|---|---|
| Amazon S3 | Amazon EC2 |
| Amazon RDS | Amazon EBS |
| Amazon DynamoDB | — |

### 4.4 Security and Compliance Products

AWS Artifact · AWS Certificate Manager · Amazon Cloud Directory · AWS CloudHSM · Amazon Cognito · AWS Directory Service · AWS Firewall Manager · AWS GuardDuty · AWS IAM · Amazon Inspector · AWS KMS · Amazon Macie · AWS Organizations · AWS Shield · AWS Secrets Manager · AWS Single Sign-On · AWS WAF

### 4.5 AWS Identity and Access Management (IAM)

| Concept | Description |
|---|---|
| **IAM User** | An entity that represents a user or an application which interacts with AWS |
| **IAM Group** | A group of IAM users |
| **IAM Role** | An identity that can be assumed for temporary privileges |

**Authentication:** The method of checking that a user and host is who they claim to be.

**Authorization:** The method of determining what permissions a user has in AWS.

**IAM Role details:**
- IAM Roles are assumed by users or applications
- An IAM Role is attached with an IAM policy for permission
- Temporary credentials are provided for users/applications assuming the role

### 4.6 Amazon Inspector

- Temporary credentials are provided for users/applications assuming the role
- Assesses applications for:
  - Exposure
  - Vulnerabilities
  - Deviations from best practices

### 4.7 DDoS Attacks and AWS Shield

**Distributed Denial of Service (DDoS) attacks:** Cybercriminals use several sources to attack a target and make the application unavailable.

**AWS Shield** is a managed service that safeguards applications running on AWS from DDoS attacks.

| Plan | Features |
|---|---|
| **AWS Shield Standard** | Quick detection, inline attack mitigation, no cost |
| **AWS Shield Advanced** | Enhanced detection, advanced attack mitigation, visibility and attack notification, DDoS cost protection, specialized support |

### 4.8 AWS Compliance

**AWS attestations and certifications.**

**How AWS helps customers achieve compliance:**
- Sharing information
- Industry certifications
- Security and control practices
- Compliance reports directly under NDA
- Assurance program
- Certifications/attestations
- Laws, regulations, and privacy
- Alignments/frameworks

**Customer responsibility:**
- Review
- Design
- Identity
- Verify

---

## 5. AWS Cloud Architecture

### 5.1 AWS Well-Architected Framework

**What is a Well-Architected Framework?**

A designing infrastructure guide comprising:
- Secure
- High-performing
- Resilient
- Efficient

- A systematic approach to evaluating and implementing architectures
- Established best practices developed through lessons learned by working with customers

### 5.2 Six Pillars of the AWS Well-Architected Framework

1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

### 5.3 Security Pillar — Breakdown

| Category | Services |
|---|---|
| **Identity & Access Management** | AWS IAM, AWS Directory Service, AWS Organizations |
| **Detective Controls** | AWS CloudWatch, AWS Trusted Advisor |
| **Infrastructure Protection** | AWS GuardDuty, AWS WAF, AWS VPC, AWS Shield |
| **Data Protection** | AWS Macie, AWS KMS, AWS CloudHSM, AWS Elastic Load Balancer |
| **Incident Response** | AWS CloudTrail, AWS CloudWatch Alarms, AWS SNS |
| **Application Protection** | AWS Inspector |

### 5.4 Reliability Pillar — Breakdown

| Category | Services |
|---|---|
| **Foundations** | AWS IAM, Amazon VPC, AWS Shield, AWS Trusted Advisor |
| **Change Management** | AWS CloudTrail, AWS Config, AWS CloudWatch, AWS Auto Scaling |
| **Failure Management** | AWS CloudFormation, AWS S3, AWS Glacier, AWS KMS |

---

## 6. Billing and Pricing

### 6.1 How Do You Pay for AWS?

- Pay as you go
- Save when you reserve
- Pay less by using more

**Reserved Instances:** Save up to **75%** over equivalent on-demand capacity.

**Use more, pay less:** Automatic volume-based discounts.

### 6.2 Pricing Concepts

| Category | Details |
|---|---|
| **Compute** | Charged per hour/second; varies by instance type; Linux only |
| **Storage** | Charged typically per GB |
| **Data Transfer** | Outbound is aggregated and charged; inbound has no charge (with some exceptions); charged typically per GB |

### 6.3 Service Pricing (categories priced individually)

Compute · Storage · Database · Migration & Transfer · Networking & Content Delivery · Developer Tools · Management and Governance · Media Services · Security, Identity & Compliance · Analytics · Machine Learning · Mobile Services · AR & VR · Application Integration · Customer Engagement · Business Applications · End User Computing · Internet of Things · Game Development · Blockchain · Robotics

### 6.4 What is Trusted Advisor?

A service providing guidance to help you:
- Reduce cost
- Increase performance
- Improve security

### 6.5 Support Plans

- Basic
- Developer
- Business
- Enterprise

---

## Quick Revision Checklist

- [ ] Can name the 3 components of AWS Global Infrastructure (Region, AZ, Edge Location)
- [ ] Can list the 4 factors for selecting a region
- [ ] Can list the 3 ways to interact with AWS
- [ ] Can explain S3 durability and the 6 storage classes
- [ ] Can differentiate Glacier retrieval options and their timing
- [ ] Can decode an EC2 instance type name (e.g. `c5.large`)
- [ ] Can list all 5 EC2 instance type categories and a use case for each
- [ ] Can differentiate SSD vs HDD EBS volume types
- [ ] Can explain VPC, subnets, and the 5-reserved-IP rule
- [ ] Can differentiate Internet Gateway vs NAT Gateway
- [ ] Can differentiate Security Groups (stateful) vs Network ACLs (stateless)
- [ ] Can differentiate Application Load Balancer (Layer 7) vs Network Load Balancer (Layer 4)
- [ ] Can differentiate RDS, Aurora, DynamoDB, Redshift, DocumentDB, Neptune
- [ ] Can list at least 5 "resources for technology support" services and their purpose
- [ ] Can differentiate Authentication vs Authorization
- [ ] Can explain IAM User vs Group vs Role
- [ ] Can differentiate AWS Shield Standard vs Advanced
- [ ] Can list the 6 pillars of the Well-Architected Framework
- [ ] Can list the 3 AWS pricing models and the 4 support plan tiers