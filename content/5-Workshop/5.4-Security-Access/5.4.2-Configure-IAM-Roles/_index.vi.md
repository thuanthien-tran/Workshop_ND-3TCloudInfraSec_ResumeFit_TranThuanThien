---
title: "5.4.2 Cấu hình IAM Roles"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.4.2. Cấu hình IAM Roles

1. Truy cập dịch vụ **IAM**, tạo role `ResumeMatching-Backend-Role` để cấp cho máy chủ backend chạy trên EC2.
   ![Tạo Backend IAM Role](/images/5-Workshop/Tao_Backend_IAM_Role.jpg)

2. Tạo role thứ hai mang tên `ResumeMatching-Worker-Role` dành riêng cho Worker server. Đính kèm các policy AWS Managed như `AmazonSQSFullAccess` và quyền thao tác với S3.
   ![Tạo Worker IAM Role](/images/5-Workshop/Tao_Worker_IAM_Role.jpg)
