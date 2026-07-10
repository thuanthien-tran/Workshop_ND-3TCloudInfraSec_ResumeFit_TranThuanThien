---
title: "5.7.2 Shell Access and Software Setup"
date: 2024-01-01
weight: 2
chapter: false
---

### 5.7.2. Shell Access and Software Setup

1. Connect to the instance securely using **Systems Manager Fleet Manager**. Choose the running node and start a terminal session.
   ![SSM Terminal Login](/images/5-Workshop/Connect_EC2_backend_bang_Systems_Manager.jpg)

2. Run commands to install **Git**:
   ```bash
   sudo dnf install git
   ```
   ![Install Git](/images/5-Workshop/Cai_GIT.jpg)

3. Install and run **Docker** service to host container workloads:
   ```bash
   sudo dnf install -y docker
   sudo systemctl enable docker
   sudo systemctl start docker
   ```
   ![Install Docker](/images/5-Workshop/Cai_Docker.jpg)
   ![Check Docker Status](/images/5-Workshop/Kiem_tra_trang_thai_Docker.jpg)

4. Clone the application code repository under `/opt` directory:
   ```bash
   cd /opt
   sudo git clone http://github.com/thuanthien-tran/resume-fit.git
   sudo chown -R ssm-user /opt/resume-fit
   ```
   ![Clone Repository](/images/5-Workshop/Clone_source_len_EC2.jpg)
