# Đồ án DS111: Hồi quy giá máy lạnh treo tường trên Tiki

Phân tích dữ liệu và dự đoán giá bán **máy lạnh treo tường** trên Tiki (**229 sản phẩm**, 24 thương hiệu), trích xuất từ bộ dữ liệu **60.014 sản phẩm** (16 cột) do nhóm tự crawl.

## Cấu trúc thư mục hiện tại

```text
├── data/
│   ├── raw/
│   │   ├── tiki_may_lanh_229.csv       # 229 sản phẩm Máy lạnh treo tường đã lọc
│   │   └── tiki_products_60k.jsonl     # (Local only, .gitignore) 60.014 sản phẩm gốc
│   └── processed/                      # Chờ dữ liệu sau xử lý
├── 01_workbook_xu_ly_du_lieu.ipynb     # Bước 1: Thu thập & lọc ngành hàng Máy lạnh treo tường
├── 02_eda.ipynb                        # Bước 1 EDA: Cấu trúc dữ liệu & dán nhãn biến (.attrs)
├── .gitignore
└── README.md
```

## Tiến độ đã thực hiện

- **Bước 1 — Thu thập & lọc dữ liệu (`01_workbook_xu_ly_du_lieu.ipynb`):**
  - Đọc bộ dữ liệu gốc `tiki_products_60k.jsonl` (60.014 dòng, 16 cột).
  - Thống kê các ngành lá có $\ge 150$ sản phẩm (77 ngành) và lọc ra ngành `Máy lạnh treo tường` (229 sản phẩm, 24 thương hiệu).
  - Lưu ra `data/raw/tiki_may_lanh_229.csv`.
- **Bước 1 EDA — Cấu trúc dữ liệu (`02_eda.ipynb` — Người B):**
  - Kiểm tra `shape`, `dtypes`, `info()`, `head()`, `tail()`.
  - Phân loại biến bằng `select_dtypes` và dán nhãn chi tiết từng cột bằng `.attrs` (`'Định tính'`, `'Định lượng rời rạc'`, `'Định lượng'`).

## Quy trình làm việc với Git

```powershell
# Kéo code mới nhất trước khi làm
git pull

# Lưu thay đổi và đẩy lên GitHub
git add <tên_file>
git commit -m "mo ta ngan gon thay doi"
git push
```
