---
title: "Nhật ký công việc Tuần 3"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3 (Proposal Giai đoạn 1 - ML Data Infrastructure):

* Thiết lập hạ tầng lưu trữ S3 cho ML Data & Model Artifacts với các phân vùng dữ liệu chuyên biệt.
* Đưa ra yêu cầu thiết kế schema các bảng Amazon DynamoDB phục vụ thu thập dữ liệu tương tác người dùng (`UserInteractions`).
* Phát triển script Data Pipeline tiền xử lý dữ liệu Machine Learning từ nguồn file Kaggle CSV thô và xuất các tập Train/Validation/Test.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Triển khai Amazon S3 bucket tại `ap-southeast-1` với quy tắc S3 Lifecycle Rules (tự động xóa trọng số mô hình cũ sau 30 ngày) <br> - Thiết lập cấu trúc prefix phân vùng ML chuyên biệt (`datasets/raw/`, `datasets/processed/`, `models/`, `reports/`) | 22/06/2026 | 22/06/2026 | Đề xuất Tầng dữ liệu Proposal |
| 3 | - Đưa ra yêu cầu schema DynamoDB cho ML Data Ingestion: tạo bảng `UserInteractions` (PK `user_id`, SK `interaction_key`) lưu thông tin tương tác ngầm định <br> - Thống nhất cấu trúc bảng `Movies` (PK `movie_id`) lưu thông tin metadata phim | 23/06/2026 | 23/06/2026 | Hướng dẫn DynamoDB Developer |
| 4 | - Đưa ra yêu cầu thiết kế bảng `PopularMovies` (PK `list_id`, SK `rank`) lưu sẵn danh sách ứng viên gợi ý Popularity tính theo công thức trọng số IMDb phục vụ cold-start | 24/06/2026 | 24/06/2026 | Yêu cầu cơ sở dữ liệu Proposal |
| 5 | - Viết script Python Data Pipeline (`src/data/preprocess.py`) để tiền xử lý tập dữ liệu Kaggle/MovieLens thô <br> - Lọc giá trị khuyết thiếu, ánh xạ MovieLens ID sang TMDB catalog ID, trích xuất đặc trưng văn bản phim | 25/06/2026 | 25/06/2026 | Tài liệu Pandas & Scikit-Learn |
| 6 | - Thực thi phân tách dữ liệu tương tác đã xử lý thành các tập Train/Validation/Test theo mốc thời gian <br> - Tính toán bảng xếp hạng `PopularMovies` và xuất toàn bộ dữ liệu đã làm sạch lên S3 storage | 26/06/2026 | 26/06/2026 | Tài liệu Python Boto3 |

### Kết quả đạt được Tuần 3:

* Khởi tạo thành công S3 ML Storage với 7 phân vùng logic và quy tắc quản lý vòng đời trọng số mô hình.
* Đưa ra yêu cầu schema bảng `UserInteractions`, `Movies` và `PopularMovies` chuẩn hóa phục vụ nạp dữ liệu huấn luyện ML.
* Phát triển xong Python Data Pipeline làm sạch dữ liệu phim Kaggle, ánh xạ ID catalog thành công và xuất tập dữ liệu Train/Validation/Test lên S3.
