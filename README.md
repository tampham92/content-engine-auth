# Trang nhận chuyển hướng cho TikTok

TikTok bắt Redirect URI phải là HTTPS, không nhận `localhost`. Trang tĩnh này
giải quyết chuyện đó mà không cần máy chủ.

## Dựng bằng GitHub Pages (miễn phí, 5 phút)

1. Tạo repo mới trên GitHub, ví dụ `tiktok-auth`
2. Upload file `index.html` trong thư mục này lên
3. Vào **Settings → Pages** → Source chọn **Deploy from a branch** → branch `main`, thư mục `/ (root)` → Save
4. Chờ 1–2 phút, GitHub cho bạn địa chỉ dạng:
   ```
   https://<ten-github>.github.io/tiktok-auth/
   ```
5. Khai **chính xác** địa chỉ đó làm Redirect URI trong app TikTok
   *(kể cả dấu `/` cuối — TikTok so khớp từng ký tự)*
6. Dán vào `.env`:
   ```
   TIKTOK_REDIRECT_URI=https://<ten-github>.github.io/tiktok-auth/
   ```

## Trang này làm gì

Không gì cả, theo đúng nghĩa đen. Nó chỉ đọc mã uỷ quyền từ thanh địa chỉ và
hiện ra cho bạn copy. Không gửi dữ liệu đi đâu, không có backend, không lưu gì.
