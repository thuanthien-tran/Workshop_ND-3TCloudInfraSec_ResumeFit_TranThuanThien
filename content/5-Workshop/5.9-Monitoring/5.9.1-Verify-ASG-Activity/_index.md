---
title: "5.9.1 Validate Auto Scaling Group Functionality"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.9.1. Validate Auto Scaling Group Functionality

1. Open the EC2 Console, navigate to the **Instances** list.
2. Confirm the instances named `ResumeMatching-ASG-Instance` are running across multiple AZs.
3. Legacy instances should be terminated as the ASG maintains system metrics configurations and cleans up unhealthy nodes.
   ![Verify ASG scale out](/images/5-Workshop/ASG_tao_EC2_moi_sau%20khi_cap_nhat_AMI.jpg)
