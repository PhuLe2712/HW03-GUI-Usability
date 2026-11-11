# HW03 — GUI & Usability Testing Report

**SUT:** EShop — Sàn thương mại điện tử tiếng Việt  
**Học viên:** Lê Mạnh Phú  
**MSSV:** 23120325  
**Luồng kiểm thử cốt lõi:** FR-01 Đăng ký ➔ FR-02 Đăng nhập ➔ FR-05 Danh sách/tìm kiếm ➔ FR-06 Chi tiết sản phẩm ➔ FR-07 Giỏ hàng  

---

## 1. Bảng Tự đánh giá (Self-Assessment Table)

| Hạng mục đánh giá | Điểm tối đa | Tự đánh giá | Minh chứng & Trạng thái |
|:---|:---:|:---:|:---|
| **Task 1 — GUI Checklist** | 30 | 28 | Thiết kế 70 tiêu chí phủ đủ 4 Interface Aspects (IA-01 đến IA-04); thực thi trên 3 môi trường; phát hiện 38 checklist ID Fail. Có file Excel và TSV. |
| **Task 2 — Usability Evaluation** | 40 | 36 | Thiết kế kế hoạch đánh giá chuẩn, kịch bản mục tiêu, 01 phiên Pilot + 07 phiên người dùng (P01–P07), bảng điểm SUS chi tiết (Điểm trung bình: 38.57), phân loại theo mức độ nghiêm trọng Nielsen. |
| **Task 3 — Cross-Browser / Platform** | 20 | 16 | Thực thi trên Chrome Desktop, Firefox Desktop và Chrome Android (Pixel 7 emulation), đối soát hành vi hiển thị và tương tác responsive. |
| **Agent Skills & Video** | 10 | 8 | Tích hợp kỹ năng tự động hóa và tài liệu hướng dẫn. |
| **TỔNG ĐIỂM TỰ CHẤM** | **100** | **88 / 100** | Mã bài nộp dự kiến: `23120325_HW03_AI_GUIUsability_088.zip` |

---

## 2. Báo cáo Tóm tắt Kiểm thử (Test Summary Report)

- **Số lượng màn hình / Luồng kiểm thử:** 05 màn hình chính (Đăng ký, Đăng nhập, Trang chủ/Danh sách sản phẩm, Chi tiết sản phẩm, Giỏ hàng).
- **Checklist GUI (Task 1):**
  - Số lượng thiết kế: **70 tiêu chí** (50 do AI gợi ý, 20 bổ sung thủ công theo accessibility, edge cases và responsive).
  - Trạng thái thực thi: 28 PASS, 36–38 FAIL (tùy nền tảng), 2 Pending, 1–4 N/A.
- **Đánh giá Khả dụng (Task 2):**
  - Số lượng người tham gia: **01 Pilot + 07 Người dùng chính thức** (P01–P07 đại diện cho Kế toán, Kỹ sư, Sinh viên, Tiểu thương, Marketing, Bác sĩ, Giáo viên hưu trí).
  - Điểm SUS trung bình: **38.57 / 100** (Grade F - Poor / Not Acceptable).
  - Thời gian trung bình hoàn thành: **8 phút 10 giây**.
- **Số lượng lỗi Usability / GUI phát hiện:** **30 nhóm lỗi giao diện và trải nghiệm** (đã dự thảo trong `GitHub_Issue_Drafts.md`), trong đó có 2 lỗi mức Catastrophe (Blocker) và 3 lỗi mức Major.

---

## 3. Cấu trúc Thư mục Tài liệu

- [`HW03_Main_Report.md`](../HW03_work/HW03_Main_Report.md): Báo cáo tổng thể toàn bộ bài tập HW03.
- [`Task2_Usability_Evaluation_Report.md`](Task2_Usability_Evaluation_Report.md): Báo cáo chi tiết toàn diện của Task 2 (Kịch bản, biên bản quan sát từng phiên, tính điểm SUS, phân tích định tính/định lượng).
- [`Task1_GUI_Checklist.xlsx`](Task1_GUI_Checklist.xlsx): File Excel Checklist 70 tiêu chí kèm liên kết bằng chứng.
- [`GitHub_Issue_Drafts.md`](GitHub_Issue_Drafts.md): Danh sách 30 bản nháp Issue chi tiết kèm đường dẫn ảnh chụp bằng chứng.
