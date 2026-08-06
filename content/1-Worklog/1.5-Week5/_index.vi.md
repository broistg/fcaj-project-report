---
title: "Nhật ký công việc Tuần 5"
date: 2026-07-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5 (Proposal Giai đoạn 1 & Giai đoạn 3 - Web Component):

* Thiết kế UI/UX cơ bản và xây dựng giao diện ứng dụng Web phim trên Vite (React + TypeScript).
* Xây dựng các luồng Đăng ký, Đăng nhập và khảo sát thể loại Onboarding trên Vite.
* Xây dựng **Interaction Pipeline** hoàn chỉnh: Thu thập các sự kiện tương tác (`click`, `watch`, `rate`, `like`) từ Frontend và lưu vào bảng `UserInteractions` trên DynamoDB.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Khởi tạo cấu trúc dự án Vite React/TypeScript frontend và hệ thống màu dark-mode <br> - Xây dựng service `apiClient` tập trung tự động chèn header xác thực JWT | 06/07/2026 | 06/07/2026 | Đặc tả Frontend trong Proposal |
| 3 | - Xây dựng các component giao diện Đăng ký, Đăng nhập và trang Profile cá nhân <br> - Triển khai modal khảo sát Onboarding cho phép người dùng mới lựa chọn các thể loại phim yêu thích | 07/07/2026 | 07/07/2026 | Luồng Onboarding Proposal |
| 4 | - Xây dựng lưới danh mục phim, modal Chi tiết phim và trình phát phim mô phỏng dựa trên poster <br> - Kết nối state Frontend với các API metadata `/api/v1/movies` của backend | 08/07/2026 | 08/07/2026 | Màn hình chi tiết phim Proposal |
| 5 | - Triển khai backend `UserInteractionsRepository` và `InteractionService` <br> - Kết nối bộ xử lý tương tác Frontend (`click`, `watch >= 0.5`, `rate`, `like/dislike`, `share`) tới route `/api/v1/interactions` | 09/07/2026 | 09/07/2026 | Đặc tả Interaction Pipeline Proposal |
| 6 | - Cấu hình `docker-compose.yml` đóng gói ứng dụng React frontend (port 5173) và FastAPI backend (port 8000) <br> - Kiểm thử xác minh các sự kiện tương tác lưu thành công vào bảng DynamoDB `UserInteractions` | 10/07/2026 | 10/07/2026 | Môi trường Docker Proposal |

### Kết quả đạt được Tuần 5:

* Xây dựng giao diện web Vite/React hiện đại, mượt mà đáp ứng đầy đủ yêu cầu UI/UX trong Proposal.
* Hoàn thành các luồng Đăng ký/Đăng nhập và khảo sát thể loại Onboarding dành cho người dùng mới.
* Xây dựng thành công Interaction Pipeline thu thập đủ 5 loại tương tác ngầm định lưu trực tiếp vào DynamoDB `UserInteractions`.
* Đóng gói thành công môi trường container cục bộ bằng `docker-compose.yml` phục vụ kiểm thử tích hợp.
