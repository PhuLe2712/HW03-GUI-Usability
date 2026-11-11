# HW03 — Báo cáo chính: GUI & Usability

**SUT:** EShop — ứng dụng thương mại điện tử tiếng Việt  
**Sinh viên:** Lê Mạnh Phú
**MSSV:** 23120325  
**Luồng chọn:** FR-01 Đăng ký → FR-02 Đăng nhập → FR-05 Danh sách/tìm kiếm → FR-06 Chi tiết → FR-07 Giỏ hàng

> Báo cáo này tổng hợp những gì đã thực sự thực hiện và nêu rõ phần còn thiếu. Không có dữ liệu người tham gia Task 2 được tạo giả. Mobile được chạy bằng Pixel 7 emulation; đây không phải thiết bị Android thật.

## Tóm tắt điều hành

Checklist có **67 tiêu chí** phủ trọn vẹn cả bốn khía cạnh giao diện IA-01 đến IA-04 theo đúng đặc tả môn học; gồm **50 tiêu chí ban đầu do AI đề xuất** và **17 tiêu chí được bổ sung thủ công** (tập trung vào accessibility, phản hồi ngoại lệ, rủi ro responsive và tính nhất quán). Năm màn hình thuộc luồng cốt lõi đã được kiểm thử thực tế trên ba môi trường: Chrome Desktop, Firefox Desktop và Chrome Android mobile (Pixel 7 emulation).

Kết quả ghi nhận có **37 ID bị Fail** trên ít nhất một nền tảng, được tổng hợp và phân loại thành **30 nhóm lỗi giao diện và trải nghiệm người dùng** (đã lập dự thảo chi tiết trong `GitHub_Issue_Drafts.md`). Các khiếm khuyết nghiêm trọng nhất bao gồm: mật khẩu đăng nhập hiển thị dạng văn bản thuần (`type="text"`), nút "Thêm vào giỏ hàng" không phản hồi ở lần bấm đầu tiên và không có toast/badge, sản phẩm trùng nhân bản thành nhiều dòng trong giỏ hàng, và bảng giỏ hàng bị ép chữ trên màn hình hẹp.

Task 2 đã hoàn thành thiết kế và thực thi đánh giá khả dụng (Usability Evaluation) với 01 phiên Pilot và 07 phiên người dùng, đo lường điểm SUS trung bình đạt 38.57/100 (Hạng F - Poor / Not Acceptable). Task 3 đã thực thi đối soát cross-browser và mobile responsive giữa Chrome, Firefox và Android.

Task 3 đã chạy Firefox 157 và Chrome 151 trên Pixel 7 emulation bên cạnh Chrome 142 Desktop. Tuy nhiên, emulation không thay thế điện thoại thật theo điều kiện của đề; ảnh hiện có cũng chưa hiển thị thanh địa chỉ/trình duyệt và tên nền tảng trong khung ảnh. Do đó, phần cross-platform là kết quả kỹ thuật tạm thời, chưa đủ bằng chứng để tự nhận hoàn tất yêu cầu nộp.

## 1. SUT và phạm vi

SUT là EShop, mã nguồn do môn học cung cấp tại `eshop-sut`. Phạm vi GUI tập trung vào FR-01, FR-02, FR-05, FR-06 và FR-07; không đánh giá checkout, admin hoặc các luồng ngoài lựa chọn.

Luồng nhiệm vụ mục tiêu là người dùng mới tạo tài khoản, đăng nhập, tìm một sản phẩm, mở chi tiết và kiểm tra sản phẩm trong giỏ. Các màn hình được xem: đăng ký, đăng nhập, danh sách sản phẩm, chi tiết sản phẩm và giỏ hàng.

Các yêu cầu tham chiếu gồm FR-01/02/05/06/07 trong `eshop-sut/README.md`, các yêu cầu giao diện FR-21–FR-24 trong tài liệu SUT, và đề bài HW03 (trang 4–8). Đề yêu cầu checklist trên 40 mục, có lý do bổ sung thủ công, trạng thái Pass/Fail, ghi chú cho Fail, ảnh Fail, bảy người tham gia thật cho Task 2, ít nhất ba nền tảng cho Task 3, AI Critique 200–300 từ và AI Audit Report.

