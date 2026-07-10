---
title: "5.7.1 Khởi tạo EC2 Backend Instance"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.7.1. Khởi tạo EC2 Backend Instance

1. Tạo một khóa **Key Pair** (`ResumeMatching-Key`) kiểu RSA dùng để truy cập SSH.
   ![Tạo Key Pair](/images/5-Workshop/Tao_Key_Pair.jpg)

2. Tại EC2 Dashboard, khởi chạy một Instance có tên `ResumeMatching-Backend` với Instance type là `t3.micro` đặt trong VPC ứng dụng.
   ![Tạo EC2 Backend](/images/5-Workshop/Tao_EC2_Backend.jpg)
