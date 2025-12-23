# Christmas Tree 3D (tree.html)

Trang Giáng Sinh 3D dùng Three.js với cây thông bằng hạt, tuyết/quà rơi, lò sưởi, ông già Noel bay qua, nhạc nền và nhiều tinh chỉnh cho di động. Đây là README dành cho trang `tree.html` hiện tại.

## Tính năng chính
- Cây thông 3D bằng hệ hạt, ngôi sao phát sáng, hiệu ứng nổ “EXPLODE”.
- Ông già Noel (xe trượt) bay ngang, có quầng sáng và vệt sao; nhấn để đổi nhạc ngẫu nhiên.
- Lò sưởi 2D phát sáng; nhấn vào lò sưởi để mở hộp nhập tên hoặc ngày sinh (định dạng `dd/mm`).
- Nhập đúng 25/12: kích hoạt “trái tim” 5 giây rồi trở về cây thông. Mặc định KHÔNG tự hiện trái tim khi tải trang.
- Lời chúc: chọn ngẫu nhiên từ `greetings.txt`, hiển thị qua modal/box.
- Nhạc nền: đọc danh sách từ `music.txt` (mỗi dòng một tên file trong thư mục `MUSIC_PLAYLIST/`). Tự hiện nút Bật/Tắt nhạc khi sẵn sàng.
- Tối ưu di động: khóa kích thước canvas khi bàn phím mềm mở (tránh màn hình bị co), giảm hiệu ứng khi FPS thấp.

## Cách chạy nhanh
- Cách 1: Mở `index.html` rồi bấm nút “Đến trang Cây Thông”.
- Cách 2: Mở trực tiếp `tree.html` bằng trình duyệt (Chrome/Edge/Firefox).
- Gợi ý dùng Live Server trong VS Code để reload nhanh.

PowerShell (Windows):

```powershell
Start-Process .\hello.html   # hoặc .\tree.html
```

## Cách dùng
- Nhấn vào lò sưởi để mở ô nhập: tên hoặc ngày sinh `dd/mm`.
- Nhập 25/12 để xem hiệu ứng trái tim; nhập tên để nhận lời chúc cá nhân.
- Chạm vào ngôi sao trên đỉnh để kích hoạt “EXPLODE”.
- Chạm vào ông già Noel để đổi bài nhạc ngẫu nhiên.
- Chạm vào hộp quà để xem lời chúc ngẫu nhiên.
- Kéo (drag) để xoay cây thông.

## Tuỳ chỉnh nhanh
- Nhạc: sửa `music.txt` (mỗi dòng tên file `.mp3` nằm trong `MUSIC_PLAYLIST/`).
- Lời chúc: sửa `greetings.txt` (mỗi dòng một câu). Dòng bắt đầu bằng `#` sẽ bị bỏ qua.
- Ảnh/texture bên ngoài (tùy chọn):
  - `Santa1.png` (xe trượt) — nếu có, sẽ tự thay vào sprite ông già Noel.
  - `lo_suoi.png` (mặt tiền lò sưởi) — nếu có, sẽ tự thay và căn tỷ lệ chuẩn.

## Ghi chú di động
- Trang đã thêm “keyboard/viewport guard”: khi mở bàn phím mềm, canvas được cố định để không co lệch UI. Khi đóng bàn phím, kích thước sẽ tự khôi phục.
- Một số hiệu ứng (tuyết rơi) chỉ bật trên desktop; di động giữ hiệu năng mượt mà hơn.

## Cấu trúc dự án
```
hello.html         # Trang chào mừng, dẫn tới tree.html
tree.html          # Trang cây thông 3D (chính)
music.txt          # Danh sách bài hát (mỗi dòng tên file trong MUSIC_PLAYLIST)
greetings.txt      # Lời chúc hiển thị ngẫu nhiên
MUSIC_PLAYLIST/    # Thư mục chứa các file .mp3
Santa1.png         # (tuỳ chọn) ảnh xe trượt
lo_suoi.png        # (tuỳ chọn) ảnh mặt lò sưởi
```

## Triển khai GitHub Pages
- Dự án tĩnh, không cần build. Bật Pages trỏ tới nhánh chứa các file này.
- Đường dẫn/tên file phải khớp chính xác (phân biệt chữ hoa/thường).

Chúc bạn một mùa Giáng Sinh an lành và rực rỡ! 🎄✨
