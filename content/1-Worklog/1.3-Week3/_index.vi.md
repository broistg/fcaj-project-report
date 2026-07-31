---
title: "Nhật ký công việc Tuần 3"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3 (Proposal Giai đoạn 1 & Giai đoạn 3 - Web Component):

* Xây dựng khung ứng dụng backend FastAPI, môi trường Docker và tầng quản lý phụ thuộc AWS SDK (`app/container.py`).
* Triển khai các luồng xác thực: Mã hóa mật khẩu PBKDF2, xác thực phiên làm việc JWT (HS256) và khảo sát thể loại onboarding.
* Phát triển các API hiển thị danh mục phim để truy xuất metadata từ bảng DynamoDB `Movies` và `PopularMovies`.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Thiết lập cấu trúc dự án backend, đóng gói Docker container và nền tảng CI/CD cơ bản <br> - Khởi tạo Pydantic configuration (`app/core/config.py`) và Boto3 AWS factory (`app/aws/infrastructure.py`) | 29/06/2026 | 29/06/2026 | Yêu cầu Web Component Proposal |
| 3 | - Phát triển lớp `PasswordHasher` sử dụng thuật toán PBKDF2-HMAC-SHA256 <br> - Phát triển lớp `JWTService` thực hiện ký, xác thực và quản lý thời hạn access token | 30/06/2026 | 30/06/2026 | Hướng dẫn FastAPI Security |
| 4 | - Triển khai các repository DynamoDB (`UsersRepository`, `MoviesRepository`, `PopularMoviesRepository`) <br> - Xây dựng các route `/api/v1/auth/register`, `/login` và `/me` | 01/07/2026 | 01/07/2026 | Yêu cầu xác thực trong Proposal |
| 5 | - Phát triển endpoint `/api/v1/auth/onboarding` lưu sở thích thể loại cho người dùng mới đăng ký <br> - Xây dựng các endpoint metadata `/api/v1/movies` lấy thông tin chi tiết phim từ DynamoDB | 02/07/2026 | 02/07/2026 | API Metadata Giai đoạn 3 Proposal |
| 6 | - Bổ sung các kiểm tra khởi động (health check) xác minh AWS identity, schema DynamoDB và quyền truy cập S3 <br> - Viết bộ unit test backend bằng `unittest` đảm bảo hợp đồng API chính xác | 03/07/2026 | 03/07/2026 | Thư viện Python `unittest` |

### Kết quả đạt được Tuần 3:

* Xây dựng thành công kiến trúc backend FastAPI tuân thủ mô hình Presentation, Application và Hot Data layer trong Proposal.
* Triển khai hệ thống xác thực người dùng an toàn (PBKDF2 + JWT) kiểm tra dữ liệu trên bảng DynamoDB `Users`.
* Hoàn thành các API hiển thị metadata phim và luồng duyệt phim dành cho khách từ `PopularMovies` và `Movies`.
* Xác minh thành công tính hợp lệ của tài nguyên AWS khi khởi động và vượt qua toàn bộ bộ unit test.
