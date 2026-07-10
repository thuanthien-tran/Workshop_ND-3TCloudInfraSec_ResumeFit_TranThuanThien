---
title: "5.9.1 Kiểm tra hoạt động của Auto Scaling Group"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.9.1. Kiểm tra hoạt động của Auto Scaling Group

1. Truy cập dịch vụ **EC2**, điều hướng đến menu **Instances**.
2. Quan sát hệ thống tự động khởi tạo các EC2 mới có tên `ResumeMatching-ASG-Instance` phân bổ đều ở các Availability Zone khác nhau.
3. Một số máy chủ cũ có thể hiển thị trạng thái `Terminated`. Đây là minh chứng ASG đang hoạt động chính xác: tự động thu hồi máy chủ cũ và khởi chạy máy chủ mới khi có sự thay đổi cấu hình hoặc lỗi hệ thống.
   ![ASG tự khởi tạo và tắt EC2](/images/5-Workshop/ASG_tao_EC2_moi_sau%20khi_cap_nhat_AMI.jpg)
