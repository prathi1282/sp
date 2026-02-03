# AWS EC2 Deployment – Manual & Terraform

## Objective
The objective of this task is to understand AWS core concepts, manually launch an EC2 instance using the AWS Management Console, and provision an EC2 instance using Terraform. The entire process is documented as part of this repository.

---

## AWS Core Concepts

### AWS (Amazon Web Services)
A cloud service provider offering scalable compute, storage, and networking services.

### EC2 (Elastic Compute Cloud)
A service that provides resizable virtual servers in the cloud.

### AMI (Amazon Machine Image)
A preconfigured image containing the operating system and required software to launch an EC2 instance.

### IAM (Identity and Access Management)
Manages users, permissions, and access to AWS services securely.

### Security Group
Acts as a virtual firewall that controls inbound and outbound traffic for EC2 instances.

### Region and Availability Zone
- **Region:** A geographical location where AWS data centers are hosted.
- **Availability Zone:** Isolated data centers within a region.

---

## Part 1: Launching EC2 Instance Manually (AWS Console)

### Steps Followed
1. Logged into the AWS Management Console
2. Navigated to EC2 service
3. Clicked on *Launch Instance*
4. Selected **Amazon Linux 2** AMI
5. Chose **t2.micro** instance type (Free Tier eligible)
6. Created a new key pair for SSH access
7. Configured security group:
   - SSH (Port 22) – My IP
   - HTTP (Port 80) – Anywhere
8. Launched the EC2 instance

### Outcome
- EC2 instance was successfully created
- Instance entered the *Running* state
- Public IP address was assigned
- Instance was accessible via SSH

---

## Part 2: Provisioning EC2 Instance Using Terraform

### Tools Used
- Terraform
- AWS CLI
- IAM User with EC2 permissions

### Terraform Configuration
The infrastructure was defined using Terraform configuration files to automate EC2 instance creation.

### Commands Executed
```bash
terraform init
terraform plan
terraform apply

Outcome

EC2 instance was provisioned automatically using Terraform

Public IP address was generated and displayed as output

Infrastructure was reproducible and manageable as code

Conclusion

This task provided hands-on experience with AWS EC2, IAM, and Infrastructure as Code using Terraform. Manual EC2 creation helped understand the AWS Console workflow, while Terraform demonstrated how infrastructure can be automated and version-controlled efficiently.
