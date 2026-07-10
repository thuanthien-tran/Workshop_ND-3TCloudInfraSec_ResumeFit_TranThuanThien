---
title: "5.11. Clean Up Resources"
date: 2024-01-01
weight: 11
chapter: false
---

## 5.11. Clean Up Resources

After completing evaluations, clean up the resources to avoid active AWS subscription bills:

1. Delete the Auto Scaling Group, then terminate running EC2 instances.
2. Delete the Application Load Balancer and its Target Group.
3. Delete the RDS database instance (skip final snapshot creation) and delete the DB subnet group.
4. Delete the NAT Gateways. Once deleted, release the allocated Elastic IPs.
5. Delete VPC endpoints, route tables, subnets, and the main VPC.
6. Empty all S3 bucket files, and delete the bucket.
