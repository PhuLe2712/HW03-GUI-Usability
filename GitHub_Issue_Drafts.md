# GitHub Issue Drafts

Prepared from the current 67-ID checklist. The 37 unique failed checklist IDs are grouped into 30 distinct bug reports. Screenshot paths below refer to local evidence files; screenshots have not been uploaded or attached to GitHub issues.

## 1. [GUI-01, GUI-10, GUI-24] Login form uses English and unclear labels

**Checklist IDs:** GUI-01, GUI-10, GUI-24  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-01:** Màn hình Login còn dùng Username và Sign In bằng tiếng Anh.
- **GUI-10:** Tên trường đăng nhập hiển thị Username, không nói rõ đây là email.
- **GUI-24:** Form Login ghi Username thay vì Email.

### Expected

- Nhãn, nút, thông báo và hướng dẫn dùng tiếng Việt rõ ràng
- Người dùng hiểu trường cần họ tên, email, mật khẩu hay từ khóa tìm kiếm
- Nhãn thể hiện đúng loại thông tin cần nhập

### Local evidence files

- `evidence/chrome_desktop/login.png`
- `evidence/firefox_desktop/firefox-login.png`
- `evidence/chrome_android_emulated/android-login.png`

## 2. [GUI-02] Page heading hierarchy is missing or duplicated

**Checklist IDs:** GUI-02  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-02:** Home có 2 H1; Register/Login/Cart không có H1.

### Expected

- Một H1 duy nhất, tên trang chính xác

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/chrome_desktop/register.png`
- `evidence/chrome_desktop/login.png`
- `evidence/chrome_desktop/cart.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`

## 3. [GUI-03] Primary action colors are inconsistent

**Checklist IDs:** GUI-03  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-03:** Nút Đăng ký màu đỏ và Thêm vào giỏ ở chi tiết màu xanh lá, lệch quy ước nút chính màu xanh.

### Expected

- Nút hành động chính màu xanh theo đặc tả và chữ đọc rõ

### Local evidence files

- `evidence/chrome_desktop/register.png`
- `evidence/chrome_desktop/product.png`
- `evidence/firefox_desktop/firefox-register.png`
- `evidence/chrome_android_emulated/android-register.png`

## 4. [GUI-05] Currency formatting varies across product views

**Checklist IDs:** GUI-05  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-05:** Danh sách dùng VND trong khi chi tiết và giỏ dùng ₫.

### Expected

- Giá không trộn VND với ₫; định dạng số dễ đọc

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/chrome_desktop/product.png`
- `evidence/chrome_desktop/cart-populated.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`

## 5. [GUI-11] Product count text does not meet contrast target

**Checklist IDs:** GUI-11  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-11:** Chữ xám trên nền trắng ở dòng số sản phẩm có tương phản khoảng 2.54:1, thấp hơn 4.5:1 cho chữ thường.

### Expected

- Nội dung chính vẫn đọc được trên nền và trạng thái tương tác

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`

## 6. [GUI-12] Product card images have empty alternative text

**Checklist IDs:** GUI-12  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-12:** Ảnh card sản phẩm có alt rỗng.

### Expected

- Ảnh sản phẩm có alt mô tả; ảnh trang trí được xử lý phù hợp

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`

## 7. [GUI-14] Required fields are not marked

**Checklist IDs:** GUI-14  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-14:** Nhãn các trường bắt buộc không có dấu *.

### Expected

- Mỗi trường bắt buộc được nhận biết trước khi gửi form

### Local evidence files

- `evidence/chrome_desktop/register.png`
- `evidence/firefox_desktop/firefox-register.png`
- `evidence/chrome_android_emulated/android-register.png`

## 8. [GUI-15] Form labels are not associated with their inputs

**Checklist IDs:** GUI-15  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-15:** Label không được liên kết với input; input.labels rỗng.

### Expected

- Chọn nhãn đưa focus tới trường tương ứng; tên truy cập mô tả đúng

### Local evidence files

- `evidence/chrome_desktop/register.png`
- `evidence/chrome_desktop/login.png`
- `evidence/firefox_desktop/firefox-register.png`
- `evidence/chrome_android_emulated/android-register.png`

