# Đồ án DS111: Hồi quy giá máy lạnh treo tường trên Tiki

Phân tích và dự đoán giá bán **máy lạnh treo tường** trên Tiki (229 sản phẩm, trích xuất từ bộ dữ liệu 60.014 sản phẩm tự crawl).

## Cấu trúc thư mục

```text
├── data/
│   ├── raw/                        # Dữ liệu thô (tiki_products_60k.jsonl & tiki_may_lanh_229.csv)
│   └── processed/                  # 4 tập dữ liệu đã qua pipeline xử lý (D1, D2, D3, D4)
├── 01_workbook_xu_ly_du_lieu.ipynb # Workbook 6 bước xử lý dữ liệu (bắt buộc)
├── 02_eda.ipynb                    # Phân tích khám phá dữ liệu (EDA - 7 mục theo Bài 04)
├── 03_kich_ban_xu_ly.ipynb         # Tạo 4 pipeline dữ liệu (R1/R2 × M1/M2)
├── 04_mo_hinh.ipynb                # Huấn luyện & đánh giá 8 kịch bản (+ Ridge) với RepeatedKFold 5×5
├── 05_insight.ipynb                # Trả lời 5 câu hỏi insight & trực quan hóa cuối
└── Plan đồ án DS111 (1).pdf        # Kế hoạch chi tiết đồ án
```

## Phân công

- **Người A:** `01_workbook_xu_ly_du_lieu.ipynb`, `03_kich_ban_xu_ly.ipynb`, `04_mo_hinh.ipynb`
- **Người B:** `02_eda.ipynb`, `05_insight.ipynb`
