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
