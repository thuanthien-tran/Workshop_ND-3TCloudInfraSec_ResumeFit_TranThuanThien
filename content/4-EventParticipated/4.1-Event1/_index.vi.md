---
title: "Event 1: FCAJ Community Day"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Bài thu hoạch "FCAJ Community Day"

### Thông tin chung về sự kiện
*   **Tên Sự Kiện:** FCAJ Community Day
*   **Thời gian tổ chức:** 09-05-2026
*   **Địa điểm tổ chức:** Tầng 26, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh
*   **Đơn vị tổ chức:** AWS Study Group phối hợp cùng cộng đồng FCAJ
*   **Vai trò tham gia:** Người tham dự

---

### Mục Đích Của Sự Kiện
*   **Mục tiêu của chương trình:** Tạo môi trường và cơ hội để các bạn trẻ (đặc biệt là sinh viên năm 3, năm 4 hoặc mới ra trường) mạnh dạn chia sẻ kiến thức, rèn luyện kỹ năng thuyết trình, thái độ tự tin trước đám đông và định hướng phát triển sự nghiệp.
*   **Nội dung chính muốn truyền tải:** Cách tạo động lực học tập (hack dopamine), kỹ thuật tối ưu hóa câu lệnh AI (Prompt Engineering), định hướng tư duy cốt lõi trong ngành IT giữa kỷ nguyên AI, và quy trình chuẩn ứng dụng AI vào phát triển phần mềm (phương pháp BMX).
*   **Giá trị dành cho người tham dự:** Giúp người tham dự vượt qua nỗi sợ bị AI thay thế, hiểu được tầm quan trọng của kiến thức nền tảng (foundation), biết cách vận dụng công cụ đúng quy trình và định hình các yếu tố cốt lõi khi phát triển sự nghiệp như "sự liêm chính" (integrity) và tư duy dài hạn.

---

### Danh Sách Diễn Giả
*   **Diễn giả Long:** Trình bày chủ đề *"Hack não bộ với Dopamine"* nhằm tạo động lực học tập bền bỉ.
*   **Diễn giả Thịnh:** Trình bày chủ đề *"Ultimate Prompt Engineering và kiến trúc AWS"*.
*   **Diễn giả Khang:** Solutions Architect tại Cloud Kinetics.
*   **Diễn giả Thảo:** Software Developer tại Ngân hàng Quốc tế Việt Nam (VIB).

---

### Nội Dung Nổi Bật

#### 1. Tổng quan vấn đề thực tế
*   Sinh viên và người đi làm thường thiếu động lực học tập dài hạn, dễ bị phân tâm bởi mạng xã hội do thiếu cơ chế "phần thưởng nhanh".
*   Trong môi trường làm việc thực tế, việc quá phụ thuộc vào AI để viết code trực tiếp mà thiếu bối cảnh và tài liệu hóa sẽ tạo ra những đoạn code rác, thiếu đồng bộ và gặp lỗi ảo giác (hallucination) từ các mô hình AI.

#### 2. Giải pháp được giới thiệu
*   **Để học tập hiệu quả:** Cần chia nhỏ mục tiêu học, tạo phần thưởng ngắn hạn, xây dựng "chuỗi" liên tục (như chơi game) để đánh lừa não bộ tiết ra dopamine tạo hưng phấn.
*   **Để làm chủ công nghệ AI:** Phải tập trung vào "kiến thức nền tảng" (foundation), chia nhỏ task ra thành các văn bản mô tả (document) theo phương pháp BMX trước khi để AI sinh code.

#### 3. Công nghệ, Dịch vụ và Công cụ
*   **Dịch vụ AWS nổi bật:** CloudFront, S3 (lưu trữ), Cognito (xác thực), API Gateway, Lambda (serverless backend), Bedrock (AI models), DynamoDB (NoSQL Database), CloudWatch (Monitoring).
*   **Công cụ AI:** Các mô hình LLMs (Claude, Gemini), extension "Promptimizer", framework BMX.

#### 4. Demo và Case Study thực tế
*   Trình bày một kiến trúc thực tế xây dựng trên AWS kết hợp nhiều dịch vụ Serverless và AI.
*   Demo sử dụng tiện ích mở rộng có tên **"Promptimizer"** để bôi đen văn bản và nhờ AI tối ưu hóa Prompt ngay trên trình duyệt một cách nhanh chóng.
*   **Điểm lưu ý cốt lõi:** Việc dùng AI sẽ **khuếch đại (amplify)** khả năng của người dùng. Nếu nền tảng của bạn kém, AI sẽ làm kết quả tệ hơn; nếu bạn có nền tảng vững, nó sẽ giúp bạn tăng năng suất gấp nhiều lần.

---

### Những Gì Học Được

#### 1. Tư duy và phương pháp học
*   Có thể dùng AI để hỗ trợ quá trình suy nghĩ (brainstorm), nhưng tuyệt đối **không được "outsource" sự hiểu biết của chính mình**. Luôn luôn phải đặt câu hỏi **"Tại sao" (Why)** cho mọi quyết định kỹ thuật.

