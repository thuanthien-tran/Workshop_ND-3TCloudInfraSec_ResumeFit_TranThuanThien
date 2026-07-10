---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Mục tiêu tuần 5:

* Hiểu khái niệm về tính sẵn sàng cao (High Availability) và khả năng chịu lỗi (Fault Tolerance).
* Tạo các Custom AMIs phục vụ việc sao chép nhân bản máy chủ nhanh chóng.
* Triển khai Application Load Balancers (ALBs) để phân phối lưu lượng truy cập.
* Cấu hình Auto Scaling Groups (ASGs) để tự động co giãn số lượng máy chủ theo tải thực tế.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 4 | - Nghiên cứu kiến trúc Elastic Load Balancing (ELB) và phân biệt các dòng ALB, NLB, GLB. | 20/05/2026 | 20/05/2026 | [AWS ELB Architecture Guide](https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html) |
| 5 | - Cài đặt web server trên một EC2 instance mẫu và tiến hành tạo Amazon Machine Image (AMI) từ instance này. | 21/05/2026 | 21/05/2026 | [Create Custom AMI Guide](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami-ebs.html) |
| 6 | - Tạo và cấu hình Application Load Balancer (ALB). Định nghĩa Target Groups và kiểm tra khả năng điều hướng lưu lượng truy cập. | 22/05/2026 | 22/05/2026 | [Application Load Balancer Introduction](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html) |
| 2 | - Cấu hình Auto Scaling Group (ASG) kết hợp Launch Template. Thiết lập các quy tắc co giãn (scaling policies) dựa trên chỉ số CPU. | 25/05/2026 | 25/05/2026 | [AWS Auto Scaling Group Docs](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html) |
| 3 | - Thực hiện kiểm tra tính sẵn sàng cao bằng cách giả lập tải nặng hoặc tắt nóng EC2 instance để test cơ chế tự phục hồi (self-healing) của ASG. | 26/05/2026 | 26/05/2026 | [EC2 Auto Scaling Groups Configuration Guide](https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html) |


### Kết quả đạt được tuần 5:

* Xây dựng thành công kiến trúc mở rộng tự động (scalability) tùy thuộc vào lưu lượng truy cập thực tế.
* Triển khai cơ chế tự phục hồi hệ thống (self-healing) khi phát hiện máy chủ bị lỗi hay không phản hồi.
* Nắm vững cách tập trung hóa các điểm truy cập ứng dụng thông qua Load Balancers.
