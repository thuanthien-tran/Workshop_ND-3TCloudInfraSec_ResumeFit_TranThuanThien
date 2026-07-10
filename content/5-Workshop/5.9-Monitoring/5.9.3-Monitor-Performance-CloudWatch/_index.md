---
title: "5.9.3 CloudWatch Dashboard Analytics"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.9.3. CloudWatch Dashboard Analytics

1. Open **CloudWatch** and select the **Metrics** page.
2. **EC2 Metrics:** Access EC2 namespace and display `CPUUtilization`. Trace load fluctuations (e.g. `81.9%`) during intensive document analysis.
   ![CloudWatch monitor EC2](/images/5-Workshop/CloudWatch_dang_monitor_EC2.jpg)
   ![EC2 Metrics Panel](/images/5-Workshop/EC2_Metrics.jpg)

3. **ALB Metrics:** Search for `RequestCount` and `TargetResponseTime` to cross-examine traffic spikes against system latency.
   ![CloudWatch monitor ALB](/images/5-Workshop/CloudWatch_monitor_Load_Balancer.jpg)
   ![ALB Metrics Panel](/images/5-Workshop/ALB_Metrics.jpg)
