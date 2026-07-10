---
title: "5.10. Verification and Testing"
date: 2024-01-01
weight: 10
chapter: false
---

## 5.10. Resume Fit Application Verification

1. Access the ALB DNS address at `/api/ready` endpoint. Receive verification JSON payload: `{"status": "ready"}`.
   ![Validate ALB DNS Endpoint](/images/5-Workshop/Test_hoat_dong_bang_DNS_cua_ALB.jpg)
   ![Database and Backend connectivity validation](/images/5-Workshop/Tien_hanh_kiem_tra_cac_ket_noi.jpg)

2. Load the Frontend UI. Go to the **Register** and **Login** windows, and authenticate.
   ![Register UI](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_dang_ky.jpg)
   ![Login UI](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_dang_nhap.jpg)

3. Execute the workflow: Create a Job Position (JD) and upload Candidate Resumes (CVs).
   ![Step 1 Create Job Name](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_1_tao_ten_cong_viec_ung_tuyen.jpg)
   ![JD List View](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_sach_JD.jpg)
   ![Step 2 Upload CV JD](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_2_upload_CV_JD.jpg)
   ![Step 2 Details](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_2_upload_CV_JD_Part-2.jpg)
   ![CV List View](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_sach_CV.jpg)

4. Trigger evaluation. The platform uses OpenAI model APIs to return a candidate report including:
   * Match rating and overall suitability score.
   * Gap analysis showing missing technical skillsets.
   * Recommendations and automated generation of interview questions.
   ![Step 3 Result Dashboard](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_buoc_3_xem_ket_qua_ung_vien.jpg)
   ![Candidate Analysis Report](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_phan_tich_ung_vien.jpg)
   ![Suitability Rating Details](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_muc_do_phu_hop.jpg)
   ![Score Distribution](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_phan_tich_diem_so.jpg)
   ![Skillset Gap Details](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_ky_nang.jpg)
   ![Recommendation Verdict](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_khuyen_nghi.jpg)
   ![Generated Interview Questions](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_cau_hoi_phong_van.jpg)
   ![Extracted Content Viewer](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_danh_gia_van_ban_trich_xuat.jpg)
   
5. You can also view assessment history, rank matching candidates, or check debugger logs.
   *   ![History View](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_lich_su_danh_gia_CV_JD.jpg)
   *   ![Rankings Dashboard](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_xep_hang_ung_vien_phu_hop.jpg)
   *   ![SSM Debugger Panel](/images/5-Workshop/giao%20di%E1%BB%87n/giao_dien_thong_tin_go_loi_debugger.jpg)
