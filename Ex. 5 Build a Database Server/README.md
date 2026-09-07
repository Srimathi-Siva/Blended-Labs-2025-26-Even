# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: SRI MATHI S
* **Register Number**: 212224230272
* **Date of Submission**: 07/09/2026

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1.First, a security group named DB Security Group was created to allow the web server to connect to the database using port 3306 (MySQL).

2.A DB Subnet Group was created with subnets from two Availability Zones to allow the database to run in a Multi-AZ environment for high availability.

3.A MySQL RDS instance named lab-db was created with the database name lab, username main, and password lab-password.

4.The database was associated with the DB Security Group and the Lab VPC so that the web server can securely connect to the database.

5.The web application running on the EC2 server was opened using its IP address, and the RDS endpoint, database name, username, and password were entered to interact with the database.


## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1008" height="507" alt="Screenshot 2026-08-22 095230" src="https://github.com/user-attachments/assets/15523392-519d-4414-96c9-5a8800d0d5f1" />

### Screenshot 2: Database Service Running

<img width="1004" height="491" alt="Screenshot 2026-08-22 095259" src="https://github.com/user-attachments/assets/48c5a271-ca4e-4f46-9d8b-bb69a570005d" />


### Screenshot 3: Sample Database and Table

<img width="834" height="453" alt="Screenshot 2026-08-22 095341" src="https://github.com/user-attachments/assets/ffbed517-af9b-4313-add4-217d96a12727" />


## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
