---
title: "Nhật ký công việc Tuần 4"
date: 2026-07-30
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4 (Proposal Giai đoạn 1 & Giai đoạn 3 - Baseline Models & API Contract):

* Phát triển mô hình gợi ý cơ sở `PopularityRecommender` cho khách chưa đăng nhập và `ContentRecommender` (TF-IDF + Cosine Similarity) cho người dùng khảo sát onboarding.
* Định nghĩa hợp đồng giao tiếp interface `BaseRecommendationProvider` với bộ phận Backend để chuẩn hóa luồng gọi kết quả gợi ý.
* Xây dựng khung kiểm thử cục bộ cho các mô hình gợi ý đầu tiên.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng module `PopularityRecommender` triển khai công thức xếp hạng IMDb Weighted Rating $WR = \frac{v}{v+m}R + \frac{m}{v+m}C$ cho người dùng chưa đăng nhập <br> - Đóng gói logic truy xuất ứng viên phổ biến | 29/06/2026 | 29/06/2026 | Thuật toán Popularity Baseline |
| 3 | - Xây dựng module `ContentRecommender` trích xuất đặc trưng văn bản (overview, genres, keywords) bằng TF-IDF <br> - Tính toán ma trận độ tương đồng Cosine giữa sở thích thể loại onboarding của user với danh mục phim | 30/06/2026 | 30/06/2026 | Thuật toán Content-Based Filtering |
| 4 | - Định nghĩa hợp đồng giao tiếp ML interface `BaseRecommendationProvider` quy định phương thức `get_recommendations(user_id, k, context)` <br> - Thống nhất chuẩn format kết quả trả về (list movie IDs, score, strategy tag) với Backend team | 01/07/2026 | 01/07/2026 | Đặc tả Interface Backend & ML |
| 5 | - Xây dựng script kiểm thử cục bộ (`tests/test_recommenders.py`) xác minh tính chính xác của danh sách gợi ý Popularity và Content-Based <br> - Kiểm tra thời gian phản hồi suy luận cục bộ | 02/07/2026 | 02/07/2026 | Thư viện Python `unittest` |
| 6 | - Đóng gói các class mô hình gợi ý ban đầu thành thư viện Python nội bộ (`src/models/`) <br> - Viết unit test kiểm tra tính toàn vẹn của dữ liệu đầu vào và định dạng danh sách phim trả về | 03/07/2026 | 03/07/2026 | Cấu trúc Module Python |

### Kết quả đạt được Tuần 4:

* Hoàn thành xây dựng 2 mô hình gợi ý cơ sở đầu tiên: Popularity Ranker và Content-Based Recommender.
* Thống nhất thành công hợp đồng giao tiếp interface `BaseRecommendationProvider` với bộ phận Backend.
* Đóng gói các mô hình gợi ý ban đầu vào thư viện `src/models/` và vượt qua toàn bộ bộ unit test kiểm thử cục bộ.
