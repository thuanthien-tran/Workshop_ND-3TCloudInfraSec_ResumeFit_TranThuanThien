---
title: "5.3.2 Subnet and Route Table Configurations"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.3.2. Subnet and Route Table Configurations

1. In the **Subnets** dashboard, create the following subnets using designated CIDR blocks:
   * Public Subnets: `Public-Subnet-A` (`10.0.1.0/24`), `Public-Subnet-B` (`10.0.2.0/24`).
   * Private App Subnets: `Private-App-A` (`10.0.11.0/24`), `Private-App-B` (`10.0.12.0/24`).
   * Private DB Subnets: `Private-DB-A` (`10.0.21.0/24`), `Private-DB-B` (`10.0.22.0/24`).
   ![Create Subnets](/images/5-Workshop/Tao_cac_Public_va_Private_subnet.jpg)

2. Create a public Route Table named `Public-RT` in your VPC.
   ![Create Public Route Table](/images/5-Workshop/Tao_Public_Route_Table.jpg)

3. In the **Edit routes** page of `Public-RT`, add a route pointing `0.0.0.0/0` to your Internet Gateway (`ResumeMatching-IGW`).
   ![Add Routes](/images/5-Workshop/Add_Routes.jpg)

4. Associate `Public-RT` with the two public subnets: `Public-Subnet-A` and `Public-Subnet-B`.
   ![Associate Public Route Table](/images/5-Workshop/Gan_Public_Route_Table.jpg)

5. Create dedicated Route Tables for App and DB layers, namely `Private-App-RT` (Subnet A), `ResumeMatching-Private-App-RT-B` (Subnet B), and `Private-DB-RT` (DB subnets), and associate them accordingly to prevent public visibility.
   ![Create Route Table B](/images/5-Workshop/Tao_Route_Table_B.jpg)
   ![Create and Associate Private App Route Table](/images/5-Workshop/Tao_va_gan_Private_App_Route_Table.jpg)
   ![Add Route Tables for Private App](/images/5-Workshop/Add_Route_Tables_cho_Private-App-RT.jpg)
   ![Create and Associate Database Route Table](/images/5-Workshop/Tao_va_gan_Database_Route_Table.jpg)