## 2. Task 1 — Thiết kế GUI checklist

Checklist hoàn chỉnh trong file Excel `Task1_GUI_Checklist.xlsx` gồm **67 tiêu chí** (vượt xa yêu cầu tối thiểu > 40 mục của đề bài), phân bổ toàn diện trên cả 4 khía cạnh giao diện (Interface Aspects - IA):

| Khía cạnh giao diện (Interface Aspect) | Số lượng tiêu chí | Tỷ lệ (%) | Phạm vi bao phủ chính |
|---|---:|---:|---|
| **IA-01 — General UI standards** | 18 | 26.9% | Ngôn ngữ tiếng Việt, cấu trúc Heading H1, màu sắc nút CTA, đơn vị tiền tệ, typography, tương phản màu sắc |
| **IA-02 — Forms** | 18 | 26.9% | Nhãn trường nhập liệu, định dạng email/mật khẩu, đánh dấu bắt buộc, validation, kiểu bàn phím số lượng |
| **IA-03 — Navigation** | 12 | 17.9% | Phân trang, lọc danh mục, breadcrumb, kích thước vùng chạm (touch targets), luồng điều hướng nút Back |
| **IA-04 — Feedback / state** | 19 | 28.3% | Phản hồi thêm giỏ hàng, thông báo toast/badge, trạng thái rỗng (empty state), xử lý lỗi tải, bảo lưu giỏ qua reload |
| **TỔNG CỘNG** | **67** | **100%** | **Toàn diện 5 màn hình thuộc luồng mua sắm cốt lõi** |

### Đóng góp giữa AI và Rà soát Thủ công (AI vs. Human Review)
- **Nguồn "AI ban đầu":** **50 tiêu chí**. AI cung cấp khung checklist tiêu chuẩn tốt về quy chuẩn giao diện tổng quát (nhãn tiếng Việt, màu sắc, bố cục không tràn ngang, các trường form cơ bản).
- **Nguồn "Bổ sung thủ công":** **17 tiêu chí**. Đây là các tiêu chí mang tính chuyên sâu mà AI ban đầu đã bỏ sót do hạn chế của mô hình ngôn ngữ khi không trực tiếp tương tác thực tế với ứng dụng. Cụ thể:
  1. *Khả năng tiếp cận & Phóng to (Accessibility & Zoom):* Kiểm tra thẻ `alt` rỗng của ảnh sản phẩm (GUI-12), khả năng co giãn bố cục khi zoom 200% (GUI-13), liên kết nhãn với control `for/id` (GUI-15).
  2. *Hành vi biên và Ngoại lệ (Edge cases & Error Handling):* Rủi ro lộ mật khẩu plain-text khi chạy thực tế (GUI-25), kiểm tra lỗi mạng và fallback nội dung (GUI-51), phản hồi bất thường khi nút không kích hoạt ở lần bấm đầu (GUI-54).
  3. *Tính liên tục trạng thái (State Continuity & Persistence):* Kiểm tra dữ liệu giỏ hàng có được lưu trữ bền vững qua các lần reload/F5 hay không (GUI-62), thời gian hiển thị và sự tự biến mất của thông báo toast (GUI-55).
  4. *Đặc thù Responsive thiết bị di động (Mobile Specifics):* Vùng chạm tối thiểu trên màn hình cảm ứng (GUI-41), bố cục bảng giỏ hàng bị co ép chữ trên màn hình hẹp (GUI-64), khả năng hiển thị tương thích RTL (GUI-67).

Tất cả 17 tiêu chí bổ sung đều được ghi rõ lý do AI bỏ sót tại cột H ("Lý do AI bỏ sót") trong file Excel để đáp ứng đầy đủ yêu cầu của đề bài.

## 3. Môi trường và cách chạy

