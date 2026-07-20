---
title: "Event 2: FCAJ Community Day"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Bài thu hoạch "FCAJ Community Day (23-05-2026)"

### Thông tin chung về sự kiện
*   **Tên Sự Kiện:** FCAJ Community Day
*   **Thời gian tổ chức:** Buổi sáng ngày nghỉ cuối tuần (23-05-2026)
*   **Địa điểm tổ chức:** Tầng 36, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh
*   **Đơn vị tổ chức:** AWS Study Group phối hợp cùng cộng đồng FCAJ
*   **Vai trò tham gia:** Người tham dự

---

### Mục Đích Của Sự Kiện
*   **Mục tiêu của chương trình:** Không chỉ là một buổi hội thảo kỹ thuật thông thường, sự kiện là nơi để kết nối, giao lưu và truyền cảm hứng cho nhau giữa các thành viên trong ngành công nghệ thông tin.
*   **Nội dung chính muốn truyền tải:** Xoay quanh các chủ đề từ AI, Cloud đến những câu chuyện thực tế được đúc kết từ kinh nghiệm của các chuyên gia. Đi sâu thảo luận về tối ưu hóa cách dùng Prompt, ứng dụng dịch vụ AWS (như CloudFront), chia sẻ hành trình thi Hackathon và tư duy xây dựng kiến trúc AI nghiệp vụ (Enterprise-grade).
*   **Giá trị dành cho người tham dự:** Giúp người học và người đi làm hiểu rõ sự biến động của thị trường việc làm dưới tác động của AI, cách chuẩn bị nền tảng kỹ thuật vững chắc để tránh bị đào thải, và trang bị tư duy thực tiễn để giải quyết bài toán của doanh nghiệp.

---

### Danh Sách Diễn Giả

*   **Quỳnh Mai:** MC chương trình.
*   **Nguyễn Gia Hưng:** Head of Solution Architect tại AWS Việt Nam, Người sáng lập FCAJ.
*   **Speaker 1 - Anh Tịnh:** Platform Engineer tại Gotam X.
*   **Speaker 2 - Chị Hải Anh:** Đang làm việc ở Pacific Việt Nam (từng present ở AWS Singapore Summit, Silicon Valley).
*   **Speaker 3 - Anh Thịnh:** DevOps Engineer.
*   **Speaker 4 - Nhóm UTM:** Developers (đồng nghiệp tại công ty chia sẻ về dự án thi Hackathon).
*   **Speaker 5 - Anh Đức:** Chia sẻ về kỹ thuật và tối ưu hóa của mô hình ngôn ngữ lớn (LLM Optimization).
*   **Speaker 6 - Chị Vy:** Đang công tác tại VPBank, chia sẻ về hệ thống Enterprise Multi-agent.
---

### Nội Dung Nổi Bật

#### 1. Tổng quan vấn đề thực tế
*   **Nhu cầu việc làm mới:** Trí tuệ nhân tạo (AI) giúp chi phí tạo ra phần mềm giảm đi đáng kể. Điều này kích cầu nhu cầu về phần mềm tăng mạnh, dẫn tới sự bùng nổ cơ hội việc làm trong mảng vận hành hạ tầng (Platform Engineering) và bảo trì/sửa lỗi (debug code do AI sinh ra).
*   **Hạn chế của AI:** Việc sinh mã nguồn bằng AI nhưng thiếu ngữ cảnh hệ thống sẽ sinh ra code rác, không đạt chuẩn và dễ gặp lỗi ảo giác (hallucination).

#### 2. Giải pháp được giới thiệu
*   **Thiết lập Prompt chuẩn:** Cần cung cấp ngữ cảnh (Context/System Prompt) rõ ràng khi tương tác với AI bao gồm: *Goal (Mục tiêu), Persona (Vai trò), Format (Định dạng kết quả)* thay vì đặt câu hỏi chung chung.
*   **Mô hình Multi-Agent:** Sử dụng hệ thống đa tác tử (Multi-Agent System) để phân chia và xử lý các bài toán phức tạp (ví dụ: phân tích tín dụng cho Startup) thay vì nhồi nhét mọi yêu cầu vào một mô hình đơn lẻ.

#### 3. Công nghệ, Dịch vụ và Công cụ
*   **AWS Services:** CloudFront (Flat-rate pricing, content compression, chống DDoS), AWS Bedrock, EC2, Lambda, VPC.
*   **AI/LLM:** Amazon Agent platform, Obsidian (xây dựng Second Brain quản lý tri thức), Model Context Protocol (MCP).
*   **Hạ tầng:** Terraform (Infrastructure as Code - IaC).

#### 4. Demo và Case Study thực tế
*   **Dự án UTM Morpo:** Demo công cụ dùng 3 AI agents chuyển đổi hình ảnh phác thảo thành code HTML/UI và cho phép người dùng kéo thả, chỉnh sửa trực tiếp trên giao diện (sản phẩm đạt giải Hackathon).
*   **Demo Tham số LLM:** So sánh chạy mô hình với tham số Temperature = 0 trên AWS Bedrock và môi trường local để chứng minh rằng trên môi trường Cloud Cloud, câu trả lời vẫn có sự biến thiên nhỏ do các cơ chế tối ưu hóa suy luận (Inference Optimization).
*   **Lưu ý nghiệp vụ:** Trong môi trường doanh nghiệp (Enterprise), việc tuân thủ bảo mật và đánh giá rủi ro (Guardrails, Security, Audit) là tối quan trọng, vượt lên trên số lượng công cụ tích hợp cho AI.

