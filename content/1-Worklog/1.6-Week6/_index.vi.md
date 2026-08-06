---
title: "Nhật ký công việc Tuần 6"
date: 2026-07-30
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6 (Proposal Giai đoạn 3 - Machine Learning Component):

* Xây dựng mô hình **Popularity Ranker** cho khách chưa đăng nhập và **Content-Based Recommender** cho người dùng mới.
* Phát triển mô hình cốt lõi **Collaborative Filtering** (Implicit ALS), chuyển đổi các sự kiện tương tác thành điểm số có trọng số.
* Triển khai thuật toán **Hybrid RRF** kết hợp các luồng ứng viên, xây dựng pipeline đánh giá offline và thiết lập **Promotion Gate** tự động.

### Công việc thực hiện trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Phát triển `PopularityRecommender` (công thức trọng số IMDb) cho khách chưa đăng nhập <br> - Phát triển `ContentRecommender` sử dụng trích xuất đặc trưng TF-IDF & độ tương đồng cosine | 13/07/2026 | 13/07/2026 | Đặc tả Popularity & Content Proposal |
| 3 | - Phát triển mô hình cốt lõi `ImplicitALSRecommender` (phân rã ma trận `implicit`) chuyển đổi tương tác người dùng thành ma trận điểm trọng số | 14/07/2026 | 14/07/2026 | Đặc tả Collaborative Filtering Proposal |
| 4 | - Triển khai `HybridRecommender` kết hợp Collaborative ALS, Content-Based và Popularity Fallback bằng thuật toán Weighted Reciprocal Rank Fusion (RRF) | 15/07/2026 | 15/07/2026 | Thuật toán Weighted RRF Proposal |
| 5 | - Xây dựng pipeline đánh giá định lượng offline (`evaluate.py`) đo lường HitRate@10, NDCG@10, độ phủ danh mục và độ đa dạng gợi ý | 16/07/2026 | 16/07/2026 | Chỉ số Information Retrieval |
| 6 | - Phát triển module **Promotion Gate** tự động (`promote.py`) đảm bảo 3 điều kiện: >1000 user được chấm điểm, vượt Popularity Baseline, giảm không quá 5% độ chính xác <br> - Đồng bộ trọng số mô hình và con trỏ phiên bản `LATEST.json` lên S3 | 17/07/2026 | 17/07/2026 | Cổng kiểm duyệt tự động Proposal |

### Kết quả đạt được Tuần 6:

* Xây dựng thành công cả 4 thuật toán gợi ý theo yêu cầu Giai đoạn 3 trong Proposal: Popularity, Content-Based, Implicit ALS và Hybrid Weighted RRF.
* Hoàn thành đánh giá định lượng trên 5.000 user test: Collaborative ALS đạt HitRate@10 = 0.1115 (tăng +235.8% so với baseline); mô hình Hybrid đạt HitRate@10 = 0.0818 (tăng +146.4% so với baseline) với độ phủ 17.85%.
* Giải quyết triệt để sự cố Cold-start cho người dùng mới nhờ tầng Fallback toàn cục trong mô hình Hybrid RRF.
* Triển khai logic Promotion Gate tự động kiểm tra mô hình trước khi xuất artifact lên S3.
