# Bước 1: Lên Ý Tưởng & Xác Thực (Ideation & Discovery)

Tài liệu này chi tiết hóa Bước 1 theo quy trình tại [quy_trinh_phat_trien_app_web.md](file:///d:/CodeVui/CodeSteps/requirements/quy_trinh_phat_trien_app_web.md#L7-L17) cho dự án Website Bán hàng Thương mại điện tử (E-Commerce).

---

## 1. Xác Định Bài Toán & Khách Hàng Mục Tiêu

### 1.1. Chân dung khách hàng (Personas)
* **Khách hàng cuối (End-user / Người mua hàng):**
  * Những người có nhu cầu mua sắm trực tuyến, tìm kiếm sản phẩm chất lượng từ một thương hiệu uy tín.
  * Mong muốn quy trình đặt hàng nhanh chóng, đơn giản, minh bạch về giá, vận chuyển và áp dụng mã giảm giá (voucher) dễ dàng.
* **Người dùng nội bộ (Internal Users):**
  * **Nhân viên (Staff):** Cần tiếp nhận đơn hàng, cập nhật trạng thái đơn, xử lý giao hàng và chăm sóc khách hàng.
  * **Quản trị viên (Admin):** Cần quản lý danh mục sản phẩm, tồn kho, cấu hình chương trình khuyến mãi/voucher, phân quyền nhân sự và xem thống kê kinh doanh.

### 1.2. Nỗi đau (Pain Points) cần giải quyết
* **Phía khách hàng:**
  * E ngại các website trôi nổi, thiếu độ tin cậy và không minh bạch nguồn gốc.
  * Thủ tục đặt hàng và thanh toán quá phức tạp, mất thời gian.
  * Voucher khó áp dụng hoặc điều kiện không rõ ràng.
* **Phía vận hành / doanh nghiệp:**
  * Khó kiểm soát đơn hàng nếu không có hệ thống quản trị tập trung (Backoffice).
  * Chi phí chiết khấu cao khi phụ thuộc hoàn toàn vào các sàn trung gian.

---

## 2. Nghiên Cứu Đối Thủ & Thị Trường (Competitor Analysis)

| Đối thủ tham chiếu | Điểm mạnh | Điểm yếu / Hạn chế | Điểm khác biệt / Lợi thế của dự án |
| :--- | :--- | :--- | :--- |
| **ShopeeFood** | Lượng người dùng lớn, voucher phong phú, tích hợp giao vận & thanh toán hoàn chỉnh. | Cửa hàng chịu chiết khấu cao, phụ thuộc chính sách của sàn, thương hiệu riêng bị hòa lẫn. | Xây dựng kênh bán hàng độc lập (D2C), giữ trọn vẹn tệp khách hàng và dữ liệu, tối ưu chi phí vận hành. |
| **The Pizza Company (Website)** | Giao diện tập trung, hình ảnh chuyên nghiệp, kiểm soát chất lượng dịch vụ và ưu đãi trực tiếp. | Chủ yếu phục vụ chuỗi món ăn riêng biệt, trải nghiệm mở rộng danh mục đa dạng còn hạn chế. | Kết hợp trải nghiệm đặt hàng chuyên nghiệp, hệ thống voucher linh hoạt cùng hệ thống Backoffice quản trị mở rộng. |

---

## 3. Định Hình Phạm Vi MVP (Minimum Viable Product)

Mục tiêu của MVP là ra mắt nhanh phiên bản khả thi tối thiểu để kiểm chứng luồng nghiệp vụ mua sắm và thanh toán thực tế với chi phí tối ưu nhất.

### 3.1. Các nhóm tính năng cốt lõi cho MVP
1. **Xác thực & Quản lý tài khoản (Authentication):**
   * Đăng ký, đăng nhập tài khoản khách hàng.
   * Phân quyền truy cập cơ bản (Khách hàng vs Nhân viên / Quản trị viên).
2. **Giao diện người dùng (Storefront):**
   * Xem danh mục sản phẩm, chi tiết sản phẩm.
   * Thêm / bớt sản phẩm vào giỏ hàng (Cart).
3. **Khuyến mãi & Thanh toán (Checkout & Third-Party Integration):**
   * Nhập và áp dụng mã Voucher hợp lệ (tính toán giảm giá trực tiếp vào tổng đơn).
   * Điền thông tin giao hàng và chọn phương thức thanh toán (COD hoặc tích hợp cổng thanh toán bên thứ ba).
4. **Hệ thống Quản trị (Backoffice):**
   * Quản lý sản phẩm (thêm/sửa/ẩn sản phẩm).
   * Quản lý đơn hàng (xem danh sách đơn, duyệt và đổi trạng thái giao hàng).
   * Quản lý mã Voucher (tạo mã, cấu hình mức giảm, hạn dùng).

### 3.2. Tiêu chí đánh giá thành công của MVP
* Người dùng hoàn tất được trọn vẹn luồng: **Đăng nhập -> Chọn món -> Thêm giỏ hàng -> Áp mã Voucher -> Thanh toán & Tạo đơn thành công**.
* Phía Backoffice ghi nhận đơn hàng đúng thời gian thực và cho phép nhân viên cập nhật trạng thái đơn.