---

### Những Gì Học Được

#### 1. Tư duy và phương pháp kỹ thuật
*   LLM là một **Probabilistic Engine** (mô hình xác suất), do đó đừng mặc định nó luôn trả về kết quả giống hệt nhau dù thiết lập Temperature = 0.
*   Không phó mặc hoàn toàn cho AI chạy tự động (auto-pilot) mà luôn cần có sự kiểm duyệt của con người (**Human in the loop**).

#### 2. Kiến thức hạ tầng
*   Hiểu cách AWS CloudFront tối ưu chi phí thông qua cơ chế gói Flat-rate (trả phí cố định) giúp doanh nghiệp tránh rủi ro "bill sốc" do lượng traffic tăng đột biến hoặc bị tấn công DDoS.

#### 3. Best practices khi phát triển
*   Tránh hội chứng **"Internet Puller"** (sao chép code, thư viện trên mạng về dự án một cách máy móc mà không hiểu rõ bản chất và ngữ cảnh hoạt động).
*   Khi tham gia các cuộc thi Hackathon, cần kiểm soát phạm vi dự án (scope), tránh quá tải ý tưởng (over-generation) dẫn tới trễ hạn. Tập trung giải quyết một bài toán cốt lõi trong vòng 36 tiếng.

---

### Ứng Dụng Vào Công Việc
*   **Áp dụng cho dự án hiện tại:** Thiết kế hệ thống AI theo chuẩn Multi-agent: giao việc cụ thể cho từng agent chuyên biệt (ví dụ: Agent phân tích tài chính, Agent nghiên cứu thị trường). Thiết lập mTLS và VPC Origin để nâng cao bảo mật tài nguyên.
*   **Công nghệ muốn thử nghiệm:** Áp dụng Terraform để deploy hạ tầng bằng code (IaC) giúp quản lý phiên bản dễ dàng. Thử nghiệm các tính năng bảo vệ biên của AWS CloudFront (chặn truy cập theo khu vực, block bot).
*   **Cải thiện quy trình làm việc:** Thay vì tải dữ liệu thủ công, sử dụng AI Agent tích hợp với thư viện (như MCP kết nối Excel) để nó tự động tạo dashboard phân tích hoặc tóm tắt nội dung các cuộc họp.

---

### Trải Nghiệm Trong Event
*   **Học hỏi chuyên môn:** Thấy rõ tầm quan trọng của 5 yếu tố cốt lõi khi đi làm: *Salary (Lương), Experience (Kinh nghiệm), Network (Mạng lưới), Knowledge (Kiến thức) và Profile (Hồ sơ)*.
*   **Ý thức bảo mật:** Nhận thức sâu sắc cảnh báo về việc copy nguyên code từ ChatGPT dán vào hệ thống doanh nghiệp sẽ phá vỡ quy chuẩn viết code và tạo ra lỗ hổng bảo mật nghiêm trọng.

---

### Bài Học Rút Ra
*   **Kiến thức quan trọng nhất:** Kiến thức nền tảng (Foundation), bằng đại học và các kỹ năng phát triển phần mềm cơ bản (Software Engineering) vẫn là bắt buộc. AI chỉ là điểm cộng hỗ trợ tăng hiệu suất, không thể thay thế kỹ thuật phần mềm cốt lõi.
*   **Thuyết phục cấp quản lý:** Để đề xuất chi phí làm dự án AI trong doanh nghiệp, cần chỉ ra được tỷ suất hoàn vốn ROI và các con số tiết kiệm cụ thể thay vì nói chung chung.
*   **Quy tắc hệ thống:** Xây dựng hệ thống không chỉ hướng tới việc chạy được, mà nó *"phải chạy một cách an toàn, chạy đáng tin cậy và phục vụ đúng nhu cầu người dùng"*.

---

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh diễn giả chia sẻ slide Agenda](/images/4-EventParticipated/fcaj_community_day_2305_1.jpg)
*Hình 1: Diễn giả giới thiệu chương trình và nội dung chia sẻ của sự kiện*

![Slide Context is Everything](/images/4-EventParticipated/fcaj_community_day_2305_2.jpg)
*Hình 2: Chuyên đề "Context is Everything - Making AI Actually Work for You"*

![Trình bày dự án Hackathon](/images/4-EventParticipated/fcaj_community_day_2305_3.jpg)
*Hình 3: Diễn giả chia sẻ về hành trình phát triển dự án UTM Morpo trong 36 giờ*

![Ảnh lưu niệm tập thể FCAJ](/images/4-EventParticipated/fcaj_community_day_2305_4.jpg)
*Hình 4: Ảnh chụp tập thể lưu niệm cùng các chuyên gia và thành viên cộng đồng FCAJ*
