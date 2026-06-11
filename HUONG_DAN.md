# DOV PHỐ HIẾN — Trang tuyển dụng Sale Bất Động Sản

Trang landing 1 trang (single page), responsive, HTML/CSS/JS thuần — **không cần framework, không cần backend**.

## 1. Chạy ngay
- Mở thẳng file **`index.html`** bằng trình duyệt (nhấp đúp) là chạy được.
- Ảnh và logo đã được **nhúng sẵn vào file** (base64) nên không lo lỗi đường dẫn khi gửi/đăng tải.
- Cần internet lần đầu để tải font Google (Playfair Display, Montserrat, Roboto). Nếu offline, trang vẫn hiển thị với font hệ thống.

## 2. Sửa nội dung tiếng Việt
Mở `index.html` bằng Notepad / VS Code, tìm nhanh theo nhãn comment `<!-- ... -->`:

| Mục | Tìm chữ |
|---|---|
| Tiêu đề Hero | `============ HERO ============` |
| Giới thiệu công ty | `============ GIỚI THIỆU ============` |
| Thu nhập & lợi ích | `============ THU NHẬP` |
| Lộ trình thăng tiến (mức lương) | `============ LỘ TRÌNH` |
| Yêu cầu ứng viên | `============ YÊU CẦU ============` |
| Câu nói CEO | `============ THÔNG ĐIỆP CEO` |
| Địa chỉ 4 văn phòng | `============ VĂN PHÒNG ============` |
| Hotline & form | `============ ỨNG TUYỂN ============` |
| Footer | `============ FOOTER ============` |

Số hotline đang dùng: **0924.89.1111** và **0977.418.222** (đổi cả phần `href="tel:..."` lẫn chữ hiển thị).

## 3. Đổi màu & font
Toàn bộ màu/font khai báo ở đầu thẻ `<style>`, trong khối `:root{ ... }`:
```css
--navy:#1a365d;     /* xanh navy chủ đạo */
--gold:#d4af37;     /* vàng gold */
--mist:#f7f7f7;     /* nền xám nhạt */
--f-display: ...    /* font tiêu đề sang trọng */
```
Đổi 1 giá trị ở đây, toàn trang tự cập nhật.

## 4. Thay logo / ảnh
**Cách A — đơn giản (giữ kiểu nhúng):** mình đã tối ưu sẵn ảnh trong thư mục `assets/`
(`logo.webp`, `poster-recruit.webp`, `poster-income.webp`, `poster-culture.webp`, `poster-ceo.webp`).
Muốn thay ảnh mới: bảo mình "nhúng lại ảnh này" kèm file, mình sẽ build lại `index.html`.

**Cách B — dùng file ảnh rời:** thay các chuỗi `src="data:image..."` rất dài bằng đường dẫn file, ví dụ:
```html
<img src="assets/logo.webp" ... >
<img src="assets/poster-recruit.webp" ... >
```
rồi để file `index.html` cùng thư mục với `assets/`. Cách này giúp file HTML nhẹ hơn nhiều.

> Ảnh nên để **dạng vuông** (poster) hoặc **tròn** (logo). Nếu ảnh quá nặng, nén về WebP ~1000px, chất lượng 70–75 là đẹp và nhẹ.

## 5. Đăng lên mạng (miễn phí)
- **Netlify:** vào netlify.com → kéo–thả cả thư mục (gồm `index.html` + `assets/`) vào ô Deploy → có link ngay.
- **GitHub Pages:** tạo repo → upload file → Settings › Pages › chọn nhánh `main` › Save.
- **Hosting thường (cPanel):** upload vào thư mục `public_html/`.

## 6. Lưu ý
- **Form ứng tuyển** hiện chỉ mô phỏng (kiểm tra dữ liệu + hiện thông báo cảm ơn), **chưa gửi về email/server**. Muốn nhận đơn thật, có thể nối Google Form, Formspree, hoặc API riêng — mình hỗ trợ thêm khi cần.
- Section **"Lộ trình thăng tiến"** được dựng lại bằng HTML (thay vì dùng ảnh poster) để hiển thị sắc nét và co giãn tốt trên điện thoại; số liệu lấy đúng từ poster của bạn.
- Trang đã hỗ trợ: cuộn mượt, hiệu ứng xuất hiện khi cuộn, menu hamburger trên mobile, nút gọi/Zalo nổi, tôn trọng chế độ giảm chuyển động, và phím Tab điều hướng rõ ràng.

© 2026 DOV PHỐ HIẾN.
