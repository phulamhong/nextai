# NextAI Landing Page

Trang chủ của NextAI — giới thiệu các sản phẩm: HKD Pro (đã ra mắt), VNLaw (sắp ra mắt), LuatGT (sắp ra mắt).

🌐 **Live**: https://phulamhong.github.io/nextai/

## Stack

- HTML5 + CSS3 thuần (không dùng framework)
- Inter font qua Google Fonts
- GitHub Pages deploy
- No build step — chỉnh file → push → live

## Cấu trúc

```
nextai/
├── _config.yml       # Jekyll config
├── index.html        # single-page landing
├── assets/
│   └── css/style.css # custom styles (Linear/Supabase-inspired)
└── README.md
```

## Cập nhật nội dung

### Đổi text
Mở `index.html` → tìm đoạn cần đổi → sửa → commit + push.

### Đổi màu / typography
Mở `assets/css/style.css` → đổi CSS variables ở `:root` block.

### Thêm sản phẩm mới
1. Trong `index.html`, copy 1 `<div class="product-card">` block trong section `#products`
2. Đổi icon, tên, mô tả
3. Nếu là sản phẩm chính, thêm class `featured` + status `live`

## Local preview

```bash
# Mở file:// trong browser (đơn giản nhất)
open index.html

# Hoặc Python serve
python3 -m http.server 8000
# → http://localhost:8000

# Hoặc Jekyll preview (giống GitHub Pages)
bundle init
bundle add jekyll
bundle exec jekyll serve
# → http://localhost:4000/nextai/
```

## Deploy

```bash
git add .
git commit -m "your message"
git push

# GitHub Pages tự rebuild ~1-2 phút
# → https://phulamhong.github.io/nextai/
```

## Liên kết với các repo khác

- **Pháp lý**: links trong footer trỏ tới `phulamhong/legal` (https://phulamhong.github.io/legal/)
- **HKD Pro**: nút "Tải xuống" sẽ trỏ App Store / Play Store khi publish

## License

Source code và nội dung thuộc NextAI. Không cho phép sử dụng làm landing cho sản phẩm khác.
