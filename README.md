# Terraform AWS 3-Tier Infrastructure Project

## Overview

This project demonstrates how to provision a complete AWS infrastructure using Terraform. It follows Infrastructure as Code (IaC) principles to automate the creation of networking and compute resources.

---

## Features

* Custom Virtual Private Cloud (VPC)
* Public Subnet with Internet access
* Internet Gateway and Route Table configuration
* Security Group with SSH and HTTP access
* EC2 instance with automated Nginx installation
* Public IP output for accessing the web server

---

## Technologies Used

* Terraform
* AWS (EC2, VPC)
* Git & GitHub

---

## Project Structure

```id="8a3j2n"
.
├── main.tf
├── README.md
└── .gitignore
```

---

## Infrastructure Architecture

```id="g4n8s2"
Internet
   ↓
Internet Gateway
   ↓
VPC
   ↓
Public Subnet
   ↓
EC2 Instance (Nginx)
```

---

## How to Run

### 1. Clone the repository

```id="p0wq9f"
git clone https://github.com/your-username/terraform-aws-3tier-infra.git
cd terraform-aws-3tier-infra
```

### 2. Initialize Terraform

```id="0x8p2q"
terraform init
```

### 3. Preview the changes

```id="5m1n8c"
terraform plan
```

### 4. Apply configuration

```id="h2l4w7"
terraform apply
```

---

## Access the Application

After successful deployment, Terraform will output the public IP:

```id="g6s9x1"
http://<public-ip>
```

Open it in your browser to view the Nginx web server.

---

## SSH Access

```id="u7k2z3"
ssh -i my-key.pem ec2-user@<public-ip>
```

---

## Cleanup

To avoid unnecessary charges, destroy the resources:

```id="l9r3v8"
terraform destroy
```

---

## Learning Outcomes

* Understanding AWS networking (VPC, Subnet, IGW, Route Table)
* Creating infrastructure using Terraform
* Managing cloud resources efficiently
* Automating server setup using user data

---

## Author

Farsana K S
# terraform-aws-3tier-infra
