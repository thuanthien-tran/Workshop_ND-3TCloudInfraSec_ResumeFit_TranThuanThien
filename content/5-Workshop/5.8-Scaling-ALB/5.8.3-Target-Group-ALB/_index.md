---
title: "5.8.3 Target Group and Load Balancer Setup"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.8.3. Target Group and Load Balancer Setup

1. Create a new **Target Group** named `ResumeMatching-TG` choosing target type `Instance` routing HTTP requests on port `8080`.
   ![Create Target Group](/images/5-Workshop/Tao_target_group.jpg)

2. Create an **Application Load Balancer (ALB)** named `ResumeMatching-ALB`. Configure it as an `Internet-facing` scheme, select two Availability Zones, and route traffic to the registered target group.
   ![Create Load Balancer](/images/5-Workshop/Tao_ALB.jpg)
