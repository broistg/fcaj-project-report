---
title: "Nhật ký công việc Tuần 3"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3 (Proposal Giai đoạn 1):

* Triển khai hạ tầng lưu trữ AWS: Cấu trúc Amazon S3 bucket và schema các bảng Amazon DynamoDB.
* Thực thi Data Pipeline tiền xử lý dữ liệu Machine Learning từ nguồn file Kaggle CSV thô.
* Phân tách tập dữ liệu đã làm sạch thành các tập Train, Validation và Test phục vụ huấn luyện mô hình.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Triển khai Amazon S3 bucket tại `ap-southeast-1` với quy tắc S3 Lifecycle Rules (tự động xóa artifact cũ sau 30 ngày) <br> - Thiết lập cấu trúc prefix (`datasets/raw/`, `datasets/processed/`, `models/`, `reports/`) | 22/06/2026 | 22/06/2026 | Đề xuất Tầng dữ liệu Proposal |
| 3 | - Thiết kế schema DynamoDB Hot Data: Khóa chính (PK) & Khóa sắp xếp (SK) <br> - Tạo bảng `Movies` (PK `movie_id`) và bảng `PopularMovies` (PK `list_id`, SK `rank`) trên AWS | 23/06/2026 | 23/06/2026 | Hướng dẫn DynamoDB Developer |
| 4 | - Tạo bảng `Users` (PK `user_id`), bảng `UserInteractions` (PK `user_id`, SK `interaction_key`) và bảng `RecommendationCache` | 24/06/2026 | 24/06/2026 | Yêu cầu cơ sở dữ liệu Proposal |
| 5 | - Viết script Python Data Pipeline để tiền xử lý tập dữ liệu Kaggle/MovieLens thô <br> - Lọc giá trị khuyết thiếu, trích xuất đặc trưng phim và ánh xạ MovieLens ID sang TMDB catalog ID | 25/06/2026 | 25/06/2026 | Tài liệu Pandas & Scikit-Learn |
| 6 | - Phân tách dữ liệu tương tác đã xử lý thành các tập Train/Validation/Test theo thời gian <br> - Nạp bản ghi danh mục phim vào bảng DynamoDB `Movies` và xếp hạng `PopularMovies` tính sẵn | 26/06/2026 | 26/06/2026 | Tài liệu Python Boto3 |

### Kết quả đạt được Tuần 3:

* Triển khai thành công S3 Cold Storage Data với 7 phân vùng logic và quy tắc quản lý vòng đời dữ liệu.
* Khởi tạo thành công 5 bảng DynamoDB Hot Data trên AWS khớp chính xác với thiết kế trong Proposal.
* Làm sạch dữ liệu phim Kaggle, xuất thành công các tập Train/Validation/Test lên S3.
* Nạp danh mục phim TMDB vào bảng `Movies` và lưu danh sách xếp hạng `PopularMovies` tính theo trọng số IMDb.
