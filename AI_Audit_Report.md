       Faculty of Information Technology (FIT) – Ho Chi Minh City University of Science 
(HCMUS) 
CS423 / CSC13003 – Software Testing (AI-augmented · 2026) 
AI POLICY · TEMPLATES — 2026 v1.0 
AI Audit Report — 5-section Template per Artifact 
Mandatory appendix for every AI-assisted homework (HW#01–HW#06, and Seminar). 
Adapted from Med Kharbach, PhD (2026) — AI Use Policy Templates for Higher Education. CC BY-NC-SA 
4.0. This adaptation is prepared for FIT@HCMUS – CS423 / CSC15003 Software Testing course. 
1. Student Information 
Field 
Value 
Student name (printed): 
LE MANH PHU 
Student ID: 
23120325 
Class / Cohort: 
CQ K2023 
Assignment ID (e.g., HW#00, 
HW#02): 
HW#03 
Assignment date: 
15/11/2026 
AI tool(s) used: 
Codex, Antigravity 
AI tool(s) used: 
[X ] Yes  [ ] No 
2. Instructions (read before filling) 
• 
Add one row per AI-generated artifact (test case, script, checklist, OpenAPI spec, 
JMeter plan, etc.). 
• 
Paste the verbatim prompt — DO NOT paraphrase. 
• 
Paste the verbatim AI output (or include a labelled screenshot in the report). 
• 
Tag the verdict: VALID / INVALID / INCOMPLETE. 
• 
Reasoning must cite a course slide, ISTQB section, or technical RFC. 
• 
Show the corrected artifact with the change highlighted. 
• 
Sample rows are in italic — replace them before submission. 
3. Audit Table — one row per artifact 
(1) Prompt + Tool 
(2) AI Output 
(3) 
Ver
dict 
(4) Reasoning 
(ISTQB) 
(5) 
Student 
Fix 
Artifact #1 
Tool: Codex 
Time: 13:40 
10/11/2026 
Prompt: 
" Design a checklist 
of more than 40 
items that together 
cover all four of the 
| STT | ID | Màn hình / Phạm 
vi | Khía cạnh (IA) | Tiêu chí 
kiểm tra (Mô tả) | Kết quả 
mong đợi (Expected Result) | 
Mức độ | 
|:---:|:---|:---|:---:|:---|:-
--|:---:| 
INC
OM
PLT
E 
 
Output của AI 
đạt yêu cầu về 
Test Coverage 
(50 > 40 tiêu 
chí), phân bổ đủ 
4 khía cạnh IA 
theo mô hình 
chất lượng 
ISO/IEC 25010 
 AI chỉ lập 
luận dựa 
trên lý 
thuyết và 
mã nguồn 
tĩnh, 
không trực 
tiếp trải

SUT's interface 
aspects — general 
UI standards (IA-
01), forms (IA-02), 
navigation (IA-03), 
and feedback / 
state (IA-04). Thực 
hiện trên Eshop " 
| 1 | **GUI-01** | Toàn luồng 
| `IA-01` | Giao diện sử dụng 
nhất quán tiếng Việt trên các 
trang thuộc luồng | Nhãn, nút, 
thông báo và hướng dẫn dùng 
tiếng Việt rõ ràng | Trung 
bình | 
| 2 | **GUI-02** | Toàn luồng 
| `IA-01` | Mỗi trang có đúng 
một tiêu đề cấp một mô tả nội 
dung trang | Một H1 duy nhất, 
tên trang chính xác | Cao | 
| 3 | **GUI-03** | Toàn luồng 
| `IA-01` | Các nút hành động 
chính có màu sắc nhất quán và 
tương phản đủ | Nút hành động 
chính màu xanh theo đặc tả và 
chữ đọc rõ | Cao | 
| 4 | **GUI-04** | Toàn luồng 
| `IA-01` | Nút hủy hoặc hành 
động nguy hiểm được phân biệt 
rõ bằng màu sắc | Nút nguy 
hiểm/hủy dùng màu đỏ theo đặc 
tả và không nhầm với hành động 
chính | Trung bình | 
| 5 | **GUI-05** | Danh sách / 
chi tiết / giỏ | `IA-01` | Đơn 
vị tiền tệ được trình bày 
thống nhất bằng ký hiệu ₫ và 
phân cách hàng nghìn | Giá 
không trộn VND với ₫; định 
dạng số dễ đọc | Cao | 
| 6 | **GUI-06** | Desktop 
only - Toàn luồng | `IA-01` | 
Thứ tự focus bằng Tab đi từ 
trên xuống dưới và trái sang 
phải | Focus di chuyển theo 
thứ tự thị giác và không bị 
nhảy bất thường | Cao | 
| 7 | **GUI-07** | Desktop 
only - Toàn luồng (zoom) | 
`IA-01` | Có thể nhận biết 
focus bàn phím trên liên kết, 
trường nhập và nút | Phần tử 
(Usability: 
Learnability, 
Operability) 
và áp dụng tốt 
kỹ thuật kiểm 
thử hộp đen 
Equivalence 
Partitioning 
(EP), Boundary 
Value Analysis 
(BVA) cho các 
trường Email, 
Mật khẩu, Số 
lượng 
 
nghiệm 
ứng dụng 
đang chạy. 
AI bỏ sót 
các rủi ro 
phát sinh 
trong thực 
tế như: nút 
Thêm vào 
giỏ hàng bị 
liệt ở lần 
click đầu 
tiên (GUI-
54), dữ 
liệu giỏ 
hàng bị 
mất sạch 
sau khi 
F5/reload 
(GUI-62), 
thẻ ảnh alt 
rỗng (GUI-
12), zoom 
trình duyệt 
200% 
(GUI-13), 
và bố cục 
bảng giỏ 
hàng bị co 
ép gãy chữ 
trên điện 
thoại di 
động (GUI-
64). 
Vì vậy, 
sinh viên 
đã rà soát 
và bổ sung 
17 tiêu chí 
thực 
nghiệm để 
hoàn thiện 
bộ 
checklist 
đầy đủ 
gồm 67 
tiêu chí 
trong file 
Excel 
Checklist.x

đang focus có viền hoặc dấu 
hiệu trực quan rõ | Cao | 
| 8 | **GUI-08** | Đăng ký / 
đăng nhập | `IA-01` | Nhãn và 
điều khiển biểu mẫu có kích 
thước chữ dễ đọc ở màn hình 
thường | Không cần phóng to để 
đọc nội dung chính | Trung 
bình | 
| 9 | **GUI-09** | Toàn luồng 
| `IA-01` | Không có nội dung, 
nút hoặc trường nhập bị cắt 
hay chồng lấn ở chiều rộng 
hiện tại | Các thành phần hiển 
thị đầy đủ, không đè lên nhau 
| Cao | 
| 10 | **GUI-10** | Đăng ký / 
đăng nhập / tìm kiếm | `IA-01` 
| Trường nhập có nhãn hoặc 
placeholder diễn đạt rõ dữ 
liệu cần nhập | Người dùng 
hiểu trường cần họ tên, email, 
mật khẩu hay từ khóa tìm kiếm 
| Trung bình | 
| 11 | **GUI-11** | Toàn luồng 
| `IA-01` | Màu chữ và nền có 
độ tương phản đủ để đọc | Nội 
dung chính vẫn đọc được trên 
nền và trạng thái tương tác | 
Cao | 
| 12 | **GUI-12** | Đăng ký / 
đăng nhập / danh sách | `IA-
02` | Tất cả trường bắt buộc 
có dấu * cạnh nhãn theo đặc tả 
| Mỗi trường bắt buộc được 
nhận biết trước khi gửi form | 
Cao | 
| 13 | **GUI-13** | Đăng ký | 
`IA-02` | Trường Họ tên nhận 
dữ liệu văn bản và hiển thị 
nội dung vừa nhập | Nội dung 
không bị cắt bất thường và có 
thể sửa trước khi gửi | Trung 
bình | 
lsx.

| 14 | **GUI-14** | Đăng ký / 
đăng nhập | `IA-02` | Trường 
Email dùng kiểu email và bàn 
phím nhập email phù hợp | 
Trình duyệt nhận biết email; 
Android có thể hiện bàn phím 
email phù hợp | Cao | 
| 15 | **GUI-15** | Đăng ký | 
`IA-02` | Email sai định dạng 
bị phát hiện và có thông báo 
dễ hiểu | Người dùng biết cách 
sửa email trước khi tiếp tục | 
Cao | 
| 16 | **GUI-16** | Đăng ký | 
`IA-02` | Email đã đăng ký 
được phản hồi bằng thông báo 
phù hợp | Thông báo không làm 
mất dữ liệu đã nhập và cho 
biết cách xử lý | Cao | 
| 17 | **GUI-17** | Đăng ký / 
đăng nhập | `IA-02` | Trường 
mật khẩu che ký tự khi nhập | 
Ký tự mật khẩu không hiển thị 
dạng văn bản thường | Cao | 
| 18 | **GUI-18** | Đăng ký | 
`IA-02` | Hướng dẫn mật khẩu 
mạnh nêu đủ điều kiện theo đặc 
tả | Hướng dẫn dễ tìm và nêu 
độ dài, chữ hoa/thường, số, ký 
tự đặc biệt | Cao | 
| 19 | **GUI-19** | Đăng ký | 
`IA-02` | Mật khẩu thiếu điều 
kiện bị từ chối với lỗi gần 
biểu mẫu và dễ hiểu | Lỗi xuất 
hiện trước nút gửi theo yêu 
cầu giao diện | Cao | 
| 20 | **GUI-20** | Đăng ký | 
`IA-02` | Form có trường xác 
nhận mật khẩu và từ chối khi 
hai mật khẩu khác nhau | Hai 
trường được đối chiếu trước 
khi tạo tài khoản | Cao | 
| 21 | **GUI-21** | Đăng nhập 
| `IA-02` | Gửi form thiếu dữ

liệu được chặn và thông báo 
ngay tại trường liên quan | 
Người dùng hiểu trường nào cần 
hoàn tất | Cao | 
| 22 | **GUI-22** | Đăng nhập 
| `IA-02` | Đăng nhập sai hiển 
thị lỗi ở vị trí dễ thấy phía 
trên nút gửi | Lỗi rõ ràng, 
không chỉ dựa vào màu sắc | 
Cao | 
| 23 | **GUI-23** | Tìm kiếm | 
`IA-02` | Người dùng có thể 
sửa hoặc xóa từ khóa tìm kiếm 
dễ dàng | Giá trị từ khóa hiện 
tại nhìn thấy và có thể chỉnh 
sửa | Trung bình | 
| 24 | **GUI-24** | Chi tiết 
sản phẩm | `IA-02` | Ô số 
lượng chỉ nhận số nguyên dương 
và giá trị nhỏ nhất là 1 | Giá 
trị 0, âm, thập phân hoặc 
không phải số bị chặn hay báo 
lỗi | Cao | 
| 25 | **GUI-25** | Toàn luồng 
| `IA-02` | Thông báo lỗi xuất 
hiện phía trên nút submit theo 
đặc tả form | Lỗi ở đúng vị 
trí quy định và không bị khuất 
| Cao | 
| 26 | **GUI-26** | Đăng ký → 
đăng nhập | `IA-03` | Sau đăng 
ký thành công, người dùng được 
đưa tới trang đăng nhập | Điều 
hướng đúng trang và có thể 
nhận biết trạng thái hoàn tất 
| Cao | 
| 27 | **GUI-27** | Đăng ký / 
đăng nhập | `IA-03` | Liên kết 
chuyển qua lại giữa đăng ký và 
đăng nhập có nội dung rõ | 
Liên kết dễ nhận ra và tới 
đúng trang đích | Cao | 
| 28 | **GUI-28** | Đăng nhập 
| `IA-03` | Liên kết Quên mật

khẩu mở đúng luồng khôi phục 
mật khẩu | Liên kết hoạt động 
và không làm mất hướng quay 
lại đăng nhập | Cao | 
| 29 | **GUI-29** | Header / 
toàn luồng | `IA-03` | Logo 
hoặc tên EShop đưa người dùng 
về trang danh sách sản phẩm | 
Nhấp/activate đưa về trang chủ 
ổn định | Cao | 
| 30 | **GUI-30** | Header / 
giỏ hàng | `IA-03` | Liên kết 
Giỏ hàng luôn dễ tìm từ các 
trang thuộc luồng | Nhãn hiển 
thị rõ và vùng bấm đủ dùng 
trên thiết bị tương ứng | Cao 
| 
| 31 | **GUI-31** | Header / 
giỏ hàng | `IA-03` | Badge giỏ 
hàng phản ánh số lượng sản 
phẩm theo đặc tả | Sau thao 
tác thêm, số hiển thị cập nhật 
và dễ nhận biết | Cao | 
| 32 | **GUI-32** | Danh sách 
sản phẩm | `IA-03` | Liên kết 
Xem chi tiết mở đúng sản phẩm 
đã chọn | Thông tin nhận diện 
sản phẩm khớp với thẻ được 
chọn | Cao | 
| 33 | **GUI-33** | Chi tiết 
sản phẩm / giỏ hàng | `IA-03` 
| Có breadcrumb ở trang chi 
tiết sản phẩm và trang giỏ 
hàng | Breadcrumb thể hiện vị 
trí và cho phép quay lại trang 
cha | Cao | 
| 34 | **GUI-34** | Danh sách 
sản phẩm | `IA-03` | Từ khóa 
tìm kiếm được gửi đúng khi 
nhấn Enter hoặc nút Tìm | Cả 
hai cách kích hoạt cho kết quả 
tương đương | Cao | 
| 35 | **GUI-35** | Danh sách 
sản phẩm | `IA-04` | Trong lúc

tải sản phẩm có chỉ báo 
loading dễ nhận biết | Không 
để người dùng tưởng trang bị 
treo | Cao | 
| 36 | **GUI-36** | Danh sách 
sản phẩm | `IA-04` | Tìm kiếm 
không có kết quả hiển thị 
empty state thân thiện và 
hướng xử lý | Thông báo rõ 
không có kết quả và gợi ý đổi 
từ khóa | Cao | 
| 37 | **GUI-37** | Danh sách 
sản phẩm | `IA-04` | Lỗi tải 
danh sách sản phẩm được báo 
rõ, không hiển thị trang trống 
khó hiểu | Người dùng nhận 
biết vấn đề và có cách thử lại 
hoặc tiếp tục | Cao | 
| 38 | **GUI-38** | Đăng ký / 
đăng nhập | `IA-04` | Khi gửi 
biểu mẫu, người dùng nhận biết 
hệ thống đang xử lý | Trạng 
thái gửi hoặc phản hồi thành 
công/lỗi xuất hiện kịp thời | 
Cao | 
| 39 | **GUI-39** | Đăng nhập 
| `IA-04` | Đăng nhập thành 
công đưa người dùng về trang 
sản phẩm và thể hiện trạng 
thái đăng nhập | Trang đích 
đúng và tài khoản đang đăng 
nhập được nhận biết | Cao | 
| 40 | **GUI-40** | Danh sách 
sản phẩm | `IA-04` | Từ khóa 
người dùng nhập được hiển thị 
an toàn như văn bản thuần | Từ 
khóa không được diễn giải 
thành HTML hoặc làm hỏng bố 
cục | Cao | 
| 41 | **GUI-41** | Danh sách 
sản phẩm | `IA-04` | Mỗi sản 
phẩm hiển thị ảnh, tên và giá 
trong trạng thái tải thành 
công | Nội dung cần chọn mua

hiện rõ, ảnh đúng sản phẩm | 
Cao | 
| 42 | **GUI-42** | Chi tiết 
sản phẩm | `IA-04` | Trong lúc 
tải chi tiết, có loading; lỗi 
hoặc ID không hợp lệ có thông 
báo hữu ích | Không để người 
dùng gặp trang trắng hoặc 
trạng thái treo | Cao | 
| 43 | **GUI-43** | Chi tiết 
sản phẩm | `IA-04` | Sau một 
lần nhấn Thêm vào giỏ, có phản 
hồi trực quan rõ ràng | Thông 
báo toast hoặc badge giỏ được 
cập nhật ngay sau thao tác | 
Cao | 
| 44 | **GUI-44** | Giỏ hàng | 
`IA-04` | Giỏ trống có 
hình/icon minh họa, thông báo 
rõ và liên kết tiếp tục mua 
sắm | Empty state thân thiện 
và có hướng đi tiếp | Cao | 
| 45 | **GUI-45** | Giỏ hàng | 
`IA-04` | Giỏ có sản phẩm hiển 
thị tên, đơn giá, số lượng và 
thành tiền chính xác, dễ đối 
chiếu | Các cột không bị nhầm; 
thành tiền tương ứng số lượng 
và đơn giá | Cao | 
| 46 | **GUI-46** | Giỏ hàng | 
`IA-04` | Tổng tiền dùng nhãn 
chính xác “Tổng cộng” và số 
tiền dễ nhận biết | Nhãn, định 
dạng và đơn vị thống nhất theo 
đặc tả | Cao | 
| 47 | **GUI-47** | Giỏ hàng | 
`IA-04` | Xóa sản phẩm yêu cầu 
xác nhận trước khi xóa | 
Dialog nêu hành động và cho 
phép hủy hoặc xác nhận | Cao | 
| 48 | **GUI-48** | Giỏ hàng | 
`IA-04` | Sau khi xác nhận 
xóa, danh sách và tổng tiền 
được cập nhật nhất quán | Nếu

xóa dòng cuối, giao diện 
chuyển sang empty state phù 
hợp | Cao | 
| 49 | **GUI-49** | Giỏ hàng | 
`IA-04` | Thêm cùng một sản 
phẩm nhiều lần tăng số lượng 
của dòng hiện có | Không tạo 
dòng trùng lặp cho cùng sản 
phẩm | Cao | 
| 50 | **GUI-50** | Toàn luồng 
| `IA-01` | Giao diện vẫn sử 
dụng được khi hệ điều hành bật 
chế độ tối hoặc ép màu tương 
phản cao | Chữ, viền, trạng 
thái focus và nút vẫn nhận 
biết được | Trung bình | 
 
 
Artifact #2: 
Tool: Codex 
Time: 21:10 
10/11/2026 
Prompt: “ Dựa vào 
file excel tôi đã hoàn 
thiện 67 GUI hãy 
viết đánh giá giúp 
tôi”. 
 
 
I. Task 1 — GUI Checklist  
  
1. SUT và phạm vi  
  
- Luồng chọn: FR-01 Đăng ký → FR-02 Đăng 
nhập → FR-05 Danh sách/tìm kiếm → FR-06 
Chi  
  
tiết → FR-07 Giỏ hàng.  
  
  
  
- SUT là EShop, mã nguồn do môn học cung 
cấp tại `eshop-sut`. Phạm vi GUI tập trung vào 
FR-  
  
01, FR-02, FR-05, FR-06 và FR-07; không đánh 
giá checkout, admin hoặc các luồng ngoài lựa  
  
chọn.  
  
  
  
- Luồng nhiệm vụ mục tiêu là người dùng mới 
tạo tài khoản, đăng nhập, tìm một sản phẩm, 
mở  
  
chi tiết và kiểm tra sản phẩm trong giỏ. Các 
màn hình được xem: đăng ký, đăng nhập, 
danh sách  
  
sản phẩm, chi tiết sản phẩm và giỏ hàng.  
  
  
  
2. Task 1 - Thiết kế GUI checklist  
 
VALI
D 
Output AI đẩy 
đủ và đạt quy 
trình kiểm thử 
ISTQB (Test 
Completion). 
Ngoài ra, AI 
phản ánh chính 
xác độ bao phủ 
(Test Coverage: 
67 tiêu chí trên 
5 màn hình 
luồng cốt lõi) và 
phân loại mạch 
lạc theo 4 khía 
cạnh giao diện 
tương ứng mô 
hình chất lượng 
ISO/IEC 25010 
(Usability & 
Functional 
Suitability). 
Sinh viên 
cần rà soát 
lại các kết 
quả trong 
báo cáo 
đúng với 
các số liệu 
trong 
excel.

- Checklist hoàn chỉnh trong file Excel 
Task1_GUI_Checklist.xlsx gồm 67 tiêu chí, 
phân bổ toàn  
  
diện trên cả 4 khía cạnh giao diện (Interface 
Aspects - IA):  
  
  
  
  
  
  
  
Khía cạnh giao diện     Số lượng      Tỷ lệ (%)     
Phạm vi bao phủ chính  
  
(Interface Aspect)      tiêu chí  
  
  
  
  
  
IA-01 - General                  18 26.9%          Ngôn 
ngữ tiếng Việt, cấu trúc Heading  
  
UI standards                                       H1, màu sắc 
nút CTA, đơn vị tiền tệ,  
  
                                                    typography, tương 
phản màu sắc  
  
IA-02 - Forms                    18 26.9%          Nhãn 
trường nhập liệu, định dạng  
  
                                                    email/mật khẩu, 
đánh dấu bắt buộc,  
  
                                                    validation, kiểu 
bàn phím số lượng  
  
IA-03 - Navigation               12 17.9%          Phân 
trang, lọc danh mục, breadcrumb,  
  
                                                    kích thước vùng 
chạm (touch targets),  
  
                                                    luồng điều hướng 
nút  
  
                                                    Back  
  
IA-04 - Feedback /               19 28.3%          Phản 
hồi thêm giỏ hàng, thông báo  
  
state                                              toast/badge, 
trạng thái rỗng (empty  
  
                                                    state), xử lý lỗi tải, 
bảo lưu giỏ qua

reload  
  
Tổng cộng                        67 100%           Toàn 
diện 5 màn hình thuộc luồng  
  
                                                    mua sắm cốt lõi  
  
  
  
- Đóng góp giữa AI và Rà soát Thủ công (AI vs. 
Human Review)  
  
+ Nguồn "AI ban đầu": 50 tiêu chí. AI cung cấp 
khung checklist tiêu chuẩn tốt về quy chuẩn 
giao  
  
diện tổng quát (nhãn tiếng Việt, màu sắc, bố 
cục không tràn  
  
ngang, các trường form cơ bản).  
  
+ Nguồn "Bổ sung thủ công": 17 tiêu chí. Đây 
là các tiêu chí mang tính chuyên sâu mà AI ban  
  
đầu đã bỏ sót do hạn chế của mô hình ngôn 
ngữ khi không trực tiếp tương tác thực tế với 
ứng  
  
dụng. Cụ thể:  
  
1. Khả năng tiếp cận & Phóng to (Accessibility 
& Zoom): Kiểm tra thẻ alt rỗng  
  
của ảnh sản phẩm (GUI-12), khả năng co giãn 
bố cục khi zoom 200% (GUI-13), liên kết nhãn  
  
với control for/id (GUI-15).  
  
  
  
  
  
  
  
2. Hành vi biên và Ngoại lệ (Edge cases & 
Error Handling): Rủi ro lộ mật khẩu  
  
plain-text khi chạy thực tế (GUI-25), kiểm tra 
lỗi mạng và fallback nội dung  
  
(GUI-51), phản hồi bất thường khi nút không 
kích hoạt ở lần bấm đầu (GUI-54).  
  
  
  
  
  
  
  
3. Tính liên tục trạng thái (State Continuity & 
Persistence): Kiểm tra dữ liệu giỏhàng có

được lưu  
  
trữ bền vững qua các lần reload/F5 hay không 
(GUI-62), thời gian hiển thị và sự tự biến mất 
của  
  
thông báo toast (GUI-55).  
  
  
  
  
  
  
  
4. Đặc thù Responsive thiết bị di động (Mobile 
Specifics): Vùng chạm tối thiểu trên màn hình  
  
cảm ứng (GUI-41), bố cục bảng giỏ hàng bị co 
ép chữ trên màn hình hẹp (GUI-64), khả năng  
  
hiển thị tương thích RTL (GUI-67).  
  
  
  
+ Tất cả 17 tiêu chí bổ sung đều được ghi rõ lý 
do AI bỏ sót tại cột H ("Lý do AI bỏ sót") trong  
  
file Excel để đáp ứng đầy đủ yêu cầu của đề 
bài.  
 
  
  
3. Kết quả thực thi checklist:  
  
  
  
                                                                                    Đã 
đánh  
  
        Nền tảng                PASS        FAIL                
N/A                    giá  
  
  
  
                                                   3 (Mobile Only: 
GUI-41,  
  
Chrome Desktop             28          36                           
64/67  
  
                                                   GUI-63, GUI-64)  
  
                                                   3 (Mobile Only: 
GUI-41,  
  
Firefox Desktop            28          36                              
64/67  
  
                                                   GUI-63, GUI-64)  
  
Chrome Android                                     4

(Desktop Only: GUI-06,  
  
                           32          31                                         
63/67  
  
emulation                                          GUI-07, GUI-
13, GUI-40)  
  
  
  
Tổng hợp và Phân nhóm 37 Lỗi Giao diện Phát 
hiện được  
  
- Toàn bộ 37 tiêu chí FAIL duy nhất được tổng 
hợp, phân tích nguyên nhân và gom thành 30 
bản  
  
bug trên GitHub Issues kèm ảnh chụp bằng 
chứng  
  
Artifact #3 
Tool: Antigravity 
Time: 12/11/2026 
20:41 
Prompt:  
Dựa vào kịch bản 
kiểm thử này: “Bạn là 
một khách hàng lần 
đầu tiên ghé thăm 
website thương mại 
điện tử EShop. Bạn 
đang  
có nhu cầu tìm mua 
một thiết bị điện tử 
hoặc phụ kiện công 
nghệ phù hợp với 
nhu cầu hàng  
ngày. 
Hãy tạo một tài 
khoản mới, đăng 
nhập vào hệ thống, 
tìm sản phẩm bạn 
ưng ý, kiểm tra kỹ  
thông tin chi tiết và 
thêm sản phẩm đó 
vào giỏ hàng với số 
lượng mong muốn để 
chuẩn bị  
thanh toán. 
Trong suốt quá trình 
thực hiện, bạn hãy 
vừa thao tác vừa suy 
nghĩ thành lời (Think-
Aloud) 
bất kỳ điều gì bạn 
đang nhìn thấy, dự 
định làm, cảm thấy 
1. Mục tiêu đánh giá 
(Objectives)  
Đánh giá mức độ hiệu quả 
(Effectiveness), hiệu suất (Efficiency) 
và sự hài lòng (Satisfaction)  
của người dùng cuối khi trải nghiệm 
luồng mua sắm cốt lõi trên ứng dụng 
EShop. Cụ thể:  
1. Khả năng tự khám phá và 
định hướng (Discoverability 
& Learnability): Người dùng 
lần  
đầu tiên truy cập có thể tự tạo tài 
khoản, đăng nhập và tìm kiếm sản 
phẩm mong muốn mà không  
cần người hướng dẫn hay không?  
2. Nhận diện điểm nghẽn tương 
tác (Cognitive Bottlenecks): 
Xác định các bước người dùng  
lúng túng, do dự hoặc thao tác sai do 
quy ước giao diện không nhất quán 
(nhãn nhập liệu, phản  
hồi trạng thái, màu sắc CTA).  
3. Phản hồi trạng thái hệ thống 
(Feedback & State Recovery): 
Kiểm tra phản ứng và khả  
năng tự xử lý của người dùng trước 
các lỗi thực tế của SUT (nút “Thêm 
vào giỏ” không phản hồi  
lần đầu, mật khẩu hiển thị plain-text, 
sản phẩm trùng lặp tạo nhiều dòng 
trong giỏ hàng).  
4. Mức độ tin cậy và an tâm 
 
INC
OMP
LeT
E 
AI đạt yêu cầu 
cao về Test 
Preparation & 
Usability Test 
Design theo 
chuẩn ISO 
9241-11 và 
ISO/IEC 25010, 
xác định đúng 3 
mục tiêu cốt lõi: 
Tính hiệu quả 
(Effectiveness), 
Hiệu suất 
(Efficiency) và 
Sự hài lòng 
(Satisfaction). 
AI chuẩn bị đầy 
đủ bộ công cụ 
đo lường chuẩn 
hóa 
(Standardized 
Questionnaire 
— SUS) kèm 
công thức tính 
điểm chuẩn 
Brooke (1996), 
cùng bộ câu hỏi 
phỏng vấn sâu 
(Probe 
Questions) 
Sinh viên 
trực tiếp 
tiến hành 
phiên thử 
nghiệm sơ 
bộ (Pilot 
Session) 
trong thực 
tế với đối 
tượng P00 
(Lê Mạnh 
Phú, 22 
tuổi, Sinh 
viên IT). 
Đo đạc và 
điền chính 
xác thời 
gian hoàn 
thành thực 
tế là 6 
phút 15 
giây. Ghi 
nhận phát 
hiện thực 
nghiệm 
quan 
trọng: 
người 
tham gia 
thường im 
lặng khi 
thao tác, từ 
đó bổ sung

hài lòng hoặc gặp 
khó khăn.” 
Thực hiện  
1. Define your 
objectives. State 
clearly what you want 
to learn — for 
example, where 
users hit 
navigation 
bottlenecks on the 
chosen flow, or how 
confident they feel 
completing it. 
2. Prepare the 
instruments. A 
standard usability 
scale to be 
completed after each 
session — SUS 
or UEQ-S (or a 
custom scale with a 
clear written 
justification) — plus a 
short set of open-
ended 
probe questions 
covering, at 
minimum: clarity, 
error recovery, 
speed, and trust. 
3. Run a pilot 
session with one 
person to catch an 
unclear scenario, 
broken flow, or 
timing 
problems; refine 
before the real 
sessions. Người 
pilot này mục tiêu là 
gì  
(Trust & Confidence): Đánh 
giá tâm lý người dùng khi 
cung cấp  
thông tin cá nhân và mật khẩu trên hệ 
thống.  
. Công cụ đo lường và Đánh giá 
(Evaluation Instruments)  
A. Thang đo khả dụng chuẩn (System 
Usability Scale — SUS)  
Thang đo SUS gồm 10 câu hỏi tiêu 
chuẩn quốc tế, đánh giá theo thang 
Likert 5 mức độ (1: Rất  
không đồng ý ➔ 5: Rất đồng ý):  
Q1 (+): Tôi nghĩ rằng tôi sẽ muốn sử 
dụng website này thường xuyên.  
Q2 (-): Tôi thấy website này phức tạp 
không cần thiết.  
Q3 (+): Tôi thấy website này dễ sử 
dụng.  
Q4 (-): Tôi nghĩ rằng tôi cần sự hỗ trợ 
của một chuyên gia kỹ thuật để có thể 
sử dụng website  
này.  
Q5 (+): Tôi nhận thấy các chức năng 
trên website được tích hợp rất tốt.  
Q6 (-): Tôi thấy có quá nhiều điều 
không nhất quán trên website này.  
Q7 (+): Tôi nghĩ phần lớn mọi người 
sẽ học được cách sử dụng website 
này rất nhanh chóng.  
Q8 (-): Tôi thấy website này rất cồng 
kềnh, rắc rối khi sử dụng.  
Q9 (+): Tôi cảm thấy rất tự tin khi 
thao tác trên website này.  
Q10 (-): Tôi phải học rất nhiều điều 
trước khi có thể làm quen và sử dụng 
website này.  
Công thức tính điểm SUS chuẩn:  
 Đối với câu hỏi lẻ 
(i∈{1,3,5,7,9}): Xi=Scorei−1  
 Đối với câu hỏi chẵn 
(j∈{2,4,6,8,10}): Yj =5−Scorej  
 Tổng điểm SUS của người 
tham gia: SUS 
Score=2.5×(∑Xi+∑Yj)  
(Thang điểm từ 0 đến 100, chuẩn 
công nghiệp trung bình là 68.0 điểm).  
B. Bộ câu hỏi phỏng vấn sâu sau phiên  
Clarity (Độ rõ ràng): Các thông tin về 
lời dặn dò 
chuẩn hóa 
trước 
phiên 
nhằm 
khích lệ 
người 
tham gia 
tích cực 
suy nghĩ 
thành lời 
(Think-
Aloud). Bổ 
sung đầy 
đủ thông 
tin nhân 
khẩu học 
của P00 
vào bảng 
danh sách 
người 
tham gia 
trong file 
báo cáo 
chính 
MainRepor
t.pdf

sản phẩm, nhãn form (VD: đăng 
kí/đăng nhập), nút bấm  
và thông báo lỗi có dễ hiểu và rõ ràng 
đối với bạn không?  
Error Recovery (Khả năng khôi phục 
lỗi): Khi bạn bấm nhầm hoặc gặp trục 
trặc (ví dụ bấm  
nút mà không thấy phản hồi), bạn đã 
xử lý như thế nào để tiếp tục?  
Speed & Efficiency (Tốc độ & Hiệu 
quả): Bạn cảm thấy tốc độ duyệt qua 
các bước từ tìm sản  
phẩm đến khi thấy hàng trong giỏ 
như thế nào? Có bước nào gây mất 
thời gian không đáng có?  
Trust (Độ tin cậy): Bạn có cảm thấy 
an tâm khi nhập mật khẩu và mua 
hàng trên trang web này  
không? Có chi tiết nào làm bạn nghi 
ngờ về tính bảo mật?  
3. Phiên thử nghiệm sơ bộ (Pilot 
Session — P00)  
Mục tiêu: Kiểm tra tính khả thi của 
kịch bản, độ trôi chảy của môi trường 
giả lập SUT, độ rõ  
ràng của bộ câu hỏi SUS tiếng Việt và 
đo lường khung thời gian hợp lý  
Diễn biến: P00 hoàn thành kịch bản 
trong bao lâu ?  
Phát hiện từ Pilot:  
Vấn đề hướng dẫn Think-Aloud: 
Người tham gia thường im lặng khi 
đọc thông tin hay trong lúc  
thực hiện kịch bản; người điều phối 
cần nhắc nhở nhẹ nhàng trước khi 
thực hiện là: “Bạn cứ thoải mái nói ra 
suy nghĩ khi gặp khó khăn hay thắc 
mắc.” mà không can thiệp vào hành 
động.  
Công cụ SUS: P00 hiểu trọn vẹn 10 
câu hỏi tiếng Việt, không bị khúc mắc 
thuật ngữ.  
Artifact #4 
Tool: Antigravity 
Time: 12/11/2026 
20:41 
Prompt: “Tôi đã thực 
nghiệm và khảo sát 
đầy đủ thông tin bao 
gồm 7 người trong 
Phân tích, Tổng hợp và Báo cáo  
  
  
       1. Bảng ma trận Điểm số SUS và 
Thống kê tổng hợp  
  
       Sau khi kết thúc từng phiên thực 
nghiệm, cả 07 người tham gia (P01 đến 
 
INC
OMP
LET
E 
AI đạt yêu cầu 
cao về Test 
Preparation & 
Usability Test 
Design theo 
chuẩn ISO 
9241-11 và 
ISO/IEC 25010, 
Sinh viên 
phải kiểm 
tra toàn bộ 
phần số 
liệu, tính 
toán AI 
làm. Ngoài 
ra, phải ghi

file MainReport.word 
ấy. 
Score the SUS / UEQ-S 
results across the seven 
participants. 
Synthesise your notes: 
group similar pain 
points together, and 
separate isolated bugs 
from 
systemic design issues. 
Prioritise by severity 
(for example, blockers 
that prevent task 
completion versus 
minor visual 
complaints). 
 
 
P07) đều hoàn thành  
  
       độc lập phiếu khảo sát System 
Usability Scale (SUS) 10 câu hỏi chuẩn 
Likert. Dữ liệu điểm từng  
  
       câu và tổng điểm SUS quy đổi theo 
công thức chuẩn (Brooke, 1996) được 
tổng hợp chi tiết trong  
  
       bảng dưới đây:  
 
  
Người tham gia    Q1     Q2   Q3     Q4    Q5    
Q6      Q7      Q8   Q9   Q10 Điểm Xếp loại 
Mức chấp  
  
                                                                               
SUS           nhận  
  
P01 (Ngô Phúc     3      3    3      2     3     4       
4       3    2    2   52.5    D       Marginal  
  
Lộc)                                                                           
Low  
  
P02 (Mai Huy      2      4    2      4     2     3       
3       4    3    3   35.0    F       Not  
  
Hoàng)                                                                      
Acceptable  
  
P03 (Phan Đặng    3      3    3      3     4     2       
3       3    3    3   55.0    D       Marginal  
  
Quốc Đạt)                                                                
Low  
  
P04 (Lê Như       2      2    3      2     2     2       
3       2    2    2   55.0    D       Marginal  
  
Hảo)                                                                          
Low  
  
P05 (Đinh Lê      2      3    2      3     3     2       
3       3    2    3   45.0    F       Not  
  
Quốc Hải)                                                                 
Acceptable  
  
P06 (Lê Phước     2      4    2      4     3     3       
3       4    2    4   32.5    F       Not  
  
Hào)                                                                          
Acceptable  
xác định đúng 3 
mục tiêu cốt lõi: 
Tính hiệu quả 
(Effectiveness), 
Hiệu suất 
(Efficiency) và 
Sự hài lòng 
(Satisfaction). 
AI đưa ra các 
đánh giá tổng 
hợp khá đầy đủ 
và chi tiết 
lỗi trên 
github 
issue cho 
phần task2

P07 (Đặng Thị     2      3    2      4     3     2       
3       4    3    4   40.0    F       Not  
  
Thúy Hoàn)                                                             
Acceptable  
  
TRUNG BÌNH        2.29   3.14 2.43 3.14 
2.86 2.57        3.14 3.14 2.43 3.00   45.00   
F      Not  
  
(Mean)                                                                      
(POOR) Acceptable  
  
  
  
  
  
  
  
       Phân tích định lượng kết quả SUS 
theo chuẩn công nghiệp (Sauro & Lewis, 
2016):  
  
       • Điểm SUS trung bình tổng thể: Đạt 
45.00 / 100 điểm với độ lệch chuẩn SD = 
9.46. Điểm số  
  
       cao nhất là 55.0 (P03, P04) và thấp 
nhất là 32.5 (P06).  
  
       • Đối chuẩn công nghiệp (Industry 
Benchmark): Mức điểm chuẩn trung bình 
của các ứng  
  
       dụng phần mềm toàn cầu là 68.0 
điểm. Mức điểm 45.00 của EShop rơi vào 
phân vị thứ 12%  
  
       (12th Percentile), thuộc mức xếp loại 
Hạng F (Grade F - POOR), nằm trong vùng 
Không thể  
  
       chấp nhận được (Not Acceptable).  
  
       • Chỉ số Net Promoter Score (NPS): 
100% người tham gia (7/7 người) đều 
rơi vào nhóm  
  
       Detractor (người phản đối, điểm câu 
hỏi sẵn sàng khuyến nghị <= 6). Khách 
hàng không an tâm  
  
       để giới thiệu website cho người thân 
sử dụng.

2. Phân tích chỉ số hiệu năng thực thi  
  
       Bên cạnh chỉ số đánh giá cảm nhận 
SUS, các thông số hiệu năng thao tác 
khách quan thu thập  
  
       trực tiếp trong 07 phiên được tổng 
hợp như sau:  
  
  
  
  
  
     Chỉ số hiệu năng (Metric)   Kết quả đo 
lường thực tế (N      Đánh giá & Ngưỡng 
kỳ vọng  
  
                                             = 7)                            
UX  
  
Tỷ lệ hoàn thành nhiệm vụ       100% (7/7 
người hoàn thành)      Cả 7 người đều đưa 
được sản  
  
(TCR)                                                            
phẩm vào giỏ hàng thành công.  
  
Tỷ lệ tự hoàn thành độc lập       85.7% 
(6/7 người độc lập)      Bác Lê Phước Hào 
(P06) cần  
  
                                                                  người 
điều phối gợi ý do kẹt ở  
  
                                                                  ô 
Username.  
  
Thời gian trung bình (Mean         8 phút 
28 giây (508 giây)     Rất cao so với luồng 
mua sắm  
  
TOT)                                                             cơ 
bản (ngưỡng kỳ vọng thông  
  
                                                                  thường 
< 3 phút).  
  
Thời gian nhanh nhất / lâu      6m33s 
(P05) / 11m56s (P06)       Người trẻ quen 
công nghệ nên  
  
nhất                                                             thao

tác nhanh hơn; người lớn  
  
                                                                  tuổi 
mất thời gian dò lỗi.  
  
Tỷ lệ cần trợ giúp (Assist      14.3% (1/7 
người cần trợ giúp)   Người lớn tuổi gặp 
trở ngại lớn  
  
Rate)                                                            với 
nhãn form và thông báo lỗi  
  
                                                                  kỹ 
thuật.  
  
Tần suất thao tác lỗi (Error            2.6 lỗi / 
phiên          Tập trung ở: nhập họ tên vào  
  
Rate)                                                            
Username, click dư thừa nút  
  
                                                                  Thêm 
giỏ, kẹt logo EShop.  
  
  
  
  
  
  
  
3. Tổng hợp Bức xúc & Phân loại Khiếm 
khuyết Khả dụng (Thematic UX  
  
Synthesis)  
  
Dựa trên biên bản quan sát thao tác và 
trích dẫn suy nghĩ thành lời (Think-
Aloud) của 7 người  
  
tham gia, các vấn đề khả dụng được phân 
loại rõ ràng thành 2 nhóm:  
  
  
  
A. Nhóm Khiếm khuyết Thiết kế Hệ thống 
(Systemic UX Flaws):  
  
1. Quy ước nhãn nhập liệu đánh đố người 
dùng (Username vs. Email): Trường nhập 
liệu  
  
đăng nhập hiển thị nhãn "Username" 
nhưng hệ thống lại yêu cầu định dạng 
Email. 6/7 người

tham gia (P01, P02, P03, P05, P06, P07) 
đều gõ họ tên theo phản xạ tự nhiên và 
nhận thông  
  
báo lỗi đăng nhập. Người tham gia P06 
phải thử lại 3-4 lần và bế tắc hoàn toàn 
nếu không có gợi  
  
ý.  
  
2. Đứt gãy phản hồi thao tác Thêm vào 
giỏ hàng (System Feedback Failure): Nút 
"Thêm vào  
  
giỏ hàng" không phản hồi ở lần bấm đầu 
tiên, không có thông báo toast thành công 
và icon giỏ  
  
hàng trên thanh header không cập nhật 
số badge. 100% người tham gia (7/7 
người) đều tưởng  
  
website bị lag hoặc chưa nhận lệnh nên 
đã bấm liên tiếp từ 2 đến 4 lần.  
  
3. Đứt gãy luồng điều hướng quay lại 
trang chủ (Navigation Bottleneck): Sau 
khi tìm kiếm  
  
không ra sản phẩm, người dùng nhấn vào 
Logo EShop để quay về trang chủ nhưng 
logo không  
  
hoạt động. 4/7 người tham gia (P01, P02, 
P05, P07) bị lúng túng mất phương 
hướng, phải dùng  
  
nút Back của trình duyệt hoặc xóa thanh 
tìm kiếm rồi Enter để quay lại.  
  
4. Thiếu hoàn toàn hình ảnh và mô tả sản 
phẩm (Catalog / Content Defect): Trang 
chi tiết  
  
sản phẩm không có ảnh minh họa và 
không có mô tả tính năng. Người tham gia 
(P01, P02, P04,  
  
P05) đều bày tỏ sự thất vọng: "Sao không 
có hình ảnh gì hết trơn vậy", "Không có 
mô tả gì sao  
  
lựa", làm giảm sút nghiêm trọng tính 
thuyết phục mua hàng.

5. Khả năng tiếp cận kém và thiếu xác 
nhận mật khẩu (Accessibility & Form 
Validation):  
  
Dòng chữ hướng dẫn quy cách mật khẩu 
quá nhỏ và mờ (P04, P06 phải lấy kính 
đeo mới đọc  
  
  
  
  
  
được). Form đăng ký thiếu trường "Xác 
nhận mật khẩu" (Confirm Password) 
khiến 4 người  
  
(P01, P03, P04, P05) lo sợ gõ sai ký tự mà 
không biết.  
  
  
  
B. Nhóm Lỗi Kỹ thuật Cô lập (Isolated 
Functional Bugs):  
  
1. Nhân bản dòng sản phẩm trong giỏ 
hàng (Cart Duplication): Khi người dùng 
bấm thêm  
  
nhiều lần do thiếu phản hồi, hệ thống 
không cộng dồn số lượng (Quantity) mà 
tạo thành các dòng  
  
riêng biệt cho cùng một sản phẩm (P02 bị 
nhân bản thành 4 dòng riêng biệt).  
  
2. Lộ mật khẩu đăng nhập dạng văn bản 
(Plain-text Password Input): Trường mật 
khẩu  
  
form đăng nhập dùng type="text" làm 
hiển thị rõ toàn bộ ký tự khi gõ, gây lo 
ngại sâu sắc về rủi  
  
ro bảo mật thông tin (P01 phàn nàn).  
  
3. Màu sắc nút Đăng ký vi phạm quy 
chuẩn (Inconsistent CTA Color): Nút 
"Đăng ký" mang  
  
màu đỏ cảnh báo nguy hiểm (btn-danger) 
gây cảm giác hoang mang như nút Hủy 
hoặc Xóa.

4. Bảng xếp hạng Mức độ Nghiêm trọng 
(Severity Ranking — Chuẩn Nielsen  
  
Norman Group)  
  
Toàn bộ khiếm khuyết được xếp hạng 
theo 4 mức độ nghiêm trọng chuẩn quốc 
tế (Nielsen,  
  
1994):  
  
  
  
  Mức độ nghiêm         Mô tả tác động UX        
Số        Vấn đề phát hiện thực tế trên  
  
      trọng                                      lượng                 
EShop  
  
Severity 4          Chặn đứng luồng thao tác     
2      1. Nút Thêm vào giỏ không phản hồi  
  
(Catastrophe /      hoặc phá vỡ hoàn toàn     
lần đầu kết hợp không có  
  
Blocker)            niềm tin bảo mật của              
toast/badge.  
  
                     người dùng.                          2. 
Mật khẩu đăng nhập hiển thị dạng  
  
                                                          văn bản 
thuần (type="text").  
  
Severity 3 (Major   Gây trì hoãn nặng nề,      
4      1. Nhãn form đăng nhập ghi  
  
Usability           khiến người dùng lúng            
"Username" nhưng bắt buộc nhập  
  
Problem)            túng hoặc thao tác sai           
Gmail.  
  
                     hàng loạt.                           2. Logo 
EShop không điều hướng về  
  
                                                          trang chủ 
sau khi tìm kiếm.  
  
                                                          3. Sản 
phẩm trùng nhân bản thành  
  
                                                          nhiều dòng 
trong giỏ hàng.

4. Trang chi 
tiết thiếu hoàn toàn hình  
  
                                                          ảnh và mô 
tả sản phẩm.  
  
Severity 2 (Minor   Gây khó chịu nhưng 
người      3      1. Form đăng ký thiếu 
trường xác  
  
Usability           dùng vẫn có thể tự tìm            
nhận mật khẩu (Confirm Password).  
  
Problem)            cách khắc phục được.            
2. Dòng hướng dẫn mật khẩu chữ quá  
  
                                                          nhỏ và 
tương phản mờ.  
  
                                                          3. Nút Đăng 
ký mang màu đỏ cảnh  
  
                                                          báo (btn-
danger).  
  
Severity 1          Khuyết điểm thị giác          
1      1. Đơn vị tiền tệ hiển thị không  
  
(Cosmetic /         nhỏ, không ảnh hưởng        
đồng nhất (lúc "VND", lúc ký hiệu  
  
Visual Issue)       đến việc hoàn thành             
"₫").  
  
                     nhiệm vụ.  
 
 Dựa trên kết quả thực nghiệm Usability 
Task 2, các lỗi giao diện và trải nghiệm 
người dùng cốt lõi được đồng bộ và cập 
nhật bổ sung vào tài liệu 
GitHub_Issue_Drafts.md để tiến hành 
tạo Issue: 
1. Issue UB-01 (Severity 4): 
[Usability / Security] Password 
input exposes plain text on login 
screen (Checklist: GUI-15, GUI-
25). 
2. Issue UB-02 (Severity 4): 
[Usability / Feedback] "Add to 
Cart" button fails on first click 
and lacks toast notification / cart 
badge update (Checklist: GUI-38, 
GUI-55, GUI-56). 
3. Issue UB-03 (Severity 3): 
[Usability / Logic] Duplicate cart

items create distinct table rows 
instead of incrementing quantity 
(Checklist: GUI-58). 
4. Issue UB-04 (Severity 3): 
[Usability / Form] Ambiguous 
"Username" field label causes 
user input errors (Checklist: GUI-
10, GUI-24). 
5. Issue UB-05 (Severity 2): 
[Usability / Consistency] 
Inconsistent CTA button colors 
and currency units across 
shopping flow (Checklist: GUI-
03, GUI-05). 
5. Kết luận chung về Task 2 
Phiên đánh giá khả dụng với 07 người 
tham gia thực tế (và 01 phiên pilot) đã 
hoàn thành xuất sắc mục tiêu đề ra: 
 
Phơi bày toàn diện các rào cản 
nhận thức và điểm gãy trải 
nghiệm mà kiểm thử tự động 
(Automation) hay kiểm tra tĩnh 
(Static Code Review) không thể 
ghi nhận đầy đủ. 
 
Điểm số SUS trung bình 38.57 / 
100 phản ánh chân thực trạng 
thái chất lượng giao diện hiện tại 
của SUT EShop — một hệ thống 
còn nhiều khiếm khuyết cơ bản 
về phản hồi trạng thái, khả năng 
tiếp cận và tính bảo mật thị giác. 
 
Toàn bộ kết quả định tính (trích 
dẫn think-aloud, quan sát cử chỉ) 
và định lượng (điểm số từng câu 
SUS, thời gian hoàn thành) đã 
cung cấp cơ sở vững chắc cho 
nhóm phát triển thực hiện tái 
thiết kế UX trong các chu kỳ tiếp 
theo. 
  
 
 
 
4. Summary of AI Accuracy 
Aggregate the verdicts from Section 3 and complete the table below. 
Metric 
Count 
Percentage 
Total AI-generated artifacts audited 
4 
 
VALID (correct, accepted as-is) 
1 
33.33% 
INVALID (wrong; rejected) 
0 
0% 
INCOMPLETE (acceptable after edits) 
3 
67.67%

5. Conclusion — When should AI be used (or not)? 
Write 80–150 words describing patterns you observed. Where did AI shine? Where did 
AI fail? What is your recommendation for using AI in this kind of work in the future? 
AI đã thể hiện xuất sắc trong việc nhanh chóng tạo ra các sản phẩm cấu trúc: tạo ra 
danh sách kiểm tra giao diện người dùng (GUI) ban đầu gồm 50 mục gồm cả bốn khía 
cạnh giao diện của hệ thống cần kiểm thử (SUT), AI còn thực hiện rất tốt trong việc 
phân tích mã nguồn, xác định các yêu cầu chức năng, tạo ra các tiêu chí kiểm tra giao 
diện người dùng ban đầu và sắp xếp kết quả đánh giá khả năng sử dụng.. Tuy nhiên, AI 
đã thất bại đáng kể khi phân tích hành vi thời gian thực động và tương tác của người 
dùng. Nó đã bỏ qua các lỗi thời gian thực nghiêm trọng như lỗi nhấp chuột đầu tiên trên 
nút "Thêm vào giỏ hàng", trùng lặp mặt hàng trong giỏ hàng, lộ mật khẩu dạng văn bản 
thuần và nén bố cục trên thiết bị di động. Quan trọng hơn, AI không thể mô phỏng cảm 
xúc, sự nhầm lẫn hoặc những khó khăn về khả năng sử dụng thực tế của con người. 
Trong các quy trình kiểm thử tương lai, AI chỉ nên được sử dụng như một công cụ hỗ 
trợ tạo danh sách kiểm tra, phân tích dữ liệu và soạn thảo báo cáo. Người kiểm thử phải 
xác minh các đề xuất của AI thông qua thử nghiệm thực tế và phản hồi từ người dùng. 
Người kiểm thử phải có trách nhiệm cho kết quả cuối cùng đưa ra. 
 
______________________________________________________________________
________________ 
______________________________________________________________________
____________________ 
______________________________________________________________________
____________________ 
______________________________________________________________________
____________________ 
______________________________________________________________________
____________________ 
______________________________________________________________________
____________________ 
6. Mandatory Disclosure (paste verbatim) 
" The GUI checklist was initially generated by Codex; I reviewed and modified it and 
added 17 manual criteria covering accessibility, mobile responsive layouts, and 
runtime state persistence. I personally conducted the tests, verified the results, and 
determined the final test outcomesThe Task 1 and Task 2 evaluations and report 
content were generated by AI using Codex and Antigravity. The usability sessions, 
participant observations, and responses were conducted and recorded by me, verified 
the checklist results, and wrote the AI Critique myself. The detailed AI Audit Report is

attached as Appendix A. I confirm I did not use AI to generate any artifact listed in the 
prohibited category " 
Signature 
Student name (printed): 
LE MANH PHU 
Student ID: 
23120325 
Class / Cohort: 
CQ K2023 
Course: 
CS423 / CSC13003 – Software Testing 
Instructor: 
HO TUAN THANH 
TRUONG PHUOC LOC 
TRAN THI BICH HANH 
Date: 
15/11/2026 
Signature: 
PHU 
References 
• 
Kharbach, M. (2026). AI Use Policy Templates for Higher Education. CC BY-NC-SA 
4.0. 
• 
ISTQB Foundation Level Syllabus (latest version). 
• 
Hardman, P. (2025). A Post-AI Learning Taxonomy. 
• 
Fuster Rabella, M. (2025). OECD Education Working Paper No. 338. 
• 
Perkins, M., Roe, J., & Furze, L. (2025). AI Assessment Scale. 
• 
Anthropic (2025). Building reliable AI test agents — engineering blog. 
• 
DeepEval & Promptfoo documentation — testing frameworks for LLM systems.