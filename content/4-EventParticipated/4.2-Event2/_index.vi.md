---
title: "Event 2"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch kỹ thuật: FCAJ Technical Meetup #2

### Tổng quan sự kiện

* **Tên sự kiện:** FCAJ Technical Meetup #2 – Giải pháp Cloud Architecture & Kinh nghiệm thực thi
* **Thời gian:** Thứ Bảy, ngày 13/06/2026 (09:00 – 12:00)
* **Địa điểm:** Văn phòng AWS Việt Nam / Sinh hoạt cộng đồng
* **Vai trò:** Người tham dự

---

### Diễn giả & Nội dung trình bày kỹ thuật

1. **Hoàng Trọng – *AWS Cloud Architecture Patterns & Tính khả dụng hệ thống***
   * Phân tích các mô hình kiến trúc độ sẵn sàng cao trên nhiều Availability Zone (Multi-AZ).
   * Thảo luận các chiến lược khôi phục sau thảm họa (Backup & Restore, Pilot Light, Warm Standby) và tự động mở rộng tài nguyên (Auto Scaling) đảm bảo vận hành liên tục.

2. **Cường Nguyễn & Đạt Phạm – *Phát triển ứng dụng hiện đại & Tích hợp điện toán đám mây***
   * Chia sẻ các kiến trúc microservices RESTful và phương pháp tích hợp AWS SDK vào ứng dụng đóng gói container.
   * Phân tích chiến lược tách biệt dữ liệu giữa tầng lưu trữ nóng tốc độ cao (DynamoDB) và tầng lưu trữ lạnh lâu dài (Amazon S3).

3. **Nghi Danh (Hiếu Nghị) – *Quản trị an ninh Cloud & Quản lý định danh (IAM)***
   * Trình bày các nguyên tắc phân quyền IAM role, kiểm soát truy cập dựa trên thuộc tính (ABAC) và bảo mật thông tin bí mật với AWS Secrets Manager.
   * Nhấn mạnh tầm quan trọng của việc ghi log audit tuân thủ sử dụng AWS CloudTrail và Amazon CloudWatch.

4. **Kiên & Thọ – *Chiến lược dịch chuyển Cloud & Tự động hóa hạ tầng***
   * Giới thiệu phương pháp luận dịch chuyển hệ thống lên đám mây (khung 7Rs: Rehost, Replatform, Refactor,...) cho doanh nghiệp.
   * Trình diễn tự động hóa khởi tạo hạ tầng bằng Infrastructure as Code (IaC) và các pipeline triển khai liên tục (CI/CD).

---

### Bài học rút ra & Ứng dụng vào dự án

* **Tách biệt tầng dữ liệu Hot/Cold:** Áp dụng trực tiếp nguyên lý phân tách dữ liệu được chia sẻ bởi anh Cường & anh Đạt để thiết kế hệ thống gợi ý phim (bảng DynamoDB quản lý tương tác nóng, S3 lưu trữ dữ liệu thô và mô hình ML).
* **Quản trị an toàn IAM:** Thiết lập các IAM execution role chặt chẽ cho EC2 instance và SageMaker processing jobs tuân thủ nguyên tắc phân quyền tối thiểu.
* **Tối ưu chi phí & Độ tin cậy:** Đưa các tiêu chuẩn kiến trúc Multi-AZ và cảnh báo AWS Budgets vào dự án để kiểm soát rủi ro chi phí hạ tầng.

---

### Minh chứng tham dự

![Minh chứng điểm danh - Meetup 13/06/2026](/images/4-EventParticipated/Event_6-6-2026_13-6-2026.png)

> **Xác nhận tham dự:** Ảnh chụp minh chứng điểm danh tham gia buổi FCAJ Technical Meetup #2 ngày 13/06/2026.