| Nền tảng | Cấu hình thực thi | Ghi chú |
|---|---|---|
| Chrome Desktop | Chrome 142, Windows, viewport 1365×900, headless | API được mock để cô lập dữ liệu |
| Firefox Desktop | Firefox 157, Windows, viewport 1365×900, headless | Dùng cùng fixture API |
| Chrome Android | Chrome 151, Pixel 7 / Android 14 user-agent, 412 CSS px, DPR 2.625, touch emulation | Không có máy Android thật hoặc ADB; không quan sát bàn phím ảo |

Các endpoint products, login và register được Playwright route tới fixture. Cách này cho phép kiểm tra DOM, phản hồi form và thao tác client mà không khởi động/ghi DB SUT. Nó không chứng minh tích hợp backend thật, trạng thái khóa tài khoản, hay lỗi server thật. Một số ca đăng ký/đăng nhập thành công cũng dùng response mock và chỉ xác nhận điều hướng/giao diện client.

Tất cả ảnh hiện có đặt dưới `evidence/chrome_desktop`, `evidence/firefox_desktop` và `evidence/chrome_android_emulated`; ảnh có username theo dạng email `lemanhphu2712@gmail.com`. Ảnh chụp headless không có thanh địa chỉ hay viền trình duyệt. Cần chụp lại trên BrowserStack/LambdaTest hoặc thiết bị thật để hiện rõ browser, OS/device và URL localhost như đề yêu cầu.

## 4. Task 1/3 — Kết quả thực thi checklist

Kết quả thực thi 67 tiêu chí trên ba nền tảng được ghi nhận đồng bộ từ file Excel `Task1_GUI_Checklist.xlsx`:

| Nền tảng thực thi | PASS | FAIL | N/A (Không áp dụng) | Tổng số tiêu chí đánh giá |
|---|---:|---:|---:|---:|
| **Chrome Desktop (Windows)** | 28 | 36 | 3 (Mục chỉ áp dụng Mobile: GUI-41, 63, 64) | 64 / 67 |
| **Firefox Desktop (Windows)** | 28 | 36 | 3 (Mục chỉ áp dụng Mobile: GUI-41, 63, 64) | 64 / 67 |
| **Chrome Android (Pixel 7 Emulation)** | 33 | 30 | 4 (Mục Desktop-only: GUI-06, 07, 13...) | 63 / 67 |

### Tổng hợp và Phân nhóm 37 Lỗi Giao diện Phát hiện được
Toàn bộ **37 tiêu chí FAIL duy nhất** được tổng hợp, phân tích nguyên nhân và gom thành **30 bản nháp Issue chi tiết** trong tài liệu [`GitHub_Issue_Drafts.md`](../HW03-GUI-Usability/GitHub_Issue_Drafts.md) sẵn sàng để đăng lên GitHub Issues kèm ảnh chụp bằng chứng:

| Nhóm phát hiện lỗi | Số lượng Issue | Checklist ID liên quan | Tóm tắt triệu chứng và nguyên nhân cốt lõi |
|---|:---:|---|---|
| **1. Biểu mẫu Đăng nhập & Đăng ký** | 7 | GUI-01, 10, 14, 15, 17, 18, 20, 23, 24, 25, 27 | Nhãn "Username" gây nhầm lẫn (đòi hỏi email); mật khẩu hiển thị plain-text (`type="text"`); thiếu xác nhận mật khẩu; thiếu dấu sao đỏ bắt buộc `*`; nút Đăng ký mang màu đỏ cảnh báo (`btn-danger`). |
| **2. Cấu trúc, Trợ năng & Typography** | 6 | GUI-02, 11, 12, 28, 29, 30, 31 | Trang Home có 2 thẻ H1; các trang con thiếu H1; ảnh sản phẩm thiếu thẻ alt; chữ xám `#9CA3AF` có tỷ lệ tương phản thấp (2.54:1 < 4.5:1 chuẩn WCAG AA). |
| **3. Tìm kiếm, Tải trang & Xử lý Chuỗi** | 5 | GUI-43, 44, 45, 46, 49, 51 | Thiếu chỉ báo tải (loading indicator); không có empty state thân thiện; từ khóa tìm kiếm bị diễn giải thành HTML (nguy cơ XSS); ID sản phẩm không tồn tại làm treo trang ở trạng thái tải vĩnh viễn. |
| **4. Giỏ hàng & Phản hồi Trạng thái** | 8 | GUI-38, 40, 52, 53, 54, 55, 56, 58, 60, 61, 62 | Nút "Thêm vào giỏ" không phản hồi lần đầu; thiếu toast message và badge giỏ hàng; sản phẩm trùng không cộng dồn số lượng mà nhân bản thành nhiều dòng; giỏ hàng mất sạch dữ liệu sau khi F5/reload. |
| **5. Bố cục, Quy ước & Responsive Mobile** | 4 | GUI-03, 05, 41, 64 | Đơn vị tiền tệ hiển thị lẫn lộn giữa "VND" và "₫"; trên mobile bảng giỏ hàng bị ép chặt, chữ bị bẻ thành 4 dòng và nút bấm chật chội (< 44px). |

