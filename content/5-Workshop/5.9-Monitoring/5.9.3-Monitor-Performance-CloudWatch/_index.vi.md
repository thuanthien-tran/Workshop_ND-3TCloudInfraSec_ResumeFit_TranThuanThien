---
title: "5.9.3 Giám sát hiệu suất qua CloudWatch"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.9.3. Giám sát hiệu suất qua CloudWatch

1. Truy cập **CloudWatch**, chọn menu **Metrics** để giám sát sâu các thông số.
2. **Đối với EC2**: Lọc Namespace EC2, chọn `CPUUtilization`. Quan sát biểu đồ để thấy các đỉnh gai xử lý (ví dụ `81.9%`) khi AI chạy tác vụ nặng.
   ![CloudWatch đang monitor EC2](/images/5-Workshop/CloudWatch_dang_monitor_EC2.jpg)
   ![EC2 Metrics](/images/5-Workshop/EC2_Metrics.jpg)

3. **Đối với ALB**: Lọc metric `RequestCount` và `TargetResponseTime`. Sự tương quan giữa việc tăng vọt lượng Request và sự thay đổi của thời gian phản hồi giúp đánh giá hiệu năng hệ thống.
   ![CloudWatch monitor Load Balancer](/images/5-Workshop/CloudWatch_monitor_Load_Balancer.jpg)
   ![ALB Metrics](/images/5-Workshop/ALB_Metrics.jpg)
