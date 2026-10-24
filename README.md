# Phân loại bệnh tim từ dữ liệu lâm sàng

## Tóm tắt

Mini project khảo sát bộ dữ liệu `heart.csv` và so sánh ba thuật toán phân loại: **K-Nearest Neighbors (KNN)**, **Decision Tree** và **Random Forest**. Quy trình bao gồm kiểm tra dữ liệu, phân tích khám phá (EDA), mã hóa biến phân loại, chuẩn hóa một số đặc trưng liên tục và đánh giá bằng cross-validation.

> Đây là dự án học thuật trên dữ liệu có sẵn, không phải công cụ chẩn đoán hay sàng lọc y khoa.

## Cấu trúc

```text
heart_disease_report/
├── notebooks/
│   └── Bao_cao_phan_loai_benh_tim.ipynb
├── docs/
│   └── GHI_CHU_PHUONG_PHAP.md
└── README.md
```

## Dữ liệu

Notebook yêu cầu file `heart.csv` trong thư mục làm việc. Output hiện có ghi nhận 303 dòng và 14 cột. Repository gốc chưa ghi URL nguồn dữ liệu và giấy phép; người nộp cần bổ sung thông tin này trước khi công bố hoặc sử dụng cho báo cáo chính thức.

## Cách chạy

1. Mở notebook trên Jupyter hoặc Google Colab.
2. Đưa `heart.csv` vào thư mục làm việc.
3. Chọn **Restart & Run All** để chạy tuần tự.

Các thư viện sử dụng gồm pandas, NumPy, Matplotlib, Seaborn và scikit-learn.

## Mô hình

- **K-Nearest Neighbors (KNN):** khảo sát `n_neighbors` từ 1 đến 20.
- **Decision Tree:** khảo sát `max_depth` từ 1 đến 10.
- **Random Forest:** khảo sát `n_estimators` từ 10 đến 100.

Accuracy được ước lượng bằng cross-validation. Các kết quả được lưu sẵn trong notebook là kết quả cũ; khi chạy lại, kết quả có thể thay đổi.

## Giới hạn cần nêu trong báo cáo

- Chưa có tập test độc lập.
- `StandardScaler` được khớp trước cross-validation, có nguy cơ rò rỉ thông tin thống kê.
- Chiến lược cross-validation không đồng nhất giữa các mô hình.
- Các mô hình cây chưa cố định `random_state`.
- Cần bổ sung Precision, Recall, F1-score và confusion matrix theo từng lớp.
- Cần ghi rõ nguồn và giấy phép của `heart.csv`.

## Phạm vi sử dụng

Chỉ sử dụng cho học tập và minh họa phương pháp Machine Learning. Không dùng để đưa ra quyết định lâm sàng.
