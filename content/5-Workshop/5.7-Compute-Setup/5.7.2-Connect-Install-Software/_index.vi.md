---
title: "5.7.2 Kết nối và cài đặt phần mềm"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.7.2. Kết nối và cài đặt phần mềm

1. Truy cập EC2 từ xa an toàn bằng **Systems Manager Fleet Manager**. Chọn Managed node đang Running và nhấn **Start terminal session**.
   ![Kết nối EC2 bằng Systems Manager](/images/5-Workshop/Connect_EC2_backend_bang_Systems_Manager.jpg)

2. Thực thi lệnh cài đặt **Git** để kéo mã nguồn:
   ```bash
   sudo dnf install git
   ```
   ![Cài Git](/images/5-Workshop/Cai_GIT.jpg)

3. Tiến hành cài đặt và khởi động **Docker** để chạy ứng dụng dạng container:
   ```bash
   sudo dnf install -y docker
   sudo systemctl enable docker
   sudo systemctl start docker
   ```
   ![Cài Docker](/images/5-Workshop/Cai_Docker.jpg)
   ![Kiểm tra trạng thái Docker](/images/5-Workshop/Kiem_tra_trang_thai_Docker.jpg)

4. Điều hướng tới thư mục `/opt` và tải source code từ GitHub:
   ```bash
   cd /opt
   sudo git clone http://github.com/thuanthien-tran/resume-fit.git
   sudo chown -R ssm-user /opt/resume-fit
   ```
   ![Clone source lên EC2](/images/5-Workshop/Clone_source_len_EC2.jpg)