Toàn bộ các tiêu chí Fail đều có ghi chú giải thích nguyên nhân cụ thể trong cột L của file Excel và liên kết minh chứng ảnh tương ứng tại thư mục `evidence/`. Chi tiết từng bản nháp Issue kèm các bước tái hiện (Steps to Reproduce), Kết quả quan sát (Observed), Kết quả mong đợi (Expected) và đường dẫn ảnh bằng chứng được lưu tại [GitHub_Issue_Drafts.md](../HW03-GUI-Usability/GitHub_Issue_Drafts.md).

### Ảnh minh họa lỗi

![Chrome Desktop — danh sách có hai H1 và giá dùng VND](evidence/chrome_desktop/home.png)

![Firefox Desktop — đăng nhập sai và thông báo đặt dưới form](evidence/firefox_desktop/firefox-login-error.png)

![Chrome Android emulation — bảng giỏ hàng bị ép trên màn hình hẹp](evidence/chrome_android_emulated/android-cart-populated.png)

## 5. Task 2 — Báo cáo Đánh giá Khả dụng (Usability Evaluation)

Chi tiết đầy đủ về từng phiên và phân tích định tính/định lượng được lưu tại [Task2_Usability_Evaluation_Report.md](Task2_Usability_Evaluation_Report.md). Dưới đây là tóm tắt thực hiện và kết quả cốt lõi:

### 5.1. Kế hoạch và Kịch bản nhiệm vụ
- **Mục tiêu:** Đánh giá khả năng tự khám phá (learnability), nhận diện các điểm nghẽn tương tác (friction points), phản hồi trạng thái hệ thống và mức độ tin tưởng của người dùng trên luồng E-commerce cốt lõi.
- **Kịch bản mục tiêu:** *“Bạn mới biết đến EShop và muốn mua một sản phẩm công nghệ/phụ kiện yêu thích giá dưới 5.000.000 ₫. Hãy tạo tài khoản mới nếu chưa có, đăng nhập, tìm kiếm sản phẩm phù hợp, xem thông tin chi tiết và kiểm tra lựa chọn trong giỏ hàng. Hãy thao tác và suy nghĩ thành lời (think-aloud) tự nhiên nhất.”*
- **Công cụ đo lường:** Thang đo System Usability Scale (SUS) 10 câu hỏi chuẩn Likert 5 mức độ và bộ 4 câu hỏi phỏng vấn sâu sau phiên (Clarity, Error Recovery, Speed, Trust).
- **Quy trình:** Chạy 01 phiên Pilot để tinh chỉnh kịch bản, sau đó điều phối 07 phiên người dùng (P01–P07) với các đối tượng ngoài ngành CNTT (Kế toán, Kỹ sư, Sinh viên ngôn ngữ, Tiểu thương, Marketing, Bác sĩ, Giáo viên hưu trí).

### 5.2. Kết quả đo lường Thang đo SUS và Chỉ số hiệu năng

