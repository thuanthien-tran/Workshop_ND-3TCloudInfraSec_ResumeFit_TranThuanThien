---
title: "5.3.3 Thiết lập NAT Gateway cho Private Subnets"
date: 2024-01-01
weight: 3
chapter: false
---

### 5.3.3. Thiết lập NAT Gateway cho Private Subnets

1. Khởi tạo hai địa chỉ IP tĩnh **Elastic IP** là `ResumeMatching-EIP` và `ResumeMatching-EIP-B`.
   ![Tạo Elastic IP](/images/5-Workshop/Tao_Elastic_IP.jpg)
   ![Tạo Elastic IP B](/images/5-Workshop/Tao_Elastic_IP_B%20%28ph%C3%ADa%20sau%20b%C6%B0%E1%BB%9Bc%20t%E1%BA%A1o%20Elastic%20IP%29.jpg)

2. Tạo **NAT Gateway** thứ nhất tên `ResumeMatching-NAT` đặt tại `Public-Subnet-A` và gắn Elastic IP thứ nhất.
   ![Tạo NAT](/images/5-Workshop/Tao_NAT.jpg)

3. Tạo thêm **NAT Gateway** thứ hai tên `ResumeMatching-NAT-B` đặt tại `Public-Subnet-B` và gắn Elastic IP thứ hai nhằm đảm bảo tính sẵn sàng cao (High Availability).
   ![Tạo NAT B](/images/5-Workshop/Tao_NAT_B%20%28b%C6%B0%E1%BB%9Bc%20n%C3%A0y%20ph%C3%ADa%20sau%20b%C6%B0%E1%BB%9Bc%20t%E1%BA%A1o%20NAT%29.jpg)
