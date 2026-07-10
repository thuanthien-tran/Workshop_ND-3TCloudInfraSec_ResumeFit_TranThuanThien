---
title: "5.10. Kiểm thử Ứng dụng"
date: 2024-01-01
weight: 10
chapter: false
---

## 5.10. Kiểm thử Ứng dụng Resume Fit

1. Kiểm thử thông qua endpoint API của ALB (ví dụ DNS Name của ALB kèm route `/api/ready`) để nhận về JSON `{"status": "ready"}` chứng minh toàn bộ Backend và Database đã được liên kết thành công.
   ![Test hoạt động bằng DNS của ALB](/images/5-Workshop/Test_hoat_dong_bang_DNS_cua_ALB.jpg)
   ![Tiến hành kiểm tra các kết nối](/images/5-Workshop/Tien_hanh_kiem_tra_cac_ket_noi.jpg)

2. Truy cập Domain/IP của Frontend. Tại giao diện **Đăng ký** và **Đăng nhập**, tiến hành tạo tài khoản và đăng nhập vào hệ thống.
   ![Giao diện đăng ký](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_dang_ky.jpg)
   ![Giao diện đăng nhập](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_dang_nhap.jpg)

3. Chạy luồng công việc chính: Tạo mô tả công việc (JD) mới và tải lên CV của ứng viên.
   ![Giao diện bước 1 tạo tên công việc ứng tuyển](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_1_tao_ten_cong_viec_ung_tuyen.jpg)
   ![Giao diện danh sách JD](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_sach_JD.jpg)
   ![Giao diện bước 2 upload CV JD](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_2_upload_CV_JD.jpg)
   ![Giao diện bước 2 upload CV JD Part 2](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_2_upload_CV_JD_Part-2.jpg)
   ![Giao diện danh sách CV](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_sach_CV.jpg)

4. Yêu cầu hệ thống phân tích. AI sẽ trả về **Báo cáo chi tiết ứng viên** bao gồm:
   * Độ khớp cấp bậc và tổng quan phần trăm phù hợp.
   * Phân tích các kỹ năng chuyên môn còn thiếu.
   * Khuyến nghị phỏng vấn và sinh tự động các câu hỏi phỏng vấn kỹ thuật dựa trên chính ngữ cảnh dự án trong CV.
   ![Giao diện bước 3 xem kết quả ứng viên](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_3_xem_ket_qua_ung_vien.jpg)
   ![Giao diện đánh giá phân tích ứng viên](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_phan_tich_ung_vien.jpg)
   ![Giao diện đánh giá mức độ phù hợp](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_muc_do_phu_hop.jpg)
   ![Giao diện đánh giá phân tích điểm số](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_phan_tich_diem_so.jpg)
   ![Giao diện đánh giá kỹ năng](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_ky_nang.jpg)
   ![Giao diện đánh giá khuyến nghị](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_khuyen_nghi.jpg)
   ![Giao diện đánh giá câu hỏi phỏng vấn](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_cau_hoi_phong_van.jpg)
   ![Giao diện đánh giá văn bản trích xuất](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_van_ban_trich_xuat.jpg)
   
5. Bạn cũng có thể theo dõi lịch sử phân tích, danh sách ứng viên xếp hạng phù hợp nhất hoặc thông tin debug hệ thống.
   ![Giao diện lịch sử đánh giá CV JD](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_lich_su_danh_gia_CV_JD.jpg)
   ![Giao diện xếp hạng ứng viên phù hợp](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_xep_hang_ung_vien_phu_hop.jpg)
   ![Giao diện thông tin gỡ lỗi debugger](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_thong_tin_go_loi_debugger.jpg)
