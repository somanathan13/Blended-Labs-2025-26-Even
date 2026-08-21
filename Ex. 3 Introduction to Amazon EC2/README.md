# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Soma Nathan L
* **Register Number**: 212223060267
* **Date of Submission**: 21/08/26

# Introduction to Amazon Elastic Compute Cloud (EC2)

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.


## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)


## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.



### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.


### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.


### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:


ssh -i "keyname.pem" ec2-user@<Public-IP>

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.


### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.


### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.


## Workflow (Student Explanation)

1. Access the Amazon EC2 dashboard in the AWS Management Console and explore key components such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs to understand available resources and configurations.
2. Launch an EC2 instance using Amazon Linux 2 AMI and select a free-tier eligible instance type (t2.micro). Configure essential settings including instance name, key pair for authentication, and initial security group.
3. Configure the Security Group to allow:

SSH (Port 22) from a specific IP for secure remote access

HTTP (Port 80) from anywhere for web access
This ensures controlled and secure communication with the instance.

4. Connect to the EC2 instance using SSH with the key pair. Perform basic operations like start, stop, and reboot, and observe how the instance state changes in the console.
5. Monitor the instance using the Monitoring tab to track CPU usage, network activity, and status checks. After completing the tasks, terminate the instance to prevent unnecessary costs.


## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1902" height="911" alt="Screenshot 2026-02-24 111106" src="https://github.com/user-attachments/assets/bffca923-9175-4633-bdcc-6a2a002c32a5" />


### Screenshot 2: SSH Connection to Instance

<img width="1908" height="913" alt="Screenshot 2026-02-24 112804" src="https://github.com/user-attachments/assets/b6348737-1220-4a4d-bcb7-17464f00ce52" />


### Screenshot 3: Instance Monitoring / Status

<img width="1913" height="913" alt="Screenshot 2026-02-24 113120" src="https://github.com/user-attachments/assets/ec71ca48-286f-47eb-9a69-87e41709deb6" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
