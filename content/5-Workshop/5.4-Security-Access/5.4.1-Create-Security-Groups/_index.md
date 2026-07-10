---
title: "5.4.1 Security Groups Creation"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.4.1. Security Groups Creation

1. **ALB Security Group** (`ResumeMatching-ALB-SG`): Open HTTP (`80`) and HTTPS (`443`) ports to `0.0.0.0/0`.
   ![Create ALB Security Group](/images/5-Workshop/Tao_ALB_Security_Group.jpg)

2. **Backend Security Group** (`ResumeMatching-Backend-SG`): Allow HTTP traffic on TCP, restricted to source matching `ResumeMatching-ALB-SG`.
   ![Create Backend Security Group](/images/5-Workshop/Tao_Backend_Security_Group.jpg)

3. **Worker Security Group** (`ResumeMatching-Worker-SG`): Restricts incoming/outgoing traffic to the background queue worker instance.
   ![Create Worker Security Group](/images/5-Workshop/T%E1%BA%A1o_Worker_Security_Group.jpg)

4. **Database Security Group** (`ResumeMatching-RDS-SG`): Open PostgreSQL port `5432` restricted to incoming connections originating from Backend and Worker Security Groups.
   ![Create Database Security Group](/images/5-Workshop/Tao_Database_Security_Group.jpg)
