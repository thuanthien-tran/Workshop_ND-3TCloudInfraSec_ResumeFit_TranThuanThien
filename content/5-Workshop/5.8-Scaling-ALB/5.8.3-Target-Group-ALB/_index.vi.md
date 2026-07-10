---
title: "5.8.3 Target Group và Application Load Balancer"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.8.3. Target Group và Application Load Balancer

1. Tạo một **Target Group** tên `ResumeMatching-TG`, dạng `Instance` giao thức HTTP trên cổng `8080`.
   ![Tạo target group](/images/5-Workshop/Tao_target_group.jpg)

2. Khởi tạo **Application Load Balancer (ALB)** tên `ResumeMatching-ALB`. Lựa chọn Scheme là `Internet-facing` để nhận traffic từ ngoài internet, lắng nghe tại 2 Availability Zones và định tuyến giao thông vào mạng thông qua Target Group trên.
   ![Tạo ALB](/images/5-Workshop/Tao_ALB.jpg)
