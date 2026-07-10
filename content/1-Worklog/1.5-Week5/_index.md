---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Understand high availability and fault tolerance concepts.
* Create custom AMIs for rapid server replication.
* Deploy Application Load Balancers (ALBs) to distribute incoming traffic.
* Configure Auto Scaling Groups (ASGs) to scale compute capacity dynamically.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 4 | - Study Elastic Load Balancing (ELB) architecture and difference between ALB, NLB, and GLB. | 20/05/2026 | 20/05/2026 | [AWS ELB Architecture Guide](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html) |
| 5 | - Prepare a web server EC2 instance and create a custom Amazon Machine Image (AMI) from it. | 21/05/2026 | 21/05/2026 | [Create Custom AMI Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami-ebs.html) |
| 6 | - Create and configure an Application Load Balancer (ALB). Define Target Groups and test traffic routing. | 22/05/2026 | 22/05/2026 | [Application Load Balancer Introduction](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html) |
| 2 | - Configure an Auto Scaling Group (ASG) using Launch Templates. Define scaling policies based on metric thresholds. | 25/05/2026 | 25/05/2026 | [AWS Auto Scaling Group Docs](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html) |
| 3 | - Simulate heavy load or terminate instances to test ALB health checks and ASG self-healing capabilities. | 26/05/2026 | 26/05/2026 | [EC2 Auto Scaling Groups Configuration Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html) |


### Week 5 Achievements:

* Built scalable architectures that automatically adjust compute power depending on active traffic demand.
* Implemented self-healing system components that detect and replace unhealthy server instances.
* Learned how to centralize application access points through load balancers.
