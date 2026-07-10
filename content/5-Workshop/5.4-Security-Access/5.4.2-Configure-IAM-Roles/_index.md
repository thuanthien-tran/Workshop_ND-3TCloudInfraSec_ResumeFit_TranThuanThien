---
title: "5.4.2 IAM Roles Configuration"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.4.2. IAM Roles Configuration

1. In the **IAM** Console, create a role named `ResumeMatching-Backend-Role` to bind to the Backend EC2 instances.
   ![Create Backend IAM Role](/images/5-Workshop/Tao_Backend_IAM_Role.jpg)

2. Create a second role named `ResumeMatching-Worker-Role` for the queue worker. Attach standard managed policies like `AmazonSQSFullAccess` and S3 bucket write/read access.
   ![Create Worker IAM Role](/images/5-Workshop/Tao_Worker_IAM_Role.jpg)
