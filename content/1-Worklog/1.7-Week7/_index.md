---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Week 7 Objectives:

* Configure Amazon Route 53 DNS records and routing policies.
* Set up Amazon CloudFront CDN to speed up asset delivery.
* Secure connections with HTTPS using AWS Certificate Manager (ACM).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 4 | - Study Amazon Route 53 DNS routing policies: Simple, Weighted, Geolocation, Latency, and Failover. | 03/06/2026 | 03/06/2026 | [Amazon Route 53 Routing Policies Guide](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html) |
| 5 | - Explore Amazon CloudFront CDN concepts: Edge Locations, Caching behaviors, Origin Access Control (OAC). | 04/06/2026 | 04/06/2026 | [CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) |
| 6 | - Deploy a CloudFront Distribution sourcing from a private S3 bucket. Apply OAC bucket policies to restrict direct S3 access. | 05/06/2026 | 05/06/2026 | [S3 Origin Access Control (OAC) CloudFront Integration](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html) |
| 2 | - Provision SSL/TLS certificates via AWS Certificate Manager (ACM) and complete DNS validation checks. | 08/06/2026 | 08/06/2026 | [AWS ACM Overview Guide](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) |
| 3 | - Map a custom domain using Route 53 Alias record to CloudFront. Attach ACM HTTPS certificate to the distribution. | 09/06/2026 | 09/06/2026 | [CloudFront Custom Domain Mapping Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-custom-filenames.html) |


### Week 7 Achievements:

* Learned how CDN architectures lower global page-load latency by caching contents at Edge Locations.
* Secured user traffic end-to-end using SSL/TLS encryption certificates with ACM.
* Practiced custom domain name mapping with Route 53.