## 9. [GUI-17, GUI-18] Registration email field accepts invalid formats

**Checklist IDs:** GUI-17, GUI-18  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-17:** Email ở Register dùng type=text; kiểm tra typeMismatch của email sai định dạng là false.
- **GUI-18:** Email sai định dạng không bị trình duyệt phát hiện trước khi gửi (input type=text, validity.typeMismatch=false).

### Expected

- Trình duyệt nhận biết email; Android có thể hiện bàn phím email phù hợp
- Người dùng biết cách sửa email trước khi tiếp tục

### Local evidence files

- `evidence/chrome_desktop/register.png`
- `evidence/firefox_desktop/firefox-register.png`
- `evidence/chrome_android_emulated/android-register.png`
- `evidence/chrome_desktop/register-invalid-email.png`
- `evidence/firefox_desktop/firefox-register-invalid-email.png`
- `evidence/chrome_android_emulated/android-register-invalid-email.png`

## 10. [GUI-20, GUI-25] Login password is displayed as plain text

**Checklist IDs:** GUI-20, GUI-25  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-20:** Mật khẩu Login dùng type=text.
- **GUI-25:** Mật khẩu Login dùng type=text.

### Expected

- Ký tự mật khẩu không hiển thị dạng văn bản thường
- Mật khẩu không lộ khi gõ hoặc khi xem lại form

### Local evidence files

- `evidence/chrome_desktop/login.png`
- `evidence/firefox_desktop/firefox-login.png`
- `evidence/chrome_android_emulated/android-login.png`

## 11. [GUI-23] Registration form has no password confirmation field

**Checklist IDs:** GUI-23  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-23:** Register không có trường xác nhận mật khẩu.

### Expected

- Hai trường được đối chiếu trước khi tạo tài khoản

### Local evidence files

- `evidence/chrome_desktop/register.png`
- `evidence/firefox_desktop/firefox-register.png`
- `evidence/chrome_android_emulated/android-register.png`

## 12. [GUI-27, GUI-32] Login error appears below the submit button

**Checklist IDs:** GUI-27, GUI-32  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-27:** Thông báo sai đăng nhập được render dưới form, sau nút gửi.
- **GUI-32:** Lỗi đăng nhập xuất hiện dưới form thay vì phía trên nút submit.

### Expected

- Lỗi rõ ràng, không chỉ dựa vào màu sắc
- Lỗi ở đúng vị trí quy định và không bị khuất

### Local evidence files

- `evidence/chrome_desktop/login-error.png`
- `evidence/firefox_desktop/firefox-login-error.png`
- `evidence/chrome_android_emulated/android-login-error.png`

## 13. [GUI-28] Product search field has no accessible name

**Checklist IDs:** GUI-28  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-28:** Ô tìm kiếm không có label, aria-label hoặc tên truy cập.

### Expected

