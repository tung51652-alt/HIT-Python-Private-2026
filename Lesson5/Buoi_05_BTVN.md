# Buổi 05 · Thư viện mini

**Bối cảnh:** Mỗi cuốn sách cần biết mình đã được mượn hay chưa. Làm các bài trong `library.py`; dùng Python có sẵn, không cần cài gói.

## Bài 1 · Tạo hai cuốn sách

Viết class `Book(title, author)`. Lưu tên, tác giả và trạng thái mượn trong `__init__`; sách mới ở trạng thái chưa mượn. Viết `describe()` **trả** chuỗi dạng `"Tên sách — Tác giả"`.

```python
a = Book("Python cơ bản", "Linh")
b = Book("Git thực hành", "Hà")
```

**Đối chiếu:** `a.describe()` trả `"Python cơ bản — Linh"`; `b.describe()` trả `"Git thực hành — Hà"`.

## Bài 2 · Mượn và trả sách

Thêm property chỉ đọc `is_borrowed`, lấy trạng thái từ thuộc tính nội bộ của từng cuốn sách. Thêm hai phương thức:

- `borrow()`: nếu sách chưa mượn, đổi sang đã mượn và trả `True`; nếu đang mượn, giữ nguyên và trả `False`.
- `return_book()`: nếu sách đang mượn, đổi về chưa mượn và trả `True`; nếu chưa mượn, giữ nguyên và trả `False`.

**Ví dụ:** Mượn `a` lần đầu trả `True` và `a.is_borrowed` là `True`. Mượn lại ngay trả `False`. Gọi property bằng `a.is_borrowed`, không thêm dấu ngoặc.

## Bài 3 · Kiểm tra trạng thái độc lập

Tạo hai sách như bài 1, rồi gọi và in kết quả theo thứ tự:

| Thao tác | Kết quả |
|---|---|
| `a.borrow()` | `True` |
| `a.borrow()` | `False` |
| `b.is_borrowed` | `False` |
| `a.return_book()` | `True` |
| `a.is_borrowed` | `False` |
| `a.return_book()` | `False` |

**Thử thêm:** lưu lịch sử riêng cho mỗi sách, chỉ ghi thao tác thành công. Sau ví dụ trên, lịch sử của `a` là `["borrow", "return"]`, của `b` là `[]`.

**Nộp:** `buoi_05/library.py` có class và phần gọi thử; chạy bằng `python library.py`.
