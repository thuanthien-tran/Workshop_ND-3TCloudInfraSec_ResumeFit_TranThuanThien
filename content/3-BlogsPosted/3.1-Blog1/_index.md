---
title: "Blog 1: System Monitoring on AWS"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# SYSTEM MONITORING ON AWS: STREAMING CLOUDWATCH METRICS TO VPC-BASED OPENTELEMETRY COLLECTORS USING LAMBDA

Managing observability for large-scale cloud deployments is always a challenging task, especially when trying to balance cost, flexibility, and security. Although OpenTelemetry is rapidly becoming the industry standard to prevent vendor lock-in, organizations often run into a significant technical hurdle: how to stream metrics from AWS CloudWatch directly into internal collectors isolated within a private VPC. To resolve this, using AWS Lambda as a bridging agent from CloudWatch Metric Streams to the internal network has proven highly effective, ensuring secure and real-time metrics delivery.

### HERE ARE KEY HIGHLIGHTS OF THIS PUSH-BASED OBSERVABILITY ARCHITECTURE:

*   **Transition from Pull to Push Model:** Utilizing tools like Prometheus to constantly poll data can cause API throttling, missed metrics, and increased API costs. The event-driven Push model via CloudWatch Metric Streams solves this, delivering metrics with sub-minute latency for real-time alerting.
*   **Overcoming Amazon Data Firehose Constraints:** Although Firehose supports pushing data to HTTP endpoints, they are required to be public. To route data into private subnets, AWS deploys a Lambda Transform Function as a bridge. Firehose batches the data and invokes Lambda; the function then securely pushes the metrics through a Network Load Balancer (NLB) into the VPC.
*   **OpenTelemetry Collector at the Core:** Running on Amazon EC2 instances inside the VPC, the Collector acts as the central processor with 3 flexible layers: Receivers (data ingestion), Processors (filtering, metadata enrichment, obfuscating sensitive data), and Exporters (sending data to final backends like Grafana, AWS X-Ray, or Amazon OpenSearch).
*   **Scalability and Fail-safe Backup:** By fronting the EC2 collector instances with a Network Load Balancer (NLB), the TCP traffic is distributed evenly, allowing effortless horizontal scaling. Furthermore, an Amazon S3 bucket acts as a backup destination for Firehose (generating no storage costs if Lambda forwards the messages successfully).
*   **Cost Optimization and Vendor Independence:** Embracing OpenTelemetry (Apache 2.0 licensed, free to use) eliminates software licensing fees for third-party platforms. Its standardized design allows teams to switch backend monitoring services in the future without re-engineering the telemetry pipeline.

In conclusion, integrating AWS Lambda, Firehose, and NLB establishes a seamless bridge between public cloud metrics streams and closed private networks. This architecture resolves performance bottlenecks and API limits while giving teams absolute ownership of their metrics. By designing an intelligent, push-based data stream, enterprises can build a powerful, cost-optimized, and future-proof observability platform.

---

### Solution Architecture Diagram

![System Monitoring on AWS](/images/3-BlogsPosted/cloudwatch_to_opentelemetry.png)

---

### Reference Links & Documentation
*   **Original Post on Facebook Group:** [Facebook Post Link](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2173544653410495/?rdid=CUzsR7GSYpgaIwjW)
*   **Official AWS Blog Guide:** [AWS Architecture Blog Guide](https://aws.amazon.com/vi/blogs/architecture/streaming-cloudwatch-metrics-to-vpc-based-opentelemetry-collectors-using-lambda/)