- Trình đọc màn hình nhận ra nhãn và biết đây là tìm kiếm sản phẩm

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`

## 14. [GUI-30] Product quantity field does not enforce a positive integer

**Checklist IDs:** GUI-30  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-30:** Trường số lượng không đặt min=1; thuộc tính min và step rỗng.

### Expected

- Giá trị 0, âm, thập phân hoặc không phải số bị chặn hay báo lỗi

### Local evidence files

- `evidence/chrome_desktop/product.png`
- `evidence/firefox_desktop/firefox-product.png`
- `evidence/chrome_android_emulated/android-product.png`

## 15. [GUI-38, GUI-57] Cart state has no persistent header confirmation

**Checklist IDs:** GUI-38, GUI-57  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-38:** Header không có badge số lượng giỏ hàng.
- **GUI-57:** Sau 2 giây thông báo trên nút biến mất; header không có badge để xác nhận trạng thái giỏ.

### Expected

- Sau thao tác thêm, số hiển thị cập nhật và dễ nhận biết
- Phản hồi tồn tại đủ lâu và badge/giỏ xác nhận trạng thái

### Local evidence files

- `evidence/chrome_desktop/home.png`
- `evidence/firefox_desktop/firefox-home.png`
- `evidence/chrome_android_emulated/android-home.png`
- `evidence/chrome_desktop/product-after-toast.png`
- `evidence/chrome_desktop/cart-populated.png`
- `evidence/firefox_desktop/firefox-product-after-toast.png`
- `evidence/chrome_android_emulated/android-product-after-toast.png`

## 16. [GUI-40] Product and cart pages have no breadcrumb navigation

**Checklist IDs:** GUI-40  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-40:** Không có breadcrumb tại chi tiết sản phẩm và giỏ hàng.

### Expected

- Breadcrumb thể hiện vị trí và cho phép quay lại trang cha

### Local evidence files

- `evidence/chrome_desktop/product.png`
- `evidence/chrome_desktop/cart.png`
- `evidence/firefox_desktop/firefox-product.png`
- `evidence/chrome_android_emulated/android-product.png`

## 17. [GUI-42] Mobile touch targets are smaller than 44 px

**Checklist IDs:** GUI-42  
**Affected environments:** Chrome Android emulation

### Observed

- **GUI-42:** Android Pixel 7 emulation đo vùng chạm: header link cao 24 px, link card 36 px; nhỏ hơn 44 px.

### Expected

- Có thể thao tác bằng ngón tay mà ít bấm nhầm

### Local evidence files

- `evidence/chrome_android_emulated/android-home.png`

## 18. [GUI-45] Product listing has no loading indicator

**Checklist IDs:** GUI-45  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-45:** Trong lúc API sản phẩm đang chờ, vùng nội dung chỉ có tiêu đề và tìm kiếm, không có loading indicator.

### Expected

- Không để người dùng tưởng trang bị treo

### Local evidence files

- `evidence/chrome_desktop/home-loading.png`
- `evidence/firefox_desktop/firefox-home-loading.png`
- `evidence/chrome_android_emulated/android-home-loading.png`

## 19. [GUI-46] Empty product search has no helpful empty state

**Checklist IDs:** GUI-46  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-46:** Tìm kiếm trả về 0 sản phẩm chỉ hiện từ khóa, không có empty state hoặc hướng xử lý.

### Expected

- Thông báo rõ không có kết quả và gợi ý đổi từ khóa

### Local evidence files

- `evidence/chrome_desktop/home-empty.png`
- `evidence/firefox_desktop/firefox-home-empty.png`
- `evidence/chrome_android_emulated/android-home-empty.png`

## 20. [GUI-47] Product loading error exposes raw server text without recovery

**Checklist IDs:** GUI-47  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-47:** Lỗi API hiện nguyên chuỗi server error, không có hướng thử lại/tiếp tục.

### Expected

- Người dùng nhận biết vấn đề và có cách thử lại hoặc tiếp tục

### Local evidence files

- `evidence/chrome_desktop/home-error.png`
- `evidence/firefox_desktop/firefox-home-error.png`
- `evidence/chrome_android_emulated/android-home-error.png`

## 21. [GUI-48] Registration submit has no processing state

**Checklist IDs:** GUI-48  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-48:** Trong lúc gửi đăng ký, nút giữ nguyên Đăng Ký, không có trạng thái đang xử lý.

### Expected

- Trạng thái gửi hoặc phản hồi thành công/lỗi xuất hiện kịp thời

### Local evidence files

- `evidence/chrome_desktop/register-invalid-email.png`
- `evidence/firefox_desktop/firefox-register-invalid-email.png`
- `evidence/chrome_android_emulated/android-register-invalid-email.png`

## 22. [GUI-51] Search query is interpreted as HTML

**Checklist IDs:** GUI-51  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-51:** Từ khóa <b id="xss-probe">probe</b> được diễn giải thành phần tử HTML.

### Expected

- Từ khóa không được diễn giải thành HTML hoặc làm hỏng bố cục

### Local evidence files

- `evidence/chrome_desktop/search-html.png`
- `evidence/firefox_desktop/firefox-search-html.png`
- `evidence/chrome_android_emulated/android-search-html.png`

## 23. [GUI-54] Missing product leaves detail page stuck loading

**Checklist IDs:** GUI-54  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-54:** ID sản phẩm không tồn tại trả 404 nhưng trang giữ Đang tải... mà không báo lỗi.

### Expected

- Không để người dùng gặp trang trắng hoặc trạng thái treo

### Local evidence files

- `evidence/chrome_desktop/product-notfound.png`
- `evidence/firefox_desktop/firefox-product-notfound.png`
- `evidence/chrome_android_emulated/android-product-notfound.png`

    ## 24. [GUI-55, GUI-56] First add-to-cart click has no effect or explanation

    **Checklist IDs:** GUI-55, GUI-56  
    **Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

    ### Observed

    - **GUI-55:** Thêm vào giỏ ở chi tiết không thêm sản phẩm ở lần nhấn đầu.
    - **GUI-56:** Lần nhấn đầu không có phản hồi hay hướng dẫn cần nhấn lại.

    ### Expected

    - Thông báo toast hoặc badge giỏ được cập nhật ngay sau thao tác
    - Không tạo hành vi nhấn lặp không được giải thích

### Local evidence files

- `evidence/chrome_desktop/product-first-add.png`
- `evidence/firefox_desktop/firefox-product-first-add.png`
- `evidence/chrome_android_emulated/android-product-first-add.png`

## 25. [GUI-58] Empty cart has no illustrative empty state

**Checklist IDs:** GUI-58  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-58:** Giỏ trống chỉ có tiêu đề và link; không có hình/icon minh họa.

### Expected

- Empty state thân thiện và có hướng đi tiếp

### Local evidence files

- `evidence/chrome_desktop/cart.png`
- `evidence/firefox_desktop/firefox-cart.png`
- `evidence/chrome_android_emulated/android-cart.png`

## 26. [GUI-60] Cart total label does not match the required wording

**Checklist IDs:** GUI-60  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-60:** Nhãn tổng tiền là Tổng tạm tính, không phải Tổng cộng.

### Expected

- Nhãn, định dạng và đơn vị thống nhất theo đặc tả

### Local evidence files

- `evidence/chrome_desktop/cart-populated.png`
- `evidence/firefox_desktop/firefox-cart-populated.png`
- `evidence/chrome_android_emulated/android-cart-populated.png`

## 27. [GUI-61] Cart item is deleted without confirmation

**Checklist IDs:** GUI-61  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-61:** Nút Xóa xóa dòng ngay, không yêu cầu xác nhận.

### Expected

- Dialog nêu hành động và cho phép hủy hoặc xác nhận

### Local evidence files

- `evidence/chrome_desktop/cart-populated.png`
- `evidence/firefox_desktop/firefox-cart-populated.png`
- `evidence/chrome_android_emulated/android-cart-populated.png`

## 28. [GUI-63] Adding the same product creates duplicate cart rows

**Checklist IDs:** GUI-63  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-63:** Thêm cùng sản phẩm hai lần tạo hai dòng riêng (2 rows).

### Expected

- Không tạo dòng trùng lặp cho cùng sản phẩm

### Local evidence files

- `evidence/chrome_desktop/cart-duplicates.png`
- `evidence/firefox_desktop/firefox-cart-duplicates.png`
- `evidence/chrome_android_emulated/android-cart-duplicates.png`

## 29. [GUI-64] Cart contents are lost after page reload

**Checklist IDs:** GUI-64  
**Affected environments:** Chrome Desktop, Firefox Desktop, Chrome Android emulation

### Observed

- **GUI-64:** Tải lại trang làm giỏ đang có sản phẩm trở về trạng thái trống.

### Expected

- Giá trị giỏ không mất hoặc lệch bất ngờ trong cùng phiên

### Local evidence files

- `evidence/chrome_desktop/cart-after-reload.png`
- `evidence/firefox_desktop/firefox-cart-after-reload.png`
- `evidence/chrome_android_emulated/android-cart-after-reload.png`

## 30. [GUI-67] Cart layout is difficult to use on narrow screens

**Checklist IDs:** GUI-67  
**Affected environments:** Chrome Android emulation

### Observed

- **GUI-67:** Bảng giỏ không tràn ngang nhưng các cột bị ép hẹp, chữ xuống nhiều dòng và nút thanh toán thành 4 dòng, khó thao tác.

### Expected

- Cột/nội dung không bị ép nhỏ đến mức không dùng được; có bố cục thay thế phù hợp

### Local evidence files

- `evidence/chrome_android_emulated/android-cart-populated.png`