#### 2. Kiến thức kỹ thuật
*   Cấu trúc thành phần trong Prompt Engineering hiệu quả bao gồm: **Role** (vai trò), **Instruction** (hướng dẫn), **Context** (ngữ cảnh), **Input**, **Output Format** (định dạng) và **Constraints** (ràng buộc).

#### 3. Best practices khi làm việc với AI
*   Để AI không bị lỗi bối cảnh, cần chia nhỏ yêu cầu đầu vào thay vì nhồi nhét.
*   Trong quy trình phát triển, hãy để AI đóng vai trò của từng bộ phận riêng biệt (BM, Architect, Dev, Scrum Master) xử lý từng tính năng nhỏ (story) đã được duyệt kỹ lượng thay vì phó mặc toàn bộ dự án cho một prompt duy nhất.

#### 4. Kinh nghiệm thực tế từ nhà tuyển dụng
*   Nhà tuyển dụng không chỉ cần kết quả đúng mà chú trọng **quá trình tư duy (thought process)** và lý do ứng viên chọn giải pháp đó. 
*   Kinh nghiệm không đếm bằng thời gian làm việc mà đếm bằng số lượng "trải nghiệm" xử lý các bài toán, dự án khác nhau.

---

### Ứng Dụng Vào Công Việc
*   **Áp dụng cho dự án hiện tại:** Thay đổi cách lập trình phần mềm với AI bằng việc đầu tư viết kỹ Document (VOD, System Architect) trước. Phân rã dự án thành Epic, Story rồi mới để AI agent code và tự động review lỗi cho từng phần đó.
*   **Công nghệ muốn thử nghiệm tiếp theo:** Ứng dụng AWS Lambda, Amazon Cognito để làm backend serverless mà không cần tự quản lý server hay database mật khẩu người dùng. Cài đặt và sử dụng extension "Promptimizer" để tăng chất lượng giao tiếp với các mô hình ngôn ngữ.
*   **Cải thiện quy trình làm việc:** Áp dụng **quy tắc 2 phút**: việc gì giải quyết được trong vòng 2 phút thì phải làm ngay, không trì hoãn.

---

### Trải Nghiệm Trong Event
*   **Học hỏi từ diễn giả:** Nhận thức rõ về 5 yếu tố quyết định khi đi làm: *Salary (Lương), Experience (Kinh nghiệm), Network (Mạng lưới), Knowledge (Kiến thức) và Profile (Hồ sơ)*.
*   **Trải nghiệm thực hành:** Việc xem các case study thiết kế kiến trúc hệ thống và demo thao tác trực tiếp với Promptimizer mang lại hình dung rất thực tế và sinh động.
*   **Giao lưu và kết nối:** Cộng đồng động viên các thành viên (kể cả sinh viên) không sợ sai, không sợ chia sẻ điều người khác đã biết, đề cao tính làm việc nhóm (teamwork) để đi xa cùng nhau.
*   **Điều ấn tượng nhất:** Quan điểm về **"Sự liêm chính" (Integrity)** - đó là việc tự giác xử lý toàn bộ các tình huống ngoại lệ (corner cases) và làm tốt mọi nhiệm vụ dù sếp có kiểm tra hay không, và tính chịu trách nhiệm với sự tin tưởng trong đường dài.

---

### Bài Học Rút Ra
*   **Kiến thức quan trọng nhất:** Nắm thật chắc **kiến thức nền tảng (foundation)**; chỉ khi hiểu tận gốc vấn đề bạn mới có khả năng thẩm định xem kết quả do AI sinh ra đúng hay sai.
*   **Kinh nghiệm thực tế:** Sai lầm là điều cần thiết để phát triển, đặc biệt ở giai đoạn "fresher". Các công ty sẵn sàng trả chi phí cho sai lầm của bạn miễn là bạn có tư duy học hỏi và sửa đổi.
*   **Định hướng học tập tiếp theo:** Tập thói quen theo dõi những cập nhật mới từ AWS hay công nghệ để tổng hợp kiến thức, định hướng trở thành người có thể trình bày/chia sẻ kiến thức (speaker) thay vì tiêu thụ nội dung vô bổ. Phát triển môi trường học tập bền bỉ và kiên trì, không mong đợi kết quả trong chớp mắt.

---

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh diễn giả đang thuyết trình](/images/4-EventParticipated/fcaj_community_day_1.jpg)
*Hình 1: Diễn giả chia sẻ về quy trình làm việc với Agent AI*

![Giao diện trình bày bài học](/images/4-EventParticipated/fcaj_community_day_2.jpg)
*Hình 2: Trình bày bài học về tư duy phát triển Growth Mindset*

![Hình ảnh diễn giả chia sẻ tại hội trường](/images/4-EventParticipated/fcaj_community_day_3.jpg)
*Hình 3: Chia sẻ về tầm quan trọng của Prompt Engineering*

![Ảnh lưu niệm tập thể](/images/4-EventParticipated/fcaj_community_day_4.jpg)
*Hình 4: Ảnh lưu niệm tập thể cùng cộng đồng FCAJ*
