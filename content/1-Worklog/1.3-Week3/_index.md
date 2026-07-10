---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Understand virtual networking fundamentals in AWS.
* Create a custom Virtual Private Cloud (VPC) with Public and Private subnets.
* Configure Internet Gateways, NAT Gateways, and Route Tables.
* Establish network security using Security Groups and Network ACLs (NACLs).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 4 | - Learn AWS VPC architecture, CIDR block allocation, and subnets definition. | 06/05/2026 | 06/05/2026 | [How Amazon VPC Works](https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html) |
| 5 | - Create a custom VPC. Set up Public and Private Subnets across different Availability Zones for high availability. | 07/05/2026 | 07/05/2026 | [VPC & Subnets Guide](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) |
| 6 | - Configure Internet Gateway (IGW) for public routing and NAT Gateway for private instances outbound internet access. | 08/05/2026 | 08/05/2026 | [NAT Gateway Setup Docs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html) |
| 2 | - Define Route Tables for both subnets. Associate routes to guide traffic through IGW or NAT Gateway. | 11/05/2026 | 11/05/2026 | [Route Tables Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) |
| 3 | - Study and configure stateful Security Groups and stateless Network ACLs (NACLs). Verify network connectivity using ping/curl between resources. | 12/05/2026 | 12/05/2026 | [Security Groups in VPC Guide](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) |


### Week 3 Achievements:

* Successfully designed and implemented a custom virtual network infrastructure on AWS.
* Gained experience in isolating database instances in private subnets while hosting web services in public subnets.
* Demonstrated configuration of network access controls at both instance level (Security Groups) and subnet level (NACLs).
