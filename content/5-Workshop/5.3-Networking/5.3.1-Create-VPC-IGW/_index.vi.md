---
title: "5.3.1 Tạo VPC và Internet Gateway"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.3.1. Tạo VPC và Internet Gateway

1. Truy cập vào giao diện VPC Console, chọn **Create VPC**. Khởi tạo một VPC với tên `ResumeMatching-VPC` và thiết lập dải IP `IPv4 CIDR` là `10.0.0.0/16`.
   ![Tạo VPC](/images/5-Workshop/tao_VPC.jpg)

2. Bật tính năng DNS Hostnames cho VPC để cho phép phân giải tên miền nội bộ.
   ![Bật DNS Hostnames](/images/5-Workshop/Enable_DNS_Hostnames.jpg)

3. Tạo một Internet Gateway có tên `ResumeMatching-IGW` để cung cấp đường truyền kết nối ra internet cho các tài nguyên công khai.
   ![Tạo Internet Gateway](/images/5-Workshop/Tao_Internet_Gateway.jpg)

4. Thực hiện Attach Internet Gateway vừa tạo vào `ResumeMatching-VPC`.
   ![Attach Internet Gateway](/images/5-Workshop/Attach_vao_VPC.jpg)
