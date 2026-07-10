---
title: "5.8.2 Auto Scaling Group (ASG) Provisioning"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.8.2. Auto Scaling Group (ASG) Provisioning

1. Create a new Auto Scaling Group named `ResumeMatching-ASG` utilizing launch template `ResumeMatching-LT`.
   ![Create ASG](/images/5-Workshop/Tao_ASG.jpg)

2. Set the Desired capacity to `2`. The ASG will automatically scale out EC2 instances to meet application demands and provide high availability.
   ![ASG scales out instances](/images/5-Workshop/ASG_tao_them_EC2.jpg)
