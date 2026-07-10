---
title: "5.3.2 Cấu hình Subnet và Route Table"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.3.2. Cấu hình Subnet và Route Table

1. Truy cập mục **Subnets** và tạo lần lượt các subnet với các dải CIDR phù hợp:
   * Public Subnets: `Public-Subnet-A` (`10.0.1.0/24`), `Public-Subnet-B` (`10.0.2.0/24`).
   * Private App Subnets: `Private-App-A` (`10.0.11.0/24`), `Private-App-B` (`10.0.12.0/24`).
   * Private DB Subnets: `Private-DB-A` (`10.0.21.0/24`), `Private-DB-B` (`10.0.22.0/24`).
   ![Tạo Subnets](/images/5-Workshop/Tao_cac_Public_va_Private_subnet.jpg)

2. Tạo một Route Table công khai với tên `Public-RT` và gán vào VPC.
   ![Tạo Public Route Table](/images/5-Workshop/Tao_Public_Route_Table.jpg)

3. Trong phần **Edit routes** của `Public-RT`, thêm route có `Destination` là `0.0.0.0/0` và trỏ `Target` đến Internet Gateway (`ResumeMatching-IGW`).
   ![Thêm Routes](/images/5-Workshop/Add_Routes.jpg)

4. Gán (Associate) `Public-RT` vào 2 subnets công cộng: `Public-Subnet-A` và `Public-Subnet-B`.
   ![Gán Route Table công khai](/images/5-Workshop/Gan_Public_Route_Table.jpg)

5. Tạo các Route Table riêng tư cho App và Database bao gồm: `Private-App-RT` (cho Subnet A), `ResumeMatching-Private-App-RT-B` (cho Subnet B), và `Private-DB-RT` (cho DB Subnets).
   ![Tạo Route Table B](/images/5-Workshop/Tao_Route_Table_B.jpg)
   ![Tạo và Gán Private App Route Table](/images/5-Workshop/Tao_va_gan_Private_App_Route_Table.jpg)
   ![Thêm Route Tables cho Private App](/images/5-Workshop/Add_Route_Tables_cho_Private-App-RT.jpg)
   ![Tạo và Gán Database Route Table](/images/5-Workshop/Tao_va_gan_Database_Route_Table.jpg)
