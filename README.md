# VAS-WMS | Bản Mẫu Giao Diện Tác Nghiệp & Điều Hành Kho Chuỗi Lạnh

---

## 1. Tổng quan Bản mẫu Giao diện (Interactive Prototype)
Bản mẫu giao diện tương tác độc lập được thiết kế theo đúng chuẩn mực công thái học kho bãi (Enterprise Industrial UX) và kỷ luật thị giác 60-30-10:
- **60% Nền trung tính:** Mã màu dịu mắt `#f6f8fa` chống mỏi mắt trong môi trường ánh sáng phòng đệm kho lạnh.
- **30% Phân cấp cấu trúc:** Thẻ Card màu trắng bo góc nhẹ viền thép `#94b2d1`.
- **10% Nhận diện thương hiệu:** Xanh Hải quân `#0B2F64` và Xanh thương hiệu `#1d4ed8`.
- **Âm thanh phản hồi Bíp Audio:** Mô phỏng chân thực tiếng còi súng quét Barcode PDA cầm tay (tần số 1000Hz khi quét đúng, tần số 300Hz trầm ngắt quãng khi quét sai).
- **Mã hóa viền màu trực quan (Color Border Encoding):** Phân biệt tức thời trạng thái các ô kệ trên sơ đồ mặt bằng (Khu tiếp nhận xanh dương, Xuất kho xanh lá, Biệt trữ cách ly KB-Q01 đỏ, Hàng cận date vàng).

---

## 2. Cấu trúc 16 Màn hình Nghiệp vụ
Bản mẫu tích hợp đầy đủ 8 màn hình tác nghiệp chính và 8 màn hình hồ sơ chuyên sâu (Sub-views):
1. **SCR-SYS-01:** Đăng nhập Hệ thống & Kiểm soát Phân quyền (RBAC)
2. **SCR-SYS-02:** Bảng Điều Khiển Trung Tâm Điều Hành Kho Tân Bình
3. **SCR-INB-01:** Tiếp nhận & Nghiệm thu Chuỗi lạnh GSP Abbott (Cảm biến Testo, Đá khô $\ge 8.0\text{ cm}$, Đếm ngược 30 phút)
4. **SCR-INB-02:** Lập Biên bản Sự cố Chuỗi lạnh BMSC (Niêm phong cách ly KB-Q01, Ký số điện tử)
5. **SCR-INB-03:** Phân bổ Vị trí Ô Kệ Lưu kho Putaway theo Dải Nhiệt độ (-20°C, 2-8°C, 15-25°C)
6. **SCR-OUT-01:** Thẩm định Tồn kho Khả dụng ATP & Khóa giữ Phân bổ (Allocation Lock 30 giây)
7. **SCR-OUT-02:** Soạn hàng theo FEFO & Lập Lệnh Chuyển kho TO
8. **SCR-OUT-03:** Quét Barcode PDA Cầm tay Đối soát 100% & In Phiếu BMPLH02
9. **SCR-BIN-01:** Sơ đồ Mặt bằng Ô Kệ Kho Tân Bình Mã Hóa Viền Màu
10. **SCR-BIN-02:** Quản trị Khu Biệt Trữ Cách Ly Kiểm Định KB-Q01
11. **SCR-BIN-03:** Báo cáo Tỷ lệ Lấp đầy & Sức chứa Ô Kệ
12. **SCR-TRC-01:** Sổ Chi Tiết Thẻ Kho Điện Tử Biến Động Bất Biến (Append-only)
13. **SCR-TRC-02:** Truy Xuất Nguồn Gốc 2 Chiều Khép Kín Audit Trail 5 Bước
14. **SCR-TRC-03:** Ma Trận Cảnh Báo Hạn Dùng FEFO 3 Cấp Độ
15. **SCR-MST-01:** Hồ sơ Master Data Vị trí Ô Kệ & Sức chứa Tải trọng (View/Edit)
16. **SCR-MST-02:** Hồ sơ Master Data Lô Hàng & Truy vết Vòng đời (View/Edit)

---

## 3. Hướng dẫn Chạy & Kiểm thử Bản mẫu
1. Tải về hoặc clone repository:
   ```bash
   git clone https://github.com/Duong312000/uiux-VAS-WMS.git
   ```
2. Mở trực tiếp tệp `index.html` bằng bất kỳ trình duyệt Web hiện đại nào (Google Chrome, Microsoft Edge, Mozilla Firefox) mà không cần cài đặt Web server.
3. Bản mẫu được xây dựng thuần HTML5, CSS3 và Vanilla JavaScript độc lập, không phụ thuộc thư viện ngoài (Zero Dependency), sẵn sàng triển khai trên GitHub Pages.
