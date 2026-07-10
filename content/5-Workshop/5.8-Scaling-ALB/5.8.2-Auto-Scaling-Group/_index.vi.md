---
title: "5.8.2 Auto Scaling Group"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.8.2. Auto Scaling Group (ASG)

1. Tạo Auto Scaling Group `ResumeMatching-ASG` và liên kết với Launch template `ResumeMatching-LT`.
   ![Tạo ASG](/images/5-Workshop/Tao_ASG.jpg)

2. Chỉnh sửa Desired capacity lên thành `2`. ASG sẽ tự động launch ra các EC2 instances mới ở trạng thái Initializing nhằm phục vụ dự phòng và mở rộng.
   ![ASG tạo thêm EC2](/images/5-Workshop/ASG_tao_them_EC2.jpg)
