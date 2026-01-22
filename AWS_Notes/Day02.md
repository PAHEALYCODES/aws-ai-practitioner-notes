


# Day 2 – AWS AI Practitioner  
# AWS Global Infrastructure & Core Services

## Focus
- AWS Global Infrastructure
- Core AWS Services (Compute & Storage)
- Foundation knowledge for AWS Certified AI Practitioner (AIF-C01)

---

## 1. AWS Global Infrastructure (Beginner Friendly)

AWS Global Infrastructure is the **backbone of AWS**.  
It allows applications to be **fast, secure, scalable, and highly available** across the world.

### Simple Analogy
Think of AWS like a **global restaurant chain**:
- **Regions** = Cities
- **Availability Zones** = Separate kitchens in one city
- **Edge Locations** = Delivery centers close to customers
- **Local Zones** = Pop-up kitchens for ultra-fast service

If one kitchen fails, others keep serving customers.

---

## 2. AWS Region

### Definition
An **AWS Region** is a **geographical area** where AWS has multiple data centers.

### Key Points
- Each region is **independent**
- Businesses choose regions based on:
  - Low latency (closer to users)
  - Compliance & laws
  - Disaster recovery

### Example
If your users are in Europe, hosting your application in a **European AWS Region** gives faster performance.

---

## 3. Availability Zones (AZ)

### Definition
An **Availability Zone (AZ)** is a **physically separate data center** within an AWS Region.

### Key Characteristics
- Separate power, cooling, and networking
- Connected with **low-latency, high-speed links**
- Designed for **fault tolerance**

### Why AZs Matter
- Applications can run in **multiple AZs**
- If one AZ fails, others keep running

### Exam Tip 📝
> High Availability = **Multiple AZs inside one Region**

---

## 4. What If an Entire Region Goes Down?

### Possible Impact
- Applications become unavailable
- Business downtime
- Possible data loss if no backups

### AWS Best Practices
- **Multi-Region deployment**
- **Cross-region data replication**
- **Disaster recovery planning**

### Example
Netflix uses **multiple AWS regions** to ensure uninterrupted streaming.

---

## 5. Edge Locations

### Definition
Edge locations are AWS sites that **cache and deliver data closer to users**.

### Used By
- Amazon CloudFront (CDN)

### Purpose
- Faster content delivery
- Lower latency
- Better user experience

### Example
Streaming videos, images, and websites load faster worldwide.

---

## 6. AWS Local Zones

### Definition
Local Zones bring AWS services **closer to specific cities**.

### Used For
- Gaming
- Live streaming
- Real-time analytics
- Media processing

### Benefit
- **Ultra-low latency** without needing a full AWS Region

---

## 7. Why AWS Global Infrastructure Is Important

AWS infrastructure helps achieve:
- High availability
- Fault tolerance
- Scalability
- Global performance

### Real-World Use
- Replicate apps across regions
- Distribute workloads across AZs
- Deliver content fast using edge locations

---

## 8. AWS Account Creation (Exam Awareness)

### Steps Summary
1. Sign up at aws.amazon.com
2. Verify email
3. Add personal details
4. Add debit/credit card (small verification charge, refunded)
5. Identity verification
6. Choose **Basic Support (Free)**
7. Access AWS Management Console

### Important
✅ AWS Free Tier allows hands-on practice  
❌ Avoid paid support plans

---

## 9. Core AWS Services Overview

Before AI services, understand **core cloud services**.

AWS services are grouped into:
- Compute
- Storage
- Networking
- Databases
- Monitoring & Security

---

## 10. Compute Services

### Amazon EC2 (Elastic Compute Cloud)

**What it is:**  
Virtual machines in the cloud.

**Key Features**
- Full control over OS
- Choose CPU, RAM, storage
- Used for long-running workloads

**Example**
Hosting a website or backend server.

---

### AWS Lambda (Serverless)

**What it is:**  
Run code **without managing servers**.

**Key Features**
- Event-driven
- Auto-scaling
- Pay only when code runs

**Example**
Image processing, API backends, automation scripts.

### Exam Tip 📝
> EC2 = Server-based  
> Lambda = Serverless

---

## 11. Storage Services

### Amazon S3 (Simple Storage Service)

**What it is:**  
Object storage for unlimited data.

**Used For**
- Images, videos
- Backups
- Logs
- Static websites

**Key Strength**
- Extremely durable (99.999999999%)

### Simple Analogy
S3 = **Unlimited cloud hard drive**

---

### Amazon EBS (Elastic Block Store)

**What it is:**  
Block storage attached to EC2 instances.

**Key Points**
- Data persists even if EC2 stops
- High performance
- Used for databases

### Example
Database storage, application data.

---

### Amazon EFS (Elastic File System)

**What it is:**  
Shared file storage for multiple EC2 instances.

**Key Features**
- Multiple servers can access same files
- Auto-scales storage
- Used for ML training & web servers

### Difference Summary
| Service | Used With | Purpose |
|------|--------|--------|
| S3 | Any | Object storage |
| EBS | Single EC2 | Block storage |
| EFS | Multiple EC2 | Shared file system |

---

## 12. Exam-Focused Takeaways (VERY IMPORTANT)

- Region = Geographic location
- AZ = Fault tolerance inside a region
- Multi-AZ = High availability
- Multi-Region = Disaster recovery
- S3 = Object storage
- EC2 = Virtual servers
- Lambda = Serverless compute

---

## Beginner Summary

Today you learned:
- How AWS infrastructure works globally
- Why regions and AZs matter
- Core compute & storage services
- Foundation needed before AWS AI services

This knowledge is **mandatory** for passing the AWS AI Practitioner exam.