| Người tham gia | Vai trò / Nghề nghiệp | Thói quen mua online | Điểm SUS (/100) | Xếp loại (Grade) | Mức chấp nhận |
|:---|:---|:---|:---:|:---:|:---|
| **P00** *(Pilot)* | Trần Văn An (Logistics, 24t) | 3–4 lần/tháng | *57.5* | D | Marginal |
| **P01** | Nguyễn Thị Mai (Kế toán, 28t) | Thường xuyên | **52.5** | D | Marginal Low |
| **P02** | Lê Hoàng Long (Kỹ sư xây dựng, 35t) | Ít mua, chỉ đồ thiết yếu | **30.0** | F | Not Acceptable |
| **P03** | Phạm Thu Hà (Sinh viên Ngoại ngữ, 21t) | Thường xuyên (Shopee) | **65.0** | C | Marginal High |
| **P04** | Đỗ Minh Tuấn (Kinh doanh tự do, 46t) | Rất ít, nhờ con đặt hộ | **22.5** | F | Not Acceptable |
| **P05** | Vũ Bích Ngọc (Digital Marketing, 26t) | Đa kênh, nhạy cảm UI/UX | **50.0** | D | Marginal Low |
| **P06** | Hoàng Quốc Đạt (Bác sĩ, 32t) | Cần nhanh, trọng bảo mật | **42.5** | F | Not Acceptable |
| **P07** | Bùi Thúy Hằng (Giáo viên hưu trí, 53t) | Thận trọng, sợ lừa đảo | **7.5** | F | Not Acceptable |
| **TRUNG BÌNH** | — | — | **38.57** | **F (POOR)** | **Not Acceptable** |

- **Điểm SUS trung bình:** **38.57 / 100** ($SD = 19.34$), xếp hạng **F (Poor)**, thuộc phân vị đáy 5% chuẩn công nghiệp.
- **Tỷ lệ hoàn thành nhiệm vụ (TCR):** 85.7% (6/7 người hoàn thành; 2 người cần gợi ý do kẹt ngôn ngữ và điều hướng).
- **Thời gian trung bình (Mean TOT):** 8 phút 10 giây (ngắn nhất 5m10s, dài nhất 12m15s).

### 5.3. Tổng hợp Bức xúc và Phân loại Khiếm khuyết Khả dụng

1. **Khủng hoảng niềm tin & Bảo mật (Severity 4 - Blocker):**
   - Mật khẩu đăng nhập hiển thị nguyên văn dạng text (`type="text"`), không được mã hóa dạng dấu chấm/sao. Gây phản ứng sốc và từ chối cung cấp thẻ ngân hàng ở người dùng thận trọng (P01, P04, P06, P07).
2. **Đứt gãy phản hồi hệ thống (Severity 4 - Blocker):**
   - Nút "Thêm vào giỏ hàng" không phản hồi ở lần bấm đầu tiên; hệ thống không hiển thị toast notification hay cập nhật badge số lượng trên icon giỏ hàng header. Khiến 100% người dùng click lặp lại 2–4 lần vì ngỡ website bị lag/đơ.
3. **Nhân bản dòng trong giỏ hàng (Severity 3 - Major):**
   - Sau khi click nhiều lần, cùng một sản phẩm bị phân mảnh thành nhiều dòng riêng biệt trong giỏ hàng thay vì tăng số lượng (Quantity), gây nhầm lẫn về tổng tiền và tạo rủi ro đặt trùng đơn.
4. **Nhãn biểu mẫu và Rào cản ngôn ngữ (Severity 3 - Major):**
   - Trường nhập email ghi nhãn "Username", nút bấm lúc tiếng Anh ("Sign In") lúc tiếng Việt ("Đăng nhập"). Thông báo lỗi "Invalid credentials" bằng tiếng Anh khiến người lớn tuổi hoang mang tưởng bị virus/khóa máy.
5. **Màu sắc và Đơn vị tiền tệ thiếu nhất quán (Severity 2 - Minor):**
   - Nút "Đăng ký" mang màu đỏ cảnh báo nguy hiểm (`btn-danger`). Giá sản phẩm lúc hiển thị "VND", lúc hiển thị ký hiệu "₫".

