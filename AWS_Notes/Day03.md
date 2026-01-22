


# Day 3 Notes
Day 3 – AWS Core Services (Deep Exam Notes)

Exam Goal:
Understand how AWS infrastructure, networking, databases, monitoring, and EC2 work together.

1. AWS Networking (VERY IMPORTANT)
1.1 Amazon VPC (Virtual Private Cloud)

Definition (Exam-Safe):
Amazon VPC lets you create a private, isolated network inside AWS where you launch resources like EC2, RDS, and Lambda.

Think of VPC as:

“My own data center inside AWS”

What You Control Inside a VPC
Component	Meaning
IP Range (CIDR)	Defines size of your network
Subnets	Divide VPC into smaller networks
Route Tables	Control traffic direction
Security Groups	Firewall for instances
NACLs	Firewall for subnets
Why VPC Is Needed

Security (private network)

Traffic control

Isolation of workloads

Hybrid cloud (AWS + on-premise)

Without VPC:
Resources would be exposed to the internet.

Exam Tip 📝

If question mentions private networking, isolation, IP control → VPC

1.2 AWS Regions & Availability Zones (Quick Recap)
Region

Physical geographic location

Example: us-east-1, eu-west-1

Independent from other regions

Availability Zone (AZ)

One or more data centers

Separate power, cooling, networking

Connected with low latency

Why AZs exist:
High availability & fault tolerance

Exam Tip 📝

Deploy across multiple AZs for high availability

1.3 Amazon Route 53 (DNS)

Definition:
Amazon Route 53 is a highly available DNS service.

DNS = Domain Name → IP Address

What Route 53 Does

Routes users to correct server

Performs health checks

Supports failover

Load balancing across regions

Example

If example.com server in one region fails →
Route 53 redirects traffic to backup region.

Exam Tip 📝

Route 53 = DNS + Traffic routing + Failover

2. AWS Database Services
2.1 Amazon RDS (Relational Database Service)

Definition:
Amazon RDS is a managed relational database service.

You do NOT manage:

OS

Patching

Backups

Scaling

AWS manages everything.

Supported Databases

MySQL

PostgreSQL

MariaDB

Oracle

SQL Server

When to Use RDS

Structured data

SQL queries

Transactions

Banking apps

E-commerce apps

Exam Tip 📝

RDS = SQL + Structured data + Managed

2.2 Amazon Redshift (Data Warehouse)

Definition:
Amazon Redshift is used for analytics on huge datasets.

Key Differences (Exam Favorite)
RDS	Redshift
Transactions	Analytics
Small-medium data	Very large data
Row-based	Column-based
OLTP	OLAP
Use Cases

Business intelligence

Reporting

Fraud detection

Predictive analytics

Exam Tip 📝

Redshift = Data analytics, NOT daily transactions

3. Monitoring & Security
3.1 Amazon CloudWatch

Definition:
CloudWatch monitors AWS resources and applications.

What CloudWatch Collects

Metrics (CPU, memory, disk)

Logs

Events

What You Use It For

Monitor EC2 health

Trigger Auto Scaling

Create alarms

Debug performance issues

Exam Tip 📝

CloudWatch = Monitoring + Metrics + Logs

3.2 AWS CloudTrail

Definition:
CloudTrail records all API calls made in AWS.

What It Tracks

Who accessed AWS

What action was taken

When it happened

From where

Used For

Security audits

Compliance

Threat detection

Exam Tip 📝

CloudTrail = “Who did what in AWS”

4. Amazon EC2 (MOST IMPORTANT)
4.1 What is EC2?

Definition:
Amazon EC2 provides resizable virtual machines in the cloud.

EC2 Instance = Virtual server

EC2 Includes

CPU

RAM

Storage

Network

4.2 How EC2 Works (Simple)

Physical server

Hypervisor enables virtualization

Multiple EC2 instances run on one host

4.3 EC2 Instance Types
Type	Use Case
General Purpose	Balanced workloads
Compute Optimized	CPU-heavy apps
Memory Optimized	Big memory apps
Storage Optimized	Large storage
Accelerated	ML, GPUs
Exam Tip 📝

Choose instance family based on workload

4.4 EC2 Storage

Temporary storage → Lost when instance stops

EBS (Elastic Block Store) → Persistent storage

4.5 EC2 Security

Security Groups → Instance-level firewall

NACLs → Subnet-level firewall

4.6 EC2 Pricing

Pay-as-you-go

Linux → per second

Windows → per hour

Free tier:

t2.micro / t3.micro

750 hours/month

Exam Tip 📝

Free tier is limited but real

4.7 EC2 Advanced Features
User Data

Startup scripts

Install software automatically

AMI (Amazon Machine Image)

Blueprint of EC2

Used to launch identical servers

Placement Groups

Low latency

High performance

HPC workloads

5. When to Use EC2 (Exam Logic)

Use EC2 when you need:

Full OS control

Custom software

Long-running workloads

Predictable performance

FINAL EXAM MEMORY MAP 🧠
Service	One-Line Meaning
VPC	Private network
Route 53	DNS & routing
RDS	Managed SQL
Redshift	Analytics
CloudWatch	Monitoring
CloudTrail	Auditing
EC2	Virtual machines

