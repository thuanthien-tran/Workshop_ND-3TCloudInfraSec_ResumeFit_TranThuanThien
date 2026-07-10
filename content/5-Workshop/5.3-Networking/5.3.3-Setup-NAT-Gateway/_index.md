---
title: "5.3.3 Provision NAT Gateways for Private Subnets"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.3.3. Provision NAT Gateways for Private Subnets

1. Allocate two static Elastic IPs named `ResumeMatching-EIP` and `ResumeMatching-EIP-B`.
   ![Allocate Elastic IP](/images/5-Workshop/Tao_Elastic_IP.jpg)
   ![Allocate Elastic IP B](/images/5-Workshop/Tao_Elastic_IP_B%20%28ph%C3%ADa%20sau%20b%C6%B0%E1%BB%9Bc%20t%E1%BA%A1o%20Elastic%20IP%29.jpg)

2. Provision the first **NAT Gateway** named `ResumeMatching-NAT` inside `Public-Subnet-A` and associate it with the first Elastic IP.
   ![Create NAT](/images/5-Workshop/Tao_NAT.jpg)

3. Provision the second **NAT Gateway** named `ResumeMatching-NAT-B` inside `Public-Subnet-B` and associate it with the second Elastic IP to ensure Availability Zone redundancy (High Availability).
   ![Create NAT B](/images/5-Workshop/Tao_NAT_B%20%28b%C6%B0%E1%BB%9Bc%20n%C3%A0y%20ph%C3%ADa%20sau%20b%C6%B0%E1%BB%9Bc%20t%E1%BA%A1o%20NAT%29.jpg)
