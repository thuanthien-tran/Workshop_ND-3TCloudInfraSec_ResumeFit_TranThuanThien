---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# AI Resume Matching & Interview Preparation Platform

### 1. Project Overview

*   **Goal:** Web application evaluating the fit between CVs and JDs based on a standard 3-Tier AWS cloud infrastructure.
*   **AI Processing:** An EC2 cluster (Backend + Worker) analyzes CVs and JDs by invoking OpenAI APIs over the Internet to optimize token consumption and save costs.

---

### 2. Cloud Infrastructure Architecture (AWS)

#### Border & Global Layer:
*   Content Delivery Network (CloudFront), WAF firewall, and authentication services are currently in a planned state (*Planned but not deployed - AWS account verification required*), they are not active services yet.
*   Amazon S3 (Amazon Simple Storage Service) is used for general storage.
*   Users interact via the Internet Gateway (1) or "upload via Pre-signed URL" directly to a dedicated S3 storage (*S3 CV/JD Storage*) (5).

#### Network & Load Balancing (Inbound):
*   A VPC with CIDR block 10.0.0.0/16 is used as the foundation.
*   Internet Gateway (IGW) acts as the single gateway connecting to the Internet for both inbound and outbound traffic (via NAT Gateway).
*   Application Load Balancer (ALB) is deployed across Availability Zones to receive traffic from the IGW and distribute it to the Auto Scaling Group.

#### Application Layer:
*   EC2 cluster (Backend + Worker) is placed in private app subnets (*Private App Subnet A* and *Private App Subnet B*), spanning two Availability Zones (AZ A and AZ B), and is managed by an Auto Scaling Group (ASG) to scale dynamically based on demand.
*   Internal Communication: EC2 (AZ A) connects to the S3 storage service and SQS (6), followed by a Dead Letter Queue (DLQ).
*   OpenAI API Flow: EC2 (AZ B) communicates outwards through the NAT Gateway in Public Subnet B to access the Internet Gateway.

#### Outbound & Internal Network:
*   Features **two NAT Gateways**, one in Public Subnet A and another in Public Subnet B, ensuring High Availability (HA) for outbound traffic from the Private Subnets.
*   Communication to SQS and S3 is handled over the network, without utilizing VPC Endpoints in the current layout.

#### Database Layer:
*   Uses Amazon RDS PostgreSQL configured in Multi-AZ mode.
*   Contains two Private DB Subnets (*Private DB Subnet A* and *Private DB Subnet B*) protected by a Security Group.
*   RDS Primary (Master) is located in AZ A. RDS Standby Replica is located in AZ B with real-time synchronous replication (dashed line).
*   Connection Flow: EC2 in AZ A connects directly to RDS Primary (7). EC2 in AZ B connects to RDS Standby Replica via RDS Endpoints (dashed line).

#### Management & Monitoring:
*   A Security & Management cluster (*Vùng Bảo mật & Quản lý*) includes AWS Systems Manager, Amazon CloudWatch (logs), and AWS Secrets Manager (API Key).

#### Deployment:
*   Source code repository hosted on GitHub (*Manual Deployment*). Automations such as AWS CodeBuild or AWS CodePipeline are not implemented in the current design.

---

### System Architecture Diagram

![AI Resume Matching & Interview Preparation Platform Architecture](/images/2-Proposal/ai_resume_matching_architecture.png)