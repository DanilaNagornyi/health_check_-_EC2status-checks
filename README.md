# AWS Infrastructure Automation with Terraform 🚀

This repository contains Terraform configurations for automating infrastructure on AWS. It demonstrates different approaches to infrastructure provisioning, ranging from basic EC2 instances to managed Kubernetes clusters (EKS).

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)

## 🌿 Branches Overview

The project is organized into three main branches, each representing a specific automation scenario:

### 1. `main` (EC2 Multi-Server Automation)
The default branch featuring:
- Custom VPC, Subnet, and Security Group configuration.
- Deployment of **three** EC2 instances (Amazon Linux).
- Automated software installation via `user_data` (entry scripts).
- Dynamic AMI lookup and SSH key pair management.

### 2. `feature/starting-code` (Basic EC2 Automation)
Ideal for learning the basics:
- Similar to `main`, but focuses on a single EC2 instance setup.
- Demonstrates how to use Terraform to provision a web server environment with custom networking.

### 3. `feature/eks` (Managed Kubernetes Cluster)
Advanced infrastructure as code (IaC) using Terraform modules:
- Uses official `terraform-aws-modules/vpc/aws` for complex networking.
- Provisions an **Elastic Kubernetes Service (EKS)** cluster using `terraform-aws-modules/eks/aws`.
- Configured with private subnets, NAT Gateways, and managed node groups.

---

## 🛠️ Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed.
- [AWS CLI](https://aws.amazon.com/cli/) configured with appropriate credentials.
- An existing SSH public key (default path usually `~/.ssh/id_rsa.pub`).

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd terraform
   ```

2. **Switch to your desired branch:**
   ```bash
   git checkout <branch-name>
   ```

3. **Initialize Terraform:**
   ```bash
   terraform init
   ```

4. **Review the execution plan:**
   ```bash
   terraform plan
   ```

5. **Apply the configuration:**
   ```bash
   terraform apply
   ```

---
*Note: Ensure you update `terraform.tfvars` with your specific values (e.g., `my_ip`, `public_key_location`) before applying.*
