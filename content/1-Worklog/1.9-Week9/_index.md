---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Week 9 Objectives:

* Protect applications from web threats using AWS WAF.
* Understand DDoS mitigation layers using AWS Shield.
* Securely manage system credentials using AWS Secrets Manager and Systems Manager Parameter Store.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 4 | - Study application vulnerabilities (SQLi, XSS) and how AWS WAF filters web requests based on rules. | 17/06/2026 | 17/06/2026 | [AWS WAF Guide Docs](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html) |
| 5 | - Create Web ACLs. Practice applying rate-limiting rules and block malicious IP address ranges. | 18/06/2026 | 18/06/2026 | [AWS WAF Web ACLs Guide](https://docs.aws.amazon.com/waf/latest/developerguide/web-acl.html) |
| 6 | - Learn about AWS Shield Standard and Advanced configurations for Layer 3/4 and Layer 7 DDoS mitigation. | 19/06/2026 | 19/06/2026 | [AWS Shield DDoS Info](https://aws.amazon.com/shield/) |
| 2 | - Study AWS Secrets Manager and Systems Manager (SSM) Parameter Store. Contrast their features (cost, rotation). | 22/06/2026 | 22/06/2026 | [AWS Secrets Manager Guide](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) |
| 3 | - Store a dummy database password in Secrets Manager. Write a script retrieving the password dynamically during runtime. | 23/06/2026 | 23/06/2026 | [Retrieving Secrets dynamically with Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/retrieving-secrets.html) |


### Week 9 Achievements:

* Protected exposed Application Load Balancers or CloudFront origins with customized firewall policies.
* Understood automated defense mechanisms against infrastructure and application DDoS attempts.
* Eliminated cleartext database credentials from code files to satisfy security audits.
