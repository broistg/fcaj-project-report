---
title: "Nhật ký công việc Tuần 5"
date: 2026-07-30
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5 (Proposal Giai đoạn 3 - Implicit Interaction Pipeline & Data Weighting):

* Thiết kế công thức chuyển đổi các sự kiện tương tác ngầm định (`click`, `watch >= 0.5`, `rate`, `like/dislike`, `share`) thành điểm số trọng số tương tác (Implicit Confidence Scores).
* Xây dựng module nạp dữ liệu (data loader) trích xuất bản ghi từ DynamoDB `UserInteractions` phục vụ nạp vào ma trận huấn luyện Collaborative Filtering.
* Kiểm thử quy trình tự động đẩy file snapshot tương tác từ DynamoDB lên S3 prefix `datasets/processed/interactions/`.

### Công việc đã hoàn thành trong tuần:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế bảng ma trận trọng số tương tác ngầm định: gán điểm số tin cậy (confidence score) cho các sự kiện `click` (+1), `watch >= 50%` (+3), `rate 1-5` (+rating), `like` (+2), `dislike` (-2), `share` (+4) <br> - Chuẩn hóa thang điểm tương tác | 06/07/2026 | 06/07/2026 | Lý thuyết Implicit Feedback ML |
| 3 | - Xây dựng module `InteractionDataIngestor` trích xuất bản ghi tương tác từ bảng DynamoDB `UserInteractions` <br> - Chuyển đổi dữ liệu tương tác thô thành ma trận thưa User-Item | 07/07/2026 | 07/07/2026 | Cấu trúc dữ liệu SciPy Sparse |
| 4 | - Xây dựng quy trình chuẩn hóa ma trận User-Item Interaction Matrix $R_{u,i}$ và biến đổi thành định dạng `scipy.sparse.csr_matrix` <br> - Thiết lập ánh xạ chỉ mục user_id và movie_id sang ma trận | 08/07/2026 | 08/07/2026 | Thuật toán Matrix Factorization |
| 5 | - Viết script xuất dữ liệu tương tác định kỳ (`scripts/export_interactions.py`) đẩy file snapshot Parquet/CSV lên S3 prefix `datasets/processed/interactions/` <br> - Kiểm tra tính toàn vẹn của dữ liệu nạp | 09/07/2026 | 09/07/2026 | Tài liệu AWS S3 & Pandas |
| 6 | - Kiểm thử luồng dữ liệu end-to-end từ sự kiện tương tác thô trong DynamoDB đến ma trận thưa nạp vào bộ nhớ cục bộ <br> - Sẵn sàng tập dữ liệu đầu vào cho giai đoạn huấn luyện Collaborative Filtering | 10/07/2026 | 10/07/2026 | Kiểm thử ML Pipeline |

### Kết quả đạt được Tuần 5:

* Thiết kế thành công mô hình gán trọng số tương tác ngầm định (Implicit Confidence Rating Scheme) biến các hành vi ngầm của user thành điểm số học máy.
* Xây dựng xong module `InteractionDataIngestor` biến đổi dữ liệu DynamoDB `UserInteractions` thành dạng ma trận thưa `csr_matrix`.
* Tự động hóa pipeline xuất dữ liệu tương tác định kỳ từ DynamoDB lên S3 storage sẵn sàng phục vụ huấn luyện mô hình Collaborative Filtering.
