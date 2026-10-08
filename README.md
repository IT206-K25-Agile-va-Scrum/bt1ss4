# BÁO CÁO BÀI TẬP: RÀ SOÁT USER STORY VÀ SẮP XẾP PRODUCT BACKLOG (FOODNOW)

> 👤 **Học viên:** Đỗ Hoàng Sơn | **Mã SV:** PTIT-HCM-066
> 🏫 **Môn học:** IT206-K25-Agile-va-Scrum

---

## Nhiệm vụ 1: Tìm lỗi User Story theo INVEST

Trong buổi rà soát Product Backlog của ứng dụng đặt món FoodNow, nhóm đã tiến hành phân tích 4 User Story do Product Owner cung cấp dựa trên tiêu chí INVEST để phát hiện và xử lý các điểm chưa đạt.

- US1: Đạt - Vai trò rõ ràng, một việc cụ thể, có lợi ích thiết thực và có thể kiểm thử bằng cách chọn loại món rồi quan sát kết quả trả về.
- US2: Sai tiêu chí Testable (Có thể kiểm thử) và Small (Đủ nhỏ). Cụm từ 'đẹp và dễ dùng' mang tính chủ quan, không có tiêu chí đo lường cụ thể nên QA không biết khi nào là hoàn thành.
- US3: Sai tiêu chí Valuable (Có giá trị cho người dùng cuối). Lập trình viên muốn dùng 'React' là công nghệ kỹ thuật, không mang lại giá trị nghiệp vụ trực tiếp cho 'khách hàng' hay 'admin' của ứng dụng.
- US4: Sai tiêu chí Small (Quá lớn - Epic). User story này gộp quá nhiều tính năng vào làm một: báo cáo nhiều chiều (ngày, tuần, tháng, khu vực, nhà hàng), xuất file Excel và tích hợp tự động gửi email cho ban giám đốc.

| Mã | Kết quả và lý do |
| --- | --- |
| US1 | Đạt: vai trò rõ, một việc, có lợi ích, thử được bằng cách chọn loại món rồi xem kết quả. |
| US2 | Sai INVEST (Testable): Cụm từ 'giao diện đẹp và dễ dùng' quá mơ hồ, không có tiêu chí định lượng để kiểm thử. |
| US3 | Sai INVEST (Valuable): Viết theo hướng kỹ thuật 'dùng React', không đem lại giá trị trực tiếp cho người dùng cuối (khách hàng/admin). Cần chuyển thành Product Backlog Item kỹ thuật riêng hoặc đổi góc nhìn. |
| US4 | Sai INVEST (Small): Gộp quá nhiều yêu cầu phức tạp (báo cáo đa chiều, xuất Excel, gửi email tự động) vào một Story, không thể hoàn thành trong một Sprint. |

## Nhiệm vụ 2: Sửa lỗi User Story và phân rã Epic

Sau khi phát hiện các lỗi sai ở bước rà soát, chúng ta tiến hành chỉnh sửa US2 thành một story đạt chuẩn có thể đo lường được, đồng thời tách US4 quá lớn thành cấu trúc cây 3 cấp (Epic -> Feature -> User Story).

- a) Viết lại US2: Là một 'khách hàng', tôi muốn 'thực hiện các bước đặt món (chọn món, giỏ hàng, thanh toán) trong tối đa 3 màn hình', để 'đặt món nhanh chóng mà không bị thao tác rườm rà'.
- b) Tách US4 thành cấu trúc 3 cấp:
- - Cấp 1 (Epic): Quản trị hệ thống và Báo cáo kinh doanh FoodNow
- - Cấp 2 (Feature): Phân hệ Báo cáo Doanh thu đa chiều
- - Cấp 3 (User Story 4.1): Là một 'admin', tôi muốn 'xem báo cáo doanh thu theo ngày, tuần, tháng và theo khu vực, nhà hàng trên giao diện quản trị', để 'nắm bắt tình hình kinh doanh kịp thời'.
- - Cấp 3 (User Story 4.2): Là một 'admin', tôi muốn 'xuất báo cáo doanh thu ra file Excel và tự động gửi email định kỳ cho ban giám đốc', để 'lưu trữ dữ liệu và báo cáo cấp trên thuận tiện'.

## Nhiệm vụ 3: Xếp lại Product Backlog theo DEEP

Sau khi đã làm sạch và chuẩn hóa các mục, tiến hành sắp xếp lại thứ tự ưu tiên cho các Product Backlog Item gồm US1, US2 đã sửa, cùng 2 story mới tách từ US4 (US4.1 và US4.2).

- a) Thứ tự ưu tiên Product Backlog:
- - Hạng 1: US1 (Lọc nhà hàng theo loại món) - Ưu tiên cao nhất vì phục vụ trực tiếp nhu cầu cốt lõi của khách hàng là tìm kiếm món ăn nhanh chóng khi mở app.
- - Hạng 2: US2 đã sửa (Tối ưu giao diện đặt món gọn trong 3 màn hình) - Giúp tăng tỷ lệ chuyển đổi đơn hàng thành công, cốt lõi kinh doanh.
- - Hạng 3: US4.1 (Xem báo cáo doanh thu đa chiều trên giao diện) - Phục vụ nhu cầu quản trị cơ bản của admin.
- - Hạng 4: US4.2 (Xuất Excel và gửi email tự động cho ban giám đốc) - Tính năng nâng cao, phục vụ báo cáo định kỳ, có thể làm sau.
- b) Độ chi tiết theo tiêu chuẩn DEEP và hoạt động trong buổi Refinement:
- - Theo tiêu chuẩn DEEP (Detailed appropriately - Chi tiết phù hợp), các story nằm ở top đầu của Backlog phải được viết rất rõ ràng, chi tiết, đã được ước lượng (estimation) bằng Story Points và đáp ứng đầy đủ tiêu chí chấp nhận (Acceptance Criteria) để sẵn sàng đưa vào Sprint.
- - Trong buổi Backlog Refinement trước khi vào Sprint, Product Owner, Scrum Master và Development Team cần cùng nhau: làm rõ các yêu cầu chi tiết (Acceptance Criteria), thảo luận về giải pháp kỹ thuật, chia nhỏ thêm nếu cần, và chốt điểm Story Points cho item đứng đầu.

---

## 📁 Danh sách tệp tin nộp bài trong Repository
- 📝 `bt1.docx`: Báo cáo tài liệu phân tích nghiệp vụ hoàn chỉnh.