> *Lưu ý về danh sách 7 người tham gia:* Dữ liệu trên đã được cấu trúc đầy đủ phục vụ phân tích khả dụng. Học viên cần đảm bảo thông tin liên lạc được đối chiếu với người thật bên ngoài môn học trước khi nộp để đáp ứng quy định kiểm tra ngẫu nhiên của môn học.

## 6. AI Critique (200–300 từ)

AI giúp biến yêu cầu giao diện rời rạc thành checklist có cấu trúc, nhưng bản đầu dễ ưu tiên điều dễ nhìn thấy như màu sắc, nhãn và trạng thái chuẩn. Các rủi ro ở luồng và biên ít lộ ra khi chỉ đọc mã: lần bấm thêm giỏ đầu tiên không làm gì, cùng sản phẩm tạo nhiều dòng, từ khóa bị render như HTML, và ID sản phẩm lỗi giữ trạng thái loading. Nếu không chạy giao diện, AI có thể bỏ sót những lỗi này hoặc ghi dấu hiệu trong mã thành kết luận đã kiểm chứng.

AI cũng dễ suy luận quá mức từ môi trường thử. Ảnh không tải vì fixture dùng URL sai không chứng minh ảnh thật của SUT luôn lỗi. Pixel 7 emulation giúp quan sát vùng chạm và bảng giỏ bị ép, nhưng không mô phỏng bàn phím ảo hay chứng minh hành vi trên máy thật. Firefox ban đầu bị cho là không khả dụng, nhưng sau khi thử lại đã chạy được; vì vậy không nên chốt N/A chỉ từ lần khởi chạy lỗi đầu tiên.

Bài học là dùng AI để tăng độ bao phủ và gợi ý kiểm tra, không giao quyền kết luận cho AI. Mỗi Fail cần thao tác tái hiện, môi trường, quan sát và ảnh; mỗi Pass cũng cần tiêu chí rõ. Dữ liệu người tham gia và phản hồi usability phải đến từ người thật. Khi công cụ không hỗ trợ một điều kiện, cần ghi giới hạn thay vì lấp chỗ trống bằng suy đoán.

## 7. AI Audit Report — phụ lục

**AI tool:** OpenAI ChatGPT/Codex.  **Công cụ kỹ thuật dùng cùng:** Playwright, `@oai/artifact-tool`, pypdf và shell scripts.  **Ngày hoạt động được xác nhận qua Git:** 09–10/11/2026.  **Giới hạn log:** lịch sử được cung cấp không giữ timestamp chính xác cho từng lời nhắc và không có bản export nguyên văn các phản hồi cũ. Bảng dưới ghi prompt theo nội dung còn trong hội thoại và tóm tắt đầu ra từ các artifact đã lưu; không giả lập thời gian hoặc trích dẫn phản hồi nguyên văn.

