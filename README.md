# Tính AHP – lựa chọn phương án

Trang web tĩnh tính AHP tự động: người dùng nhập điểm so sánh cặp đôi, trang **hiện kết quả ngay** (không phải tự tính rồi kiểm tra như trang `ahp-checker`).

1. Nhập điểm so sánh cặp đôi các phương án theo từng tiêu chí → trang tính ngay trọng số của từng phương án theo tiêu chí đó.
2. Nhập điểm so sánh cặp đôi các tiêu chí → trang tính ngay trọng số của từng tiêu chí.
3. Trang tính điểm có trọng số = trọng số tiêu chí × trọng số phương án theo tiêu chí.
4. Trang tính tổng điểm có trọng số, xếp hạng và nêu phương án được chọn.

Mỗi bảng trọng số có phần “chi tiết các lần bình phương” để xem từng bước tính, kèm λmax, CI, CR (tham khảo).

**Khi mở trang lần đầu:** tên phương án/tiêu chí của ví dụ (Tom, Dick, Harry; Kinh nghiệm, Trình độ, Khả năng lãnh đạo, Tuổi), mọi cặp so sánh đều là 1 – 1. Nút “Nạp ví dụ Tom – Dick – Harry” nạp điểm so sánh của ví dụ trong slide. Người dùng đổi được tên và số lượng phương án, tiêu chí.

**Thang điểm và quy tắc nhập** (Bước 0): khai báo điểm tối đa của thang (mặc định 9). Mỗi ô điểm nhận số từ 1 đến điểm tối đa (cho phép số thập phân như 1,2); trong mỗi cặp, ô của yếu tố kém hơn luôn là 1. Cặp nào sai quy tắc sẽ bị tô đỏ kèm lý do và chưa được đưa vào tính toán.

Cách tính giống ví dụ Tom – Dick – Harry trong slide: bình phương ma trận liên tiếp, cộng theo hàng, chia cho tổng; mặc định lấy trọng số ở lần bình phương thứ 2 (có thể đổi ở Bước 0).

Dữ liệu chỉ lưu trên trình duyệt của người dùng; muốn lưu kết quả dùng nút “In / lưu PDF”.

## Các file

| File | Vai trò |
|---|---|
| `index.html` | Giao diện trang |
| `ahp.js` | Phần tính toán (giống hệt file của `ahp-checker`) |
| `README.md` | Hướng dẫn này |

## Đưa lên GitHub Pages (không cần cài đặt gì)

1. Đăng nhập GitHub → nút **New** (tạo repository mới), đặt tên `ahp-calculator`, chọn **Public** → **Create repository**.
2. Trong repository vừa tạo, bấm **uploading an existing file** (hoặc **Add file → Upload files**), kéo thả cả 3 file `index.html`, `ahp.js`, `README.md` → **Commit changes**.
3. Vào **Settings → Pages**. Ở mục **Build and deployment**, *Source* chọn **Deploy from a branch**; *Branch* chọn **main** và thư mục **/(root)** → **Save**.
4. Đợi 1–2 phút, tải lại trang Settings → Pages sẽ hiện địa chỉ
   `https://ntvhoa.github.io/ahp-calculator/`.

Muốn sửa trang: mở file trên GitHub → biểu tượng bút chì → sửa → **Commit changes**; trang tự cập nhật sau 1–2 phút.

## Chạy thử trên máy

Mở `index.html` trực tiếp bằng trình duyệt là dùng được (hai file `index.html` và `ahp.js` phải nằm cùng thư mục).
