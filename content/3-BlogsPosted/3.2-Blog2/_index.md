---
title: "Blog 2: Building an AI Gateway for Amazon Bedrock"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Hands-on Experience: Building an AI Gateway to Manage Amazon Bedrock with API Gateway

Hi everyone! Recently, while working on AWS infrastructure labs—from configuring networks and troubleshooting security with Secrets Manager in a Cloud9 environment, to designing a proposal to integrate Machine Learning with Prometheus for system monitoring—I ran into a tough challenge: How do we manage access control and cost when multiple teams share Large Language Models (LLMs) on Amazon Bedrock?

In practice, when building Generative AI applications, you cannot simply hand out raw Bedrock API keys for client-side direct calls. Costs would skyrocket, and tenant isolation would be non-existent. After some research, I found an excellent reference pattern from Dynatrace and decided to test it. Today, I'll share my experience designing an "AI Gateway" from a practical infrastructure perspective.

### Solution Architecture: Lightweight Yet Powerful
Instead of letting clients connect directly to Bedrock, I deployed an Amazon API Gateway as a central protective layer. The complete request flow is broken down as follows:

*   **Route 53 (Optional but recommended):** Instead of using the long default AWS endpoints, Route 53 maps a custom domain that fits enterprise styling.
*   **API Gateway (Main Entrance):** Here I configured rate limiting rules to prevent spam and set usage quotas to stay within budget limits. Crucially, it supports response streaming, allowing real-time, token-by-token streaming from Bedrock models.
*   **Lambda Authorizer (Security Checkpoint):** Requests are validated via a custom Lambda Authorizer verifying JWT tokens. Only authorized calls can proceed.
*   **Lambda Integration (Heart of the System):** This Lambda function intercepts the client request (including headers, body, and query parameters), signs it using AWS Signature Version 4 (SigV4), and forwards it to the Amazon Bedrock API endpoint.

### Why Do I Recommend This Pattern?
During my implementation, this pattern resolved two core problems that infrastructure engineers care about:

#### 1. Transparent to Client
I frequently test code locally using the Boto3 library. The beauty of this gateway is that client-side code requires almost no modification. It communicates seamlessly as if it was hitting Bedrock directly, while all control checks occur transparently behind the scenes.

#### 2. Future-proof Design
AWS continuously updates Bedrock with new models and features. If the gateway hardcoded specific API endpoints, every new model release would require code updates.

Since the Lambda Integration function simply packages and signs requests instead of parsing API models, the gateway remains completely unaffected when Bedrock introduces new models or updates features like Knowledge Bases.

### Conclusion
Coming from an observability background (working with Grafana or Zabbix), consolidating all AI traffic into a single API Gateway makes it easy to attach monitoring tools to track system health and project costs.

Leveraging Serverless services as a governance layer for GenAI applications not only improves security but also dramatically simplifies operations. If you are building GenAI infrastructure on AWS, this AI Gateway model is a must-have architectural pattern.

---

### Solution Architecture Diagram

![Building an AI Gateway for Amazon Bedrock](/images/3-BlogsPosted/ai_gateway_amazon_bedrock.png)

---

### Reference Links & Documentation
*   **Original Post on Facebook Group:** [Facebook Post Link](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2179637596134534/?rdid=654DT9MyMTrqQ5kg#)
*   **Official AWS Blog Guide:** [AWS Architecture Blog Guide](https://aws.amazon.com/vi/blogs/architecture/building-an-ai-gateway-to-amazon-bedrock-with-amazon-api-gateway/)