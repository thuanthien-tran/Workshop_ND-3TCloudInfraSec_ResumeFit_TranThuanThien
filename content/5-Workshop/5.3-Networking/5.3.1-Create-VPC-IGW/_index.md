---
title: "5.3.1 Create VPC and Internet Gateway"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.3.1. Create VPC and Internet Gateway

1. Navigate to the VPC Console, click **Create VPC**. Name your VPC `ResumeMatching-VPC` and configure CIDR block `10.0.0.0/16`.
   ![Create VPC](/images/5-Workshop/tao_VPC.jpg)

2. Enable DNS Hostnames on the VPC to resolve private AWS domains.
   ![Enable DNS Hostnames](/images/5-Workshop/Enable_DNS_Hostnames.jpg)

3. Create an Internet Gateway named `ResumeMatching-IGW` to provide inbound/outbound connectivity to public-facing resources.
   ![Create Internet Gateway](/images/5-Workshop/Tao_Internet_Gateway.jpg)

4. Attach the Internet Gateway to your newly created VPC (`ResumeMatching-VPC`).
   ![Attach Internet Gateway to VPC](/images/5-Workshop/Attach_vao_VPC.jpg)
