# MobileDev-BTVN01
# SINH VIÊN THỰC HIỆN: LƯƠNG HOÀNG VIỆT - K225480106073
# MÔN HỌC: LẬP TRÌNH TRÊN THIẾT BỊ DI ĐỘNG
# BÀI TẬP 01
# BÀI LÀM
# I. NGUYÊN LÝ HOẠT ĐỘNG
# II. THỰC HÀNH
## 1. KHỞI TẠO KIẾN TRÚC MÀN HÌNH

Truy cập vào thanh menu điều khiển phía trên vùng hiển thị Viewer, thực hiện lần lượt:

Hệ thống mặc định có sẵn Screen1 ( Dùng làm nơi giới thiệu bản thân)

Nhấn vào nút + Add Screen → Nhập tên chính xác là Screen2 → Nhấn OK (Dùng cho chức năng Giải toán).

Tiếp tục nhấn nút + Add Screen → Nhập tên chính xác là Screen3 → Nhấn OK (Dùng cho chức năng hiển thị WebViewer).

## 2. THIẾT KẾ UI & THUỘC TÍNH (DESIGNER VIEW)

### a) Cấu hình Screen1 (Thông tin cá nhân & Điều hướng)

Từ bảng Palette mục User Interface, kéo 1 thành phần Label vào màn hình. Sang bảng Properties, tìm ô Text và nhập dữ liệu cá nhân (Họ tên: Lương Hoàng Việt, MSV: K225480106073...).

Kéo tiếp 2 thành phần Button vào đặt phía dưới.

Bấm chọn Button thứ nhất ở danh sách Components → Chọn Rename → Đổi tên thành btn_SangToan. Thay đổi thuộc tính Text của nó thành Sang trang tính toán.

Bấm chọn Button thứ hai → Chọn Rename → Đổi tên thành btn_SangWeb. Thay đổi thuộc tính Text của nó thành Sang Youtube.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/fb10d49e-3b49-4040-9f0c-e1e1e6e9fe00" />

### b) Cấu hình Screen2 (Giải bài toán Tính Tổng đơn giản)
Chọn hộp chuyển đổi màn hình (Screens dropdown) ở cạnh trên thanh công cụ để chuyển sang làm việc với Screen2:

Kéo 2 thành phần TextBox vào. Lần lượt tiến hành Rename thành txt_SoA và txt_SoB. Tại bảng Properties của cả 2 ô nhập này, tìm và **tích chọn mục NumbersOnly** (Ràng buộc hệ thống chỉ cho phép nhập số ký tự, chặn nhập chữ để tránh lỗi Crash ứng dụng khi tính toán).

Kéo 1 Button đặt bên dưới → Đổi tên thành btn_TinhTong → Đổi thuộc tính Text thành Tính Tổng (A + B).

Kéo 1 Label → Đổi tên thành lbl_KetQua → Đổi thuộc tính Text mặc định thành Kết quả hiển thị tại đây....

Kéo thêm 1 Button nữa ở cuối → Đổi tên thành btn_Back2 → Đổi thuộc tính Text thành ← Quay Lại Trang Chủ.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/48b57b88-2b35-41ad-85f5-1eb53cbeade5" />

### c) Cấu hình Screen3 (Tích hợp WebViewer Responsive)
Chuyển thanh menu Screens dropdown sang chọn dữ liệu của Screen3:

Tại bảng Palette mục User Interface, kéo linh kiện WebViewer thả vào màn hình. Sang cột thuộc tính Properties bên phải: Cấu hình tham số Height = Fill parent và Width = Fill parent (Giúp trình xem web kéo dãn toàn màn hình điện thoại).

Tại mục thuộc tính HomeUrl, dán đường dẫn trang web muốn hiển thị (Ví dụ: https://www.youtube.com/ - engine WebKit sẽ tự động gọi giao diện Mobile responsive).

Kéo thêm 1 Button đặt ở dưới cùng của màn hình → Đổi tên thành btn_Back3 → Đổi thuộc tính Text thành ← Thoát Trình Duyệt.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/c772dcbb-af8c-4fa3-9fbf-09b56378e24a" />

## 3. LẬP TRÌNH HOÀN THIỆN LOGIC (BLOCKS VIEW)

Ấn vào nút chuyển đổi Blocks ở góc trên bên phải màn hình để thực hiện ghép nối các khối xử lý thuật toán sau đây:

### a) Lập trình tại Screen1 (Điều hướng trang):

Chọn mã nguồn Screen1 bên cây thư mục trái. Bấm vào linh kiện btn_SangToan kéo khối sự kiện Click ra vùng trống. Tiến hành lắp ghép cấu trúc

Thực hiện tương tự đối với nút bấm qua trang Web 

Với Screen 1 ta được Blocks sau:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/7dff4299-07ad-4058-a5e8-fc067b361be8" />

### b) Lập trình tại Screen2 (Xử lý thuật toán giải toán):

Chuyển không gian làm việc sang Screen2. Bấm vào linh kiện btn_TinhTong lấy khối click, sau đó click vào thư mục Math và các linh kiện TextBox để lấy các khối tương ứng ghép thành cấu trúc hoàn chỉnh

Lập trình cho nút quay lại Màn hình 1 (Hệ thống sẽ giải phóng bộ nhớ của Screen2 và lùi về trang chủ)

Với Screen 2 ta được Blocks sau:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/a15b294e-91e5-4659-aad7-8076997211d1" />

### c) Lập trình tại Screen3 (Quản lý WebViewer):

Chuyển sang không gian Screen3. Linh kiện WebViewer sẽ tự động tải trang theo đường dẫn cấu hình sẵn ở `HomeUrl` ngay khi màn hình kích hoạt. Công việc duy nhất của lập trình viên là xử lý nút thoát thoát trang để trở lại:

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/e31f17ec-2892-4d5e-af69-0d715dd332a5" />

## 4. Build APK và test trên Điện thoại



