---
title: "5.5.2 SQS Queue Setup"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.5.2. SQS Queue Setup

1. Navigate to the **SQS** Console. Create a Standard queue named `ResumeMatching-DLQ` (Dead Letter Queue) to isolate failed message payloads.
   ![Create SQS DLQ](/images/5-Workshop/Tao_queue.jpg)

2. Create the main SQS queue named `ResumeMatching-Queue`.
   ![Create Main SQS Queue](/images/5-Workshop/Tao_main_queue.jpg)
