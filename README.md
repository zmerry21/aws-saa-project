# aws-saa-project
My test SAA 2 tier project
# AWS 2-Tier Architecture (SAA Practice Project)

## Overview

This project demonstrates a simple 2-tier architecture:

Tier 1: Web/Application Layer (PHP on EC2)
Tier 2: Database Layer (MySQL on RDS or EC2)

The goal is to understand secure communication between layers in AWS.

---

## Architecture Diagram

User → Internet → EC2 (Public Subnet) → RDS (Private Subnet)

Security Groups:
- Web SG: Allows HTTP (80), HTTPS (443), SSH (22)
- DB SG: Allows MySQL (3306) only from Web SG

## Deployment Steps

### Step 1: Create VPC
- Create 2 subnets:
  - Public subnet (Web server)
  - Private subnet (Database)

### Step 2: Launch EC2 Instance
- Install:
  - Apache
  - PHP
- Place in Public Subnet

### Step 3: Create RDS MySQL Database
- Place in Private Subnet
- Disable public access
- Allow inbound from Web Security Group

### Step 4: Configure index.php
- Update database endpoint
- Place file in:
  /var/www/html/

### Step 5: Test Application
- Access via browser:
  http://3.94.214.107/index.php

---
