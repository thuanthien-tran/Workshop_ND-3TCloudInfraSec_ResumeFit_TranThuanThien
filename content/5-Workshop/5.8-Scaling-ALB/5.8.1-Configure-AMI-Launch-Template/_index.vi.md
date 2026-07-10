---
title: "5.8.1 Cấu hình AMI và Launch Template"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.8.1. Cấu hình AMI và Launch Template

1. Chuẩn hóa môi trường EC2 vừa cài đặt bằng cách tạo ra một Amazon Machine Image (AMI) mang tên `ResumeMatching-Backend-AMI`.
   ![Tạo AMI](/images/5-Workshop/Tao_AMIs.jpg)

2. Từ AMI này, tạo một **Launch Template** mang tên `ResumeMatching-LT` chứa các cấu hình phần cứng, mạng và bảo mật chuẩn.
   ![Tạo launch template](/images/5-Workshop/Tao_launch_template.jpg)
