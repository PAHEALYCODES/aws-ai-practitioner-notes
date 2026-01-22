# Day 3: AWS Core Services (Simplified)

**Exam Goal:** Understand the "backbone" of AWS: Networking, Databases, Security, and Virtual Servers.

---

## 1. AWS Networking (The "Plumbing")

### 1.1 Amazon VPC (Virtual Private Cloud)
* **The Analogy:** Think of a VPC as **your own private house** inside the massive city of AWS.
* **Definition:** A private, isolated network where you launch your resources.
* **Key Parts:**
    * **Subnets:** The **rooms** in your house (Public room = Guest room; Private room = Bedroom).
    * **Security Groups:** The **Security Guard** at the door of a specific room (Instance level).
    * **NACLs:** The **Fence** around the whole property (Subnet level).

> **💡 Exam Cheat Code:**
> * If the question says "private network" or "isolated," the answer is **VPC**.
> * **Security Groups** = Stateful (Remembers who came in).
> * **NACLs** = Stateless (Needs distinct rules for in/out).

### 1.2 Regions & Availability Zones (AZ)
* **Region:** A physical location on the map (e.g., "Northern Virginia").
* **Availability Zone (AZ):** The actual **Data Center building** inside that region.
* **Why use multiple AZs?** If one building loses power, the other one keeps working.

> **💡 Exam Cheat Code:**
> * **Multi-AZ** = High Availability (won't crash if one fails).

### 1.3 Amazon Route 53 (DNS)
* **The Analogy:** The **Phonebook** of the internet.
* **What it does:** Humans read names (`google.com`), computers read numbers (`192.168.1.1`). Route 53 translates the name to the number.
* **Bonus:** It also checks health (doesn't send users to a broken server).

---

## 2. Databases (Storing Data)

### 2.1 Amazon RDS (Relational Database Service)
* **The Analogy:** An **Excel Spreadsheet** or a traditional filing cabinet.
* **Usage:** Strict, structured data (Rows & Columns).
* **Examples:** Customer lists, Orders, Inventory.
* **Engines:** MySQL, PostgreSQL, Oracle, SQL Server.

> **💡 Exam Cheat Code:**
> * **RDS** = Structured data, SQL, Transactions (OLTP).

### 2.2 Amazon Redshift (Data Warehouse)
* **The Analogy:** A massive **Public Library Archive**.
* **Usage:** Analyzing HUGE amounts of history to find trends. NOT for quick daily edits.
* **Examples:** "What was our total sales profit over the last 10 years?"

> **💡 Exam Cheat Code:**
> * **Redshift** = Analytics, Big Data, Business Intelligence (OLAP).

---

## 3. Monitoring vs. Auditing (The "Eyes")

### 3.1 Amazon CloudWatch (Performance)
* **The Analogy:** The **Dashboard in your car**.
* **What it shows:** Speed (CPU), Fuel (Memory), Engine Temp (Errors).
* **Key Word:** **Metrics**.

### 3.2 AWS CloudTrail (History)
* **The Analogy:** A **Security Camera / CCTV**.
* **What it shows:** *Who* came in, *what* they touched, and *when* they left.
* **Key Word:** **Auditing**.

> **💡 Exam Cheat Code:**
> * **CloudWatch** = "How is it performing?" (Metrics/Alarms).
> * **CloudTrail** = "Who did it?" (User Activity/API calls).

---

## 4. Amazon EC2 (The Virtual Server)

### 4.1 What is EC2?
* **Definition:** Elastic Compute Cloud. It is just **renting a computer** in someone else's data center.
* **You choose:** The Speed (CPU), Memory (RAM), and Space (Storage).

### 4.2 Instance Types (Menu Options)

| Type | Name | Best For... |
| :--- | :--- | :--- |
| **General Purpose** | `t` or `m` series | Websites, simple apps (Balanced). |
| **Compute Optimized** | `c` series | High performance, gaming servers, number crunching. |
| **Memory Optimized** | `r` series | Big databases that need to "remember" a lot of data quickly. |

### 4.3 Pricing (How you pay)
1.  **On-Demand:** Pay by the second (No commitment). Good for short tests.
2.  **Reserved:** Sign a 1-3 year contract (Discount!). Good for steady usage.
3.  **Spot:** Bid for unused space (Super cheap, but risky—can be kicked off).

> **💡 Exam Cheat Code:**
> * **Spot Instances** = Cheapest option, but can be interrupted.

---

### 🧠 Quick Memory Match

| Service | One-Line Meaning |
| :--- | :--- |
| **VPC** | Private Network |
| **Route 53** | DNS / Phonebook |
| **RDS** | SQL / Excel Sheets |
| **Redshift** | Analytics / Big Data |
| **CloudWatch** | Metrics / Performance |
| **CloudTrail** | Auditing / Who-did-what |
| **EC2** | Virtual Computer |
