---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---


Mục này tổng hợp các bài viết kỹ thuật chia sẻ kiến thức (Blogs) của em đã đăng tải trên cộng đồng [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj):

###  [Blog 1 - GIÁM SÁT HỆ THỐNG TRÊN AWS: ĐƯA CLOUDWATCH METRICS VÀO OPENTELEMETRY COLLECTOR TRONG VPC BẰNG LAMBDA](3-blogsposted/3.1-blog1/)
Blog này hướng dẫn giải pháp sử dụng AWS Lambda làm cầu nối để truyền dữ liệu từ CloudWatch Metric Streams vào OpenTelemetry Collector nằm trong private subnet của VPC một cách bảo mật, tối ưu chi phí và loại bỏ rủi ro phụ thuộc nhà cung cấp (vendor lock-in).

###  [Blog 2 - KINH NGHIỆM THỰC CHIẾN: XÂY DỰNG AI GATEWAY QUẢN TRỊ AMAZON BEDROCK BẰNG API GATEWAY](3-blogsposted/3.2-blog2/)
Blog này chia sẻ trải nghiệm thiết kế và triển khai "AI Gateway" sử dụng Amazon API Gateway và AWS Lambda để xác thực, kiểm soát tốc độ (rate limiting), phân chia quota và quản trị tập trung luồng truy cập tới Amazon Bedrock một cách bảo mật, linh hoạt.

###  [Blog 3 - MỘT TÍNH NĂNG KHÁ LIÊN QUAN CỦA AWS LAKE FORMATION](3-blogsposted/3.3-blog3/)
Blog này giới thiệu tính năng tự động cấp thông tin đăng nhập tạm thời (temporary credentials) của AWS Lake Formation giúp EMR Spark truy cập trực tiếp file dữ liệu trên S3 mà không bị lỗi lệch cấu hình phân quyền với Athena.