---
title: "5.11. Clean Up & Cost"
date: 2024-01-01
weight: 11
chapter: false
---

## 5.11. Clean Up & Cost

After completing evaluations, clean up the resources to avoid active AWS subscription bills:

1. Delete the Auto Scaling Group, then terminate running EC2 instances.
2. Delete the Application Load Balancer and its Target Group.
3. Delete the RDS database instance (skip final snapshot creation) and delete the DB subnet group.
4. Delete the NAT Gateways. Once deleted, release the allocated Elastic IPs.
5. Delete VPC endpoints, route tables, subnets, and the main VPC.
6. Empty all S3 bucket files, and delete the bucket.

## 3. Cost Breakdown

The following estimate is prepared in the style of an AWS cost report, using **AWS Pricing Calculator** assumptions for **US East (N. Virginia) - us-east-1**, **On-Demand pricing**, and **730 hours/month**.

| STT | AWS Service | Configuration | Quantity | Estimated Monthly Cost (USD) | Notes | Total (USD) |
|---|---|---|---:|---:|---|---:|
| 1 | Amazon VPC | 01 VPC, 02 public subnets, 02 private application subnets, 02 private database subnets, 01 Internet Gateway, route tables, and Security Groups | 1 set | 0.000 | Network foundation only; no direct hourly charge | 0.000 |
| 2 | Internet Gateway | 01 Internet Gateway attached to the VPC | 1 | 0.000 | No direct charge | 0.000 |
| 3 | Public / Private Subnets | 06 subnets in total | 6 | 0.000 | No direct charge | 0.000 |
| 4 | Security Group | Security rules for EC2, ALB, and RDS access control | 1 set | 0.000 | No direct charge | 0.000 |
| 5 | NAT Gateway | 02 NAT Gateways in us-east-1 | 2 | 32.963 | Approx. USD 0.045/hour per NAT Gateway x 730 hours + low data processing | 65.925 |
| 6 | Amazon EC2 | t3.micro Linux instance for backend | 3 | 7.592 | Approx. USD 0.0104/hour per instance x 730 hours | 22.776 |
| 7 | Amazon EBS | gp3, 30 GB per EC2 instance | 3 volumes | 2.400 | 30 GB x 3 instances x USD 0.08/GB-month | 7.200 |
| 8 | Amazon Machine Image (AMI) | AMI snapshot storage for one 30 GB image | 1 | 1.500 | Snapshot-based AMI storage estimate | 1.500 |
| 9 | Launch Template | EC2 launch template for Auto Scaling deployment | 1 | 0.000 | Configuration object only | 0.000 |
| 10 | Auto Scaling Group | 02 instances in ASG | 1 set | 0.000 | Management layer only; EC2 cost is counted separately | 0.000 |
| 11 | Application Load Balancer | 01 ALB in us-east-1 | 1 | 22.265 | Approx. USD 0.0225/hour + light LCU usage | 22.265 |
| 12 | Target Group | 01 target group for ALB forwarding | 1 | 0.000 | No direct charge | 0.000 |
| 13 | Amazon RDS | db.t3.micro, Single-AZ, PostgreSQL, 20 GB gp3 storage | 1 | 15.440 | Approx. USD 0.018/hour + 20 GB storage | 15.440 |
| 14 | Amazon S3 | Standard storage, approximately 5 GB | 1 bucket | 0.115 | Storage only; request volume is assumed minimal | 0.115 |
| 15 | Amazon SQS | Standard Queue + DLQ | 2 queues | 0.000 | Low demo traffic remains within free tier threshold | 0.000 |
| 16 | AWS Secrets Manager | 01 secret | 1 | 0.400 | USD 0.40 per secret-month | 0.400 |
| 17 | Amazon Cognito | User authentication below 50,000 MAU | 1 user pool | 0.000 | Demo usage assumed to remain within free tier | 0.000 |
| 18 | AWS Systems Manager | Session Manager for instance access | 1 | 0.000 | No direct charge for Session Manager usage | 0.000 |
| 19 | Amazon CloudWatch | Basic metrics and logs | 1 set | 0.530 | Light log ingestion and retention for demo monitoring | 0.530 |

**Total estimated monthly cost:** **USD 136.151**

### Cost analysis

- **Highest-cost service:** NAT Gateway, with an estimated monthly cost of **USD 65.925**, accounting for approximately **48.42%** of the total monthly cost.
- **Other significant cost drivers:** Application Load Balancer (**USD 22.265**) and EC2 instances (**USD 22.776** combined) are the next largest components.
- **AWS Credits assessment:** The estimated monthly cost is **below the USD 200 AWS Credits limit**. Therefore, the current architecture is financially feasible for the demo and thesis defense scope.

### Cost optimization recommendations

1. **Reduce NAT Gateway usage** where possible, because it is the dominant cost component.
2. **Delete non-production resources immediately** after evaluation, especially NAT Gateways, RDS, and ALB.
3. **Use the smallest suitable instance type** already adopted in the current design, and avoid unnecessary scaling beyond the demo requirement.
4. **Apply short log retention in CloudWatch** and keep S3 storage limited to essential artifacts only.
5. **Preserve the current architecture** but schedule cleanup promptly after each demonstration session to avoid idle charges.
