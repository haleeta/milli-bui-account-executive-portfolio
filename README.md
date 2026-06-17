# 📘 Hướng dẫn sửa website & đẩy lên GitHub (cho người mới)

Repo của bạn: **https://github.com/haleeta/milli-bui-account-executive-portfolio**

Hình dung đơn giản như **mượn tài liệu về sửa rồi trả lại**:
- **Clone / Pull** = tải bản mới nhất về máy
- **Sửa file** trên máy
- **Commit** = đóng gói thay đổi + ghi chú "đã sửa gì"
- **Push** = gửi trả lại lên GitHub

> Khi đã nối với Vercel, **mỗi lần push xong web live tự cập nhật** sau ~30 giây. Không cần làm gì thêm.

---

## 🔧 CHUẨN BỊ (chỉ làm 1 lần trên máy mới)

### 1. Cài Git
- Mở **Terminal** (bấm `Cmd + Space`, gõ "Terminal", Enter)
- Gõ: `git --version`
- Nếu báo chưa có → máy sẽ tự hỏi cài, bấm **Install**. Hoặc tải tại https://git-scm.com

### 2. Khai báo tên & email (để GitHub biết ai sửa)
```bash
git config --global user.name "Milli Bui"
git config --global user.email "mybuiforwork21@gmail.com"
```

### 3. Cài VS Code (app để sửa code, dễ dùng)
- Tải tại https://code.visualstudio.com → cài như app bình thường

---

## 🟢 BƯỚC 1 — Lấy code về máy (làm 1 lần)

Mở Terminal, gõ từng dòng (Enter sau mỗi dòng):

```bash
cd ~/Downloads
git clone https://github.com/haleeta/milli-bui-account-executive-portfolio.git
cd milli-bui-account-executive-portfolio
```

→ Code được tải về thư mục `~/Downloads/milli-bui-account-executive-portfolio`

> Lần đầu push/clone, GitHub có thể hỏi đăng nhập. Làm theo hướng dẫn ở **phần ⚠️ cuối file**.

---

## 🟡 BƯỚC 2 — Sửa code

### a) Luôn tải bản mới nhất về TRƯỚC khi sửa
```bash
cd ~/Downloads/milli-bui-account-executive-portfolio
git pull
```

### b) Mở thư mục bằng VS Code
```bash
code .
```
(dấu chấm nghĩa là "mở thư mục hiện tại")

### c) Sửa nội dung
- File chính là **`index.html`**
- Nội dung các dự án (tên, mô tả, số liệu...) nằm trong phần `projectsData` ở gần đầu file
- Sửa xong nhớ **bấm `Cmd + S`** để lưu

> ⚠️ Lưu ý: code trang đã được "dịch sẵn" (kiểu `React.createElement`), hơi khó đọc.
> Nếu cần sửa nhiều/phức tạp → nhắn lại để được hỗ trợ, đừng sửa liều kẻo lỗi.
> Còn chỉ đổi **chữ, số, tên** thì cứ tìm đúng đoạn text và thay là được.

### d) Xem thử trước khi đẩy lên
- Bấm đúp vào file `index.html` để mở bằng trình duyệt, kiểm tra ổn chưa

---

## 🟢 BƯỚC 3 — Đẩy thay đổi lên GitHub

Trong Terminal (vẫn ở trong thư mục dự án), gõ 3 dòng:

```bash
git add -A
git commit -m "Mô tả ngắn việc vừa sửa, vd: cap nhat so lieu du an Habeco"
git push
```

Xong! Đợi ~30 giây, web live trên Vercel sẽ tự cập nhật. 🎉

---

## 📋 BẢNG LỆNH BỎ TÚI (copy dùng mỗi lần)

```bash
# Vào thư mục dự án
cd ~/Downloads/milli-bui-account-executive-portfolio

# 1. Tải bản mới nhất
git pull

# 2. (sửa file index.html, lưu Cmd+S)

# 3. Đẩy lên
git add -A
git commit -m "ghi chu viec vua sua"
git push
```

---

## ⚠️ ĐĂNG NHẬP GITHUB (lần đầu push thường bị hỏi)

GitHub **không cho dùng mật khẩu thường** khi push. Cần "chìa khóa" gọi là **Personal Access Token**:

1. Vào https://github.com/settings/tokens
2. Bấm **Generate new token** → chọn **Generate new token (classic)**
3. Đặt tên bất kỳ (vd "macbook cua toi")
4. **Expiration:** chọn **No expiration** (hoặc 90 ngày)
5. Tích vào ô **`repo`** (cho phép sửa kho code)
6. Kéo xuống bấm **Generate token**
7. **Copy chuỗi token** hiện ra (chỉ hiện 1 lần, lưu lại chỗ an toàn!)

→ Khi Terminal hỏi:
- **Username:** gõ tên GitHub của bạn (vd `haleeta`)
- **Password:** **dán cái token vừa copy** (KHÔNG phải mật khẩu thường)

> Máy sẽ nhớ token cho các lần sau, không phải nhập lại.

---

## 🆘 GẶP LỖI?

| Lỗi | Cách xử lý |
|-----|-----------|
| `Authentication failed` | Sai token → tạo lại token (phần ⚠️ trên) |
| `Updates were rejected` | Có người sửa trước → gõ `git pull` rồi `git push` lại |
| `not a git repository` | Bạn đang đứng sai thư mục → gõ lại `cd ~/Downloads/milli-bui-account-executive-portfolio` |
| Web không cập nhật | Đợi 1-2 phút; kiểm tra trên vercel.com xem deploy xong chưa |

Kẹt chỗ nào cứ chụp màn hình gửi lại để được hỗ trợ nhé!
