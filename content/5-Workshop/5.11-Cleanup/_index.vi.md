---
title: "5.11. Dọn dẹp tài nguyên & Chi phí"
date: 2024-01-01
weight: 11
chapter: false
---

## 5.11. Dọn dẹp tài nguyên & Chi phí (Clean up & Cost)

Sau khi hoàn tất quá trình workshop và kiểm thử, để tránh phát sinh chi phí duy trì hạ tầng không cần thiết trên AWS, hãy tiến hành:

1. Xóa Auto Scaling Group để ngăn hệ thống tự khởi tạo lại máy chủ, sau đó Terminate các EC2 Instances thủ công còn sót lại.
2. Xóa Application Load Balancer và Target Group.
3. Xóa Database RDS (bỏ chọn tính năng tạo Snapshot cuối cùng) và Subnet Group của RDS.
4. Xóa NAT Gateway, đợi đến khi trạng thái là Deleted thì Release các Elastic IPs.
5. Giải phóng VPC Endpoints, Route Tables, Internet Gateway, Subnets và cuối cùng là xóa VPC.
6. Xóa rỗng toàn bộ object trong S3 bucket, sau đó tiến hành Delete Bucket.

## 3. Cost Breakdown

Phần dưới đây được lập theo phong cách báo cáo học thuật, với cơ sở tính toán từ **AWS Pricing Calculator** tại **US East (N. Virginia) - us-east-1**, sử dụng **On-Demand Pricing** và thời gian vận hành **730 giờ/tháng**.

| STT | AWS Service | Configuration | Quantity | Estimated Monthly Cost (USD) | Notes | Total (USD) |
|---|---|---|---:|---:|---|---:|
| 1 | Amazon VPC | 01 VPC, 02 public subnets, 02 private application subnets, 02 private database subnets, 01 Internet Gateway, route tables, và Security Groups | 1 bộ | 0.000 | Hạ tầng mạng nền tảng, không phát sinh phí trực tiếp | 0.000 |
| 2 | Internet Gateway | 01 Internet Gateway gắn với VPC | 1 | 0.000 | Không tính phí trực tiếp | 0.000 |
| 3 | Public / Private Subnets | Tổng cộng 06 subnet | 6 | 0.000 | Không tính phí trực tiếp | 0.000 |
| 4 | Security Group | Bộ quy tắc truy cập cho EC2, ALB và RDS | 1 bộ | 0.000 | Không tính phí trực tiếp | 0.000 |
| 5 | NAT Gateway | 02 NAT Gateway tại us-east-1 | 2 | 32.963 | Khoảng USD 0.045/giờ mỗi NAT Gateway x 730 giờ + lưu lượng xử lý thấp | 65.925 |
| 6 | Amazon EC2 | Instance Linux t3.micro cho backend | 3 | 7.592 | Khoảng USD 0.0104/giờ mỗi instance x 730 giờ | 22.776 |
| 7 | Amazon EBS | gp3, 30 GB cho mỗi EC2 instance | 3 volume | 2.400 | 30 GB x 3 instance x USD 0.08/GB-tháng | 7.200 |
| 8 | Amazon Machine Image (AMI) | Dung lượng snapshot cho 01 AMI 30 GB | 1 | 1.500 | Ước tính chi phí lưu trữ snapshot AMI | 1.500 |
| 9 | Launch Template | Launch template dùng cho Auto Scaling | 1 | 0.000 | Chỉ là đối tượng cấu hình | 0.000 |
| 10 | Auto Scaling Group | Nhóm ASG chứa 02 instance | 1 bộ | 0.000 | Chỉ quản lý vòng đời instance, chi phí EC2 đã tính riêng | 0.000 |
| 11 | Application Load Balancer | 01 ALB tại us-east-1 | 1 | 22.265 | Khoảng USD 0.0225/giờ + mức sử dụng LCU thấp | 22.265 |
| 12 | Target Group | 01 target group cho ALB | 1 | 0.000 | Không tính phí trực tiếp | 0.000 |
| 13 | Amazon RDS | db.t3.micro, Single-AZ, PostgreSQL, 20 GB gp3 storage | 1 | 15.440 | Khoảng USD 0.018/giờ + 20 GB lưu trữ | 15.440 |
| 14 | Amazon S3 | Standard storage, khoảng 5 GB | 1 bucket | 0.115 | Chỉ tính dung lượng lưu trữ, số request giả định rất thấp | 0.115 |
| 15 | Amazon SQS | Standard Queue + DLQ | 2 queue | 0.000 | Lưu lượng demo thấp, nằm trong ngưỡng miễn phí | 0.000 |
| 16 | AWS Secrets Manager | 01 secret | 1 | 0.400 | USD 0.40/secret-tháng | 0.400 |
| 17 | Amazon Cognito | Xác thực người dùng dưới 50.000 MAU | 1 user pool | 0.000 | Giả định mức sử dụng demo nằm trong ngưỡng miễn phí | 0.000 |
| 18 | AWS Systems Manager | Session Manager để truy cập instance | 1 | 0.000 | Session Manager không phát sinh phí trực tiếp | 0.000 |
| 19 | Amazon CloudWatch | Metrics và Logs cơ bản | 1 bộ | 0.530 | Lưu lượng log và theo dõi ở mức thấp cho mục đích demo | 0.530 |

**Tổng chi phí triển khai mỗi tháng:** **USD 136.151**

### Phân tích chi phí

- **Dịch vụ chiếm chi phí cao nhất:** NAT Gateway, với chi phí khoảng **USD 65.925/tháng**, tương đương khoảng **48.42%** tổng chi phí.
- **Các khoản chi phí lớn tiếp theo:** EC2 (**USD 22.776**) và Application Load Balancer (**USD 22.265**).
- **Đánh giá theo AWS Credits:** Tổng chi phí ước tính **thấp hơn mức AWS Credits 200 USD**, do đó hệ thống **phù hợp** với phạm vi demo và bảo vệ đồ án.

### Đề xuất tối ưu chi phí

1. **Giảm thời gian tồn tại của NAT Gateway** vì đây là thành phần có chi phí cao nhất.
2. **Xóa ngay tài nguyên không dùng đến** sau khi demo, đặc biệt là NAT Gateway, RDS và ALB.
3. **Giữ nguyên loại instance nhỏ nhất phù hợp** như kiến trúc hiện tại và tránh tăng quy mô không cần thiết.
4. **Thiết lập thời gian lưu log ngắn trên CloudWatch** và giới hạn dung lượng S3 ở mức cần thiết.
5. **Không thay đổi kiến trúc hiện tại**, nhưng cần thực hiện quy trình dọn dẹp theo từng phiên demo để tránh phát sinh chi phí nhàn rỗi.