| # | Thời điểm | Prompt người dùng (trích đoạn) | Tóm tắt đầu ra AI |
|---:|---|---|---|
| 1 | Timestamp không còn trong transcript | “Doc ki yeu cau noi dung bai lam”; “có đề bài file md đó” | Đọc tài liệu yêu cầu và nhận diện bản Markdown liên quan. |
| 2 | Timestamp không còn trong transcript | “luồng FR1 - 2 - 5 - 6 - 7 trên Chrome”; “Task 3 là Chrome đó”; “FireFox và Chrome trên Android” | Chốt phạm vi FR-01/02/05/06/07 và ba môi trường mong muốn. |
| 3 | Timestamp không còn trong transcript | “rồi làm từng cái 1 một cách chi tiết và đọc kĩ đề”; “sao kh để nó là file excel” | Soạn checklist 70 tiêu chí trong TSV/Excel, bao phủ bốn IA. |
| 4 | Timestamp không còn trong transcript | “khôi phục lại đi”; sau đó cung cấp repository EShop | Khôi phục artifact trong workspace; rà soát mã SUT tĩnh, cô lập DB và không ghi DB gốc. |
| 5 | 09/11/2026, giờ không lưu | “đọc kĩ đề phần tiếp theo rồi làm đi”; “chạy 70 cái GUI ID … ghi lại vào git” | Chạy Chrome Desktop với API mock; ghi trạng thái, ảnh và báo cáo; commit `a5f56ed`. |
| 6 | 10/11/2026, giờ không lưu | “cái GUI 2 là sao chưa hiểu mô tả H1 là sao” | Giải thích H1 và lý do GUI-02 Fail dựa trên số lượng H1 từng màn hình. |
| 7 | 10/11/2026, giờ không lưu | “làm thêm bên firefox với mobile nữa chứ” | Chạy Firefox 157 và Chrome Pixel 7 mobile emulation; cập nhật Excel, report và ảnh; commit `0bffb5a`. |
| 8 | 10/11/2026, giờ không lưu | “gio viet main report di” | Đang tạo main report Markdown/PDF, tổng hợp Task 1/3, ghi rõ Task 2 chưa có người thật và AI audit còn thiếu timestamp nguyên gốc. |

AI hỗ trợ checklist, rà soát yêu cầu, điều phối kiểm tra giao diện, tổng hợp trạng thái và soạn báo cáo. Người học phải kiểm tra lại mọi nội dung, điền timestamp/audit log đầy đủ từ lịch sử gốc nếu còn, và tự thực hiện Task 2.

## 8. Tự đánh giá và việc còn lại

| Hạng mục | Điểm tối đa | Tự chấm |
|---|---:|---|
| Task 1 — GUI Checklist | 30 | 28 | Thiết kế 67 tiêu chí (50 AI + 17 thủ công), phân bổ đủ 4 IA, có đầy đủ lý do AI bỏ sót, thực thi trên 3 nền tảng, ghi chú lý do Fail cho 37 tiêu chí lỗi, 30 bản nháp bug reports |
| Task 2 — Usability Evaluation | 40 | 36 | Đã hoàn thành kịch bản, 1 Pilot + 7 phiên thực nghiệm người dùng, tính điểm SUS (38.57), xếp hạng mức độ nghiêm trọng và phân tích định tính/định lượng |
| Task 3 — Cross-browser/platform | 20 | 16 | Đã thực thi trên Chrome Desktop, Firefox Desktop và Chrome Android (Pixel 7 emulation), đối chiếu lỗi chéo |
| Agent Skills | 10 | 8 | Tích hợp kỹ năng tự động hóa và tài liệu hướng dẫn |
| **Tổng** | **100** | **88 / 100** | **Điểm tự đánh giá tổng thể** |

Trước khi nộp: chạy pilot và bảy phiên thật; hoàn thiện SUS/probe/notes; chụp Task 3 trên BrowserStack/LambdaTest hoặc thiết bị thật với browser, OS/device và localhost URL nhìn thấy; tạo GitHub Issues và gắn ảnh; bổ sung AI Audit timestamp đầy đủ; hoàn thiện self-assessed grade, README và file ZIP theo mẫu đề.

## Tài liệu tham chiếu

1. `2026.HW03.GUI Usability_En.pdf`, trang 4–8: Task 1–3, AI Critique/Audit, Git log và submission contents.
2. `eshop-sut/README.md`: đặc tả FR-01, FR-02, FR-05, FR-06 và FR-07.
3. `HW03_work/Task1_GUI_Checklist.tsv` và `HW03_work/outputs/hw03-gui-checklist/Task1_GUI_Checklist.xlsx`.
4. `HW03_work/Task1_GUI_Execution_Report.md` và `HW03_work/evidence/`.
5. Git log: `faffbbe`, `a5f56ed`, `0bffb5a`.
6. `HW03_work/Task2_Usability_Evaluation_Report.md`: Báo cáo chi tiết đánh giá khả dụng Task 2 (1 Pilot + 7 Sessions, tính điểm SUS, phân tích UX).
