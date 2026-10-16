# Bố Cục Trang Web Với DIV và CSS

Bài thực hành CSS — Sử dụng thẻ `<div>` và các thuộc tính CSS để tạo bố cục (layout) đầy đủ cho một trang web.

---

## 🎯 Mục tiêu

- Hiểu cách chia trang web thành các phân vùng (section) bằng thẻ `<div>` với ID riêng biệt.
- Áp dụng `float: left` / `float: right` để tạo bố cục nhiều cột.
- Sử dụng `clear: both` để footer luôn nằm đúng vị trí.
- Biết cách căn giữa vùng nội dung bằng `margin: auto`.

---

## 📁 Cấu trúc dự án

```
div-layout/
├── index.html   # Cấu trúc HTML đầy đủ
├── style.css    # Định dạng CSS cho toàn bộ layout
└── README.md    # Mô tả dự án
```

---

## 🖥️ Bố cục trang

```
┌─────────────────────────────────────────┐
│              #head (Logo & Banner)       │
├─────────────────────────────────────────┤
│     #head-link (Home | Students | ...)  │
├──────────┬──────────────────┬───────────┤
│  #left   │    #content      │  #right   │
│ (200px)  │  (phần còn lại) │  (200px)  │
│  float:  │  margin-left:   │  float:   │
│  left    │  200px          │  right    │
│          │  margin-right:  │           │
│          │  200px          │           │
├──────────┴──────────────────┴───────────┤
│         #footer  (clear: both)          │
└─────────────────────────────────────────┘
```

---

## 🔑 CSS Selectors chính

| Selector | Vai trò kỹ thuật |
|---|---|
| `body` | Font chữ toàn trang |
| `#main` | `width: 980px; margin: auto` — cố định & căn giữa |
| `#head` | Logo & Banner — `height: 100px` |
| `#head-link` | Thanh nav — `overflow: hidden` |
| `#left` | `width: 200px; float: left` |
| `#right` | `width: 200px; float: right` |
| `#content` | `margin-left: 200px; margin-right: 200px` |
| `#footer` | `clear: both` — luôn nằm dưới hai cột |

---

## 📌 Kỹ thuật quan trọng

### Float + Margin để tạo 3 cột
```css
#left    { width: 200px; float: left;  }
#right   { width: 200px; float: right; }
#content { margin-left: 200px; margin-right: 200px; }
```
> `#content` **không float** — nó tự điền vào khoảng trống giữa nhờ margin.

### Footer dùng `clear: both`
```css
#footer { clear: both; }
```
> Không cần clearfix vì `#main` có `#footer` cuối cùng dùng `clear: both`.

---

## 🚀 Cách chạy

Mở file `index.html` trực tiếp trên trình duyệt — không cần server.

---

## 👤 Tác giả

- **Học viên:** Ha Thi My Binh
- **Khóa học:** CodeGym — Thực hành CSS Layout với DIV
