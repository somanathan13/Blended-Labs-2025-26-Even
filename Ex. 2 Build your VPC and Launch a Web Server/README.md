# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Soma Nathan L
* **Register Number**: 212223060267
* **Date of Submission**: 

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1. Created a VPC named lab-vpc in the us-east-1 region with a 10.0.0.0/16 CIDR block, along with public and private subnets, an Internet Gateway, NAT Gateway, and route tables.
2. Created additional public and private subnets in a second Availability Zone and configured the route table associations so that public subnets used the Internet Gateway and private subnets used the NAT Gateway.
3. Created a security group named Web Security Group and configured an inbound HTTP rule to allow web requests from anywhere over IPv4.
4. Launched an EC2 instance named Web Server 1 using Amazon Linux 2023 and t2.micro, placed it in the lab-subnet-public2 subnet, enabled a public IP, and attached the Web Security Group.
5. Added the user-data script to install and start the Apache web server, accessed the instance through its Public IPv4 DNS, verified the website and instance metadata, and submitted the lab successfully with a score of 30/30.

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/c09f5733-2286-4fdb-a6ca-dc682e07da6f" />


---

### Screenshot 2: EC2 Instance Running

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/3e55f808-24d0-4a0e-b55a-5431015ccdb2" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/4bb13184-41df-4109-927e-39d60d7495c7" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
