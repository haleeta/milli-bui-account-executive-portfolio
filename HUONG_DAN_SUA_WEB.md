# 📘 Hướng dẫn sửa website (dùng VS Code, không cần gõ lệnh)

Web của bạn: **https://github.com/haleeta/milli-bui-account-executive-portfolio**

Quy trình gói gọn trong 4 nhịp:
1. **Lấy code về** (làm 1 lần)
2. **Pull** = tải bản mới nhất trước khi sửa
3. **Sửa file** trong VS Code
4. **Commit + Push** = gửi thay đổi lên → web live **tự cập nhật** sau ~30 giây

> 💡 Mọi thao tác git đều bấm nút ngay trong VS Code, **không cần dùng Terminal**.

---

## 🟢 PHẦN 1 — Lấy code về máy (chỉ làm 1 lần đầu)

1. Mở **VS Code**
2. Bấm `Cmd + Shift + P` → gõ **"Git Clone"** → Enter
3. Dán link này vào:
   ```
   https://github.com/haleeta/milli-bui-account-executive-portfolio.git
   ```
4. Chọn nơi lưu (ví dụ thư mục **Downloads**)
5. Khi hỏi "Open the cloned repository?" → bấm **Open**

→ Code đã về máy, mở sẵn trong VS Code. Xong!

> Lần đầu có thể bị hỏi đăng nhập GitHub → xem **PHẦN 5** ở cuối.

---

## 🟡 PHẦN 2 — Trước khi sửa: bấm PULL (tải bản mới nhất)

Mỗi lần ngồi vào sửa, **luôn pull trước** để chắc chắn bạn đang sửa trên bản mới nhất:

- Nhìn **góc dưới cùng bên trái** VS Code → có biểu tượng **🔄 (vòng tròn xoay)** cạnh tên nhánh `main`
- **Bấm vào biểu tượng 🔄 đó** → VS Code tự tải bản mới về

Vậy là xong bước pull.

---

## 🟡 PHẦN 3 — Sửa nội dung

- File chính cần sửa: **`index.html`**
- Nội dung các dự án (tên, mô tả, số liệu...) nằm ở phần **`projectsData`** gần đầu file
  - Mẹo: bấm `Cmd + F` để **tìm** đúng chữ muốn sửa cho nhanh
- Sửa xong nhớ bấm **`Cmd + S`** để lưu

> ⚠️ **Quan trọng:** code trang đã được "dịch sẵn" (kiểu `React.createElement`), hơi khó đọc.
> - ✅ Chỉ nên đổi **chữ, số, tên, đường link** trong dấu ngoặc kép `" "`
> - ❌ Đừng xóa/đổi các dấu `(`, `)`, `{`, `}`, `,` — sai một dấu là web trắng trang
> - Cần sửa nhiều/phức tạp → nhắn lại để được hỗ trợ, đừng sửa liều

### Xem thử trước khi đẩy lên
- Bấm đúp vào file `index.html` ngoài Finder để mở bằng trình duyệt, kiểm tra ổn chưa

---

## 🟢 PHẦN 4 — Đẩy lên (Commit + Push)

Vẫn trong VS Code:

1. Bấm vào biểu tượng **Source Control** ở thanh dọc bên trái (icon hình **nhánh cây 🔀**, hoặc bấm `Cmd + Shift + G`)
2. Bạn sẽ thấy danh sách file vừa sửa
3. Ô **"Message"** phía trên → gõ ghi chú ngắn, ví dụ: *"cap nhat so lieu du an Habeco"*
4. Bấm nút **✓ Commit**
   - Nếu hỏi "stage all changes?" → bấm **Yes**
5. Bấm nút **Sync Changes** (hoặc **Push**) hiện ra sau đó

→ Xong! Đợi ~30 giây, web live tự cập nhật. 🎉

**🌐 Link web live của bạn:** https://milli-bui-account-executive-portfolio.vercel.app
> Đây là link gửi cho mọi người / để trong CV. Link này cố định, không đổi.

---

## 🎬 THÊM VIDEO NỀN TRANG CHỦ (nếu muốn)

Trang chủ có chỗ để **video chạy nền** phía sau dòng chữ "Account Executive".
Hiện đang để **nền đen** (vẫn đẹp). Muốn thêm video thì làm vầy:

1. Chuẩn bị 1 video ngắn (chạy lặp, không cần tiếng — web tự tắt tiếng)
2. **Đổi tên** file video thành đúng: **`background_video_layer.mp4`**
3. **Copy** file đó vào **thư mục gốc** của dự án (cùng chỗ với file `index.html`)
4. Trong VS Code: **Commit + Push** như Phần 4

→ Web sẽ tự lấy video làm nền (mờ 40%, có phủ tối để chữ trắng vẫn rõ).

> ⚠️ Tên file phải **chính xác** `background_video_layer.mp4` (đuôi `.mp4`), sai một chữ là không hiện.
> Nếu video bạn có đuôi khác (`.mov`, `.webm`) → đừng đổi đuôi liều, nhắn lại để được chỉnh cho đúng.

---

## 🔁 TÓM TẮT MỖI LẦN SỬA (ghi nhớ 4 bước)

| Bước | Làm gì | Ở đâu |
|------|--------|-------|
| 1️⃣ Pull | Bấm 🔄 góc dưới trái | Tải bản mới về |
| 2️⃣ Sửa | Mở `index.html`, sửa, `Cmd+S` | Soạn thảo |
| 3️⃣ Commit | Gõ ghi chú + bấm ✓ Commit | Source Control |
| 4️⃣ Push | Bấm Sync / Push | Gửi lên → web tự update |

---

## ⚠️ PHẦN 5 — Đăng nhập GitHub (lần đầu thường bị hỏi)

Cách dễ nhất: **để VS Code tự lo**.
- Khi push lần đầu, VS Code hiện popup **"Sign in with GitHub"** → bấm vào, trình duyệt mở ra → bấm **Authorize** → xong, máy tự nhớ.

Nếu nó hỏi username/password kiểu cũ thì cần **token** (không dùng mật khẩu thường):
1. Vào https://github.com/settings/tokens
2. **Generate new token** → **(classic)**
3. Đặt tên bất kỳ, Expiration chọn **No expiration**
4. Tích ô **`repo`** → kéo xuống **Generate token**
5. **Copy** chuỗi token (chỉ hiện 1 lần!)
6. Khi máy hỏi Password → **dán token** (không phải mật khẩu)

---

## 🆘 GẶP LỖI?

| Tình huống | Cách xử lý |
|-----------|-----------|
| Web bị trắng trang sau khi sửa | Có thể lỡ xóa nhầm dấu ngoặc → bấm pull lại bản cũ, hoặc nhắn nhờ hỗ trợ |
| Push báo "rejected / behind" | Bấm 🔄 (Pull) trước, rồi Push lại |
| Đăng nhập thất bại | Tạo lại token (Phần 5) |
| Web không cập nhật | Đợi 1–2 phút; vào vercel.com xem deploy xong chưa |

Kẹt chỗ nào cứ chụp màn hình gửi lại nhé!
