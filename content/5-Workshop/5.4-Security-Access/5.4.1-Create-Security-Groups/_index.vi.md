---
title: "5.4.1 Khởi tạo Security Groups"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.4.1. Khởi tạo Security Groups

1. **ALB Security Group** (`ResumeMatching-ALB-SG`): Mở port HTTP (`80`) và HTTPS (`443`) (TCP) với Source là `0.0.0.0/0`.
   ![Tạo ALB Security Group](/images/5-Workshop/Tao_ALB_Security_Group.jpg)

2. **Backend Security Group** (`ResumeMatching-Backend-SG`): Cấu hình Inbound rule cho phép giao thức HTTP trên cổng TCP. Source được giới hạn chỉ nhận luồng từ `ResumeMatching-ALB-SG`.
   ![Tạo Backend Security Group](/images/5-Workshop/Tao_Backend_Security_Group.jpg)

3. **Worker Security Group** (`ResumeMatching-Worker-SG`): Tường lửa bảo vệ Worker Server xử lý tác vụ nền.
   ![Tạo Worker Security Group](/images/5-Workshop/T%E1%BA%A1o_Worker_Security_Group.jpg)

4. **Database Security Group** (`ResumeMatching-RDS-SG`): Mở port `5432` (PostgreSQL). Source chỉ cho phép nhận kết nối nội bộ từ Backend và Worker Security Group.
   ![Tạo Database Security Group](/images/5-Workshop/Tao_Database_Security_Group.jpg)
