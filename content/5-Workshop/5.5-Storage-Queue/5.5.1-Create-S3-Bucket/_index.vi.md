---
title: "5.5.1 Khởi tạo S3 Bucket"
date: 2024-01-01
weight: 1
chapter: false
---

### 5.5.1. Khởi tạo S3 Bucket

1. Chuyển sang dịch vụ **S3**, nhấn **Create bucket** để tạo nơi lưu trữ CV và tài liệu của ứng viên.
   ![Tạo S3](/images/5-Workshop/Tao_S3.jpg)

2. Tạo cấu trúc thư mục lưu trữ bên trong S3 Bucket.
   ![Tạo Folder trong S3](/images/5-Workshop/Create_Folder_S3.jpg)

3. Tại tab **Permissions**, tiến hành chỉnh sửa **Cross-origin resource sharing (CORS)**. Thêm nội dung JSON để cấu hình `AllowedMethods` bao gồm: `GET`, `PUT`, `POST` nhằm cho phép ứng dụng web tải file lên bucket.
   ![Bổ sung CORS S3](/images/5-Workshop/Bo_sung_CORS_S3.jpg)
