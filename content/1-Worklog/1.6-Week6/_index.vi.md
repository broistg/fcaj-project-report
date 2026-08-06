---
title: "Nhật ký công việc Tuần 6"
date: 2026-07-30
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6 (Proposal Giai đoạn 3 - Core ML Algorithms, Evaluation & Promotion Gate):

* Khởi tạo mô hình cốt lõi **Collaborative Filtering** (Implicit ALS) phân rã ma trận tương tác người dùng.
* Phát triển mô hình lai ghép **Hybrid Weighted RRF** kết hợp các luồng ứng viên Popularity, Content-Based và ALS.
* Xây dựng khung đánh giá định lượng Offline (`evaluate.py`) đo lường chỉ số IR và triển khai logic **Promotion Gate** tự động (`promote.py`).

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng mô hình cốt lõi `ImplicitALSRecommender` dựa trên thuật toán Phân rã ma trận Alternating Least Squares (Implicit ALS) <br> - Thử nghiệm điều chỉnh siêu tham số `factors=64`, `regularization=0.05`, `iterations=20` | 13/07/2026 | 13/07/2026 | Thư viện Python `implicit` |
| 3 | - Triển khai mô hình lai ghép `HybridRecommender` kết hợp các ứng viên từ ALS, Content-Based và Popularity bằng thuật toán Weighted Reciprocal Rank Fusion (Weighted RRF): $RRF(d) = \sum_{m \in M} w_m \cdot \frac{1}{k + r_m(d)}$ | 14/07/2026 | 14/07/2026 | Thuật toán Weighted RRF |
| 4 | - Xây dựng framework đánh giá định lượng offline (`evaluate.py`) đo lường các chỉ số Information Retrieval: HitRate@10, NDCG@10, Catalog Coverage, và Recommendation Diversity | 15/07/2026 | 15/07/2026 | Chỉ số Đánh giá Mô hình IR |
| 5 | - Thực thi đánh giá trên 5.000 user test: Implicit ALS đạt HitRate@10 = 0.1115 (+235.8% so với baseline); Hybrid RRF đạt HitRate@10 = 0.0818 (+146.4% so với baseline) với độ phủ 17.85% giải quyết cold-start | 16/07/2026 | 16/07/2026 | Báo cáo Đánh giá Mô hình ML |
| 6 | - Phát triển module **Promotion Gate** tự động (`promote.py`) đảm bảo 3 điều kiện: >1000 user chấm điểm, vượt Popularity Baseline, không suy giảm >5% độ chính xác <br> - Tự động cập nhật con trỏ `LATEST.json` lên S3 | 17/07/2026 | 17/07/2026 | Cổng Kiểm duyệt Mô hình Proposal |

### Kết quả đạt được Tuần 6:

* Xây dựng thành công mô hình cốt lõi Implicit ALS và mô hình lai ghép Hybrid Weighted RRF giải quyết triệt để vấn đề Cold-start.
* Hoàn thành bộ đánh giá offline đo lường định lượng các chỉ số HitRate@10, NDCG@10 và catalog coverage trên 5.000 user test.
* Triển khai module Promotion Gate tự động đảm bảo chất lượng mô hình trước khi xuất artifact weight lên S3 storage.
