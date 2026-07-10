---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:

* Master Infrastructure as Code (IaC) design principles.
* Write modular CloudFormation templates in YAML/JSON.
* Create, update, and manage CloudFormation stacks via AWS Console and CLI.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 4 | - Study IaC design patterns and how AWS CloudFormation simplifies infrastructure provisioning. | 10/06/2026 | 10/06/2026 | [AWS CloudFormation Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html) |
| 5 | - Learn CloudFormation block syntax including Parameters, Resources, Properties, Mappings, and Outputs. | 11/06/2026 | 11/06/2026 | [CloudFormation Template Sections Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html) |
| 6 | - Write a template deploying one EC2 instance connected to a custom Security Group. | 12/06/2026 | 12/06/2026 | [CloudFormation Template Basics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-guide.html) |
| 2 | - Deploy the CloudFormation template to create a Stack. Analyze event logs and understand rollbacks on deployment errors. | 15/06/2026 | 15/06/2026 | [AWS CloudFormation Stacks Concepts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html) |
| 3 | - Practice stack updates (changing properties) and perform stack deletion to clean up all provisioned resources automatically. | 16/06/2026 | 16/06/2026 | [AWS Stack Update Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) |


### Week 8 Achievements:

* Avoided manual click-ops on AWS Management Console by managing resources programmatically.
* Understood stack management states, event timelines, and rollback mechanisms.
* Wrote YAML deployment blueprints that are version-controllable.
