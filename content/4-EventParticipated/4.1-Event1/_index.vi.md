---
title: "Event 1"
date: 2026-06-06
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch kỹ thuật: FCAJ Technical Meetup #1

### Tổng quan sự kiện

* **Tên sự kiện:** FCAJ Technical Meetup #1 – Containerization, Bảo mật & GraphRAG
* **Thời gian:** Thứ Bảy, ngày 06/06/2026 (09:00 – 12:00)
* **Địa điểm:** Văn phòng AWS Việt Nam / Sinh hoạt cộng đồng
* **Vai trò:** Người tham dự

---

### Diễn giả & Nội dung trình bày kỹ thuật

1. **Bảo Huỳnh – *Docker: A Containerization Technology***
   * Phân tích cơ chế cô lập container, mô hình lưu trữ nhiều tầng (image layering) và các phương pháp tối ưu tệp Dockerfile.
   * Trình diễn điều phối container cục bộ bằng Docker Compose cho môi trường ứng dụng microservices.

2. **Lê Hoàng Gia Đại – *Combining AWS WAF with Machine Learning for Cyber Attack Detection on AWS***
   * Trình bày kiến trúc bảo mật kết hợp Amazon CloudWatch, Lambda và mô hình Machine Learning SageMaker để phát hiện lưu lượng web bất thường.
   * Minh họa tự động cập nhật IP set và rule group của AWS WAF để ngăn chặn các cuộc tấn công zero-day theo thời gian thực.

3. **Nguyễn Quốc Bảo – *Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets***
   * Giới thiệu kiến trúc game multiplayer thời gian thực sử dụng Amazon API Gateway WebSockets và AWS Lambda.
   * Giải thích phương pháp đồng bộ trạng thái, định tuyến message độ trễ thấp và xây dựng backend serverless cho game engine Godot.

4. **Trương Phước – *Phương pháp làm việc nhóm hiệu quả trong dự án công nghệ***
   * Chia sẻ kinh nghiệm thực tế về quản lý nhóm Agile/Scrum, quy chuẩn Git workflow và giao tiếp bất đồng bộ.
   * Nhấn mạnh các nguyên tắc giảm thiểu nợ kỹ thuật (technical debt) và nâng cao hiệu quả phối hợp giữa các thành viên.

5. **Vinh Trần – *Từ IT Helpdesk lên Senior Sysadmin: Hành trình tự học và Lộ trình dịch chuyển sang Cloud-DevOps***
   * Chia sẻ lộ trình phát triển sự nghiệp cá nhân từ hỗ trợ kỹ thuật IT đến quản trị hệ thống điện toán đám mây.
   * Phác thảo lộ trình tự học các chứng chỉ AWS (SAA, DVA, SAP), quản trị Linux và hạ tầng dưới dạng mã (Terraform).

6. **Việt Phát – *AWS Neptune for Building a Graph Knowledge Base for GraphRAG***
   * Phân tích chuyên sâu dịch vụ cơ sở dữ liệu đồ thị Amazon Neptune để mô hình hóa quan hệ dữ liệu doanh nghiệp phức tạp.
   * Trình diễn tích hợp Graph Knowledge Base với kỹ thuật Retrieval-Augmented Generation (GraphRAG) để nâng cao độ chính xác context cho các mô hình LLM.

---

### Bài học rút ra & Ứng dụng vào dự án

* **Áp dụng Containerization:** Áp dụng kỹ thuật Docker multi-stage build và container orchestration để đóng gói FastAPI backend và React frontend trong dự án Hệ thống Gợi ý Phim.
* **Tư duy bảo mật hạ tầng:** Tầm quan trọng của việc kết hợp giám sát tự động (CloudWatch + WAF) với chính sách phân quyền IAM tối thiểu.
* **Cơ sở dữ liệu tri thức AI:** Nắm bắt tư duy kết hợp giữa cơ sở dữ liệu Vector và Graph để xây dựng các pipeline suy luận AI tiên tiến.

---

### Minh chứng tham dự

![Minh chứng điểm danh - Meetup 06/06/2026](/images/4-EventParticipated/Event_6-6-2026_13-6-2026.png)

> **Xác nhận tham dự:** Ảnh chụp minh chứng điểm danh tham gia buổi FCAJ Technical Meetup #1 ngày 06/06/2026.
