# Create Administrative Report
### 1. Boundary Classes:
- ReportCriteriaForm: Thu thập thông tin tiêu chí báo cáo từ Payroll Administrator.
- ReportView: Hiển thị báo cáo đã được tạo.
- SaveReportDialog: Hộp thoại lưu báo cáo, nơi Payroll Administrator nhập tên và vị trí lưu.
### 2. Entity Classes:</h3>
- Employee: Chứa thông tin nhân viên cần thiết cho báo cáo.
- Report: Chứa dữ liệu của báo cáo đã tạo.
- PayrollData: Chứa dữ liệu bảng lương và giờ làm của nhân viên.
### 3. Controller Classes:
- ReportController: Điều khiển quy trình tạo báo cáo và liên kết các lớp boundary với entity.
- SaveReportController: Xử lý việc lưu báo cáo vào vị trí được xác định bởi Payroll Administrator.
### 4. Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V99DJiCm48NtFiLSe1Vm0ZKY1I4X6b69_P1Cq4Z-YHodA6TZmP6u0ZPEegGrpIAItxnldktnpzVtllVe_A2LmDfR1nMEpYfLD9eDzzvX5B67gX2YAc1t1w_KMUVl7NjoZ0_MQGa74nPJ1UQIk7QkU6jy328duJIyQxxc5aUafdsLw5665jundMbM8SfYPO5TDYXmWpDRAXTsq9so8z4gQPRWoRHMBAkRELic5vGq2OzaA5mrJSBalTrzPfejb0juO_gKK7BVAHndkq3buOJd9HJ2bqOSrIIMZCf-I3XsP98vAN_cIziMtKouevhRCNLujZLwjWRGDF22cYwQvQzejTCqkF-Xx0c2eUNm0cD5a6c4s8T_VFY_0000__y30000)_
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V95D2i8m48NtEKNetYj8CQrhKN0_j4C9facPJ9KYdio5H_8ADWeQRMfsUTzZtlpShxVSCn3thH4TL0TeK6OhrziQQ93AWFVeCtaMSdnL-CejTevOaMOa3Mj7xGJkDPuYSGT7V852Wt6Dk8XFM6bPyqnKsNR63OYJW4ZOm43Ec08OlkegPpa0fBzZl5t9VYCyrlxLv6APsiQyxRcNUPn4yNofne9dik0SRHrE-W000F__0m00)

# Create Employee Report
### 1. Boundary Classes:
- ReportCriteriaForm: Thu thập thông tin yêu cầu báo cáo từ nhân viên.
- ReportView: Hiển thị báo cáo cho nhân viên sau khi đã được tạo.
- SaveReportDialog: Thu thập tên và vị trí lưu báo cáo từ nhân viên nếu họ chọn lưu.
### 2. Entity Classes:
- EmployeeData: Chứa dữ liệu về nhân viên, bao gồm số giờ làm việc, ngày nghỉ phép, và thông tin lương.
- ProjectDatabase: Chứa thông tin mã công việc phục vụ cho báo cáo "Total Hours Worked for a Project."
- Report: Lưu trữ báo cáo đã được tạo và có thể lưu trữ lại nếu được yêu cầu.
### 3. Controller Classes:
- ReportController: Điều khiển quy trình tạo báo cáo dựa trên các tiêu chí được cung cấp.
- SaveReportController: Xử lý việc lưu báo cáo nếu nhân viên chọn lưu báo cáo.
### 4. Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V5FBJiCm4BpxA_O8X_w03wWI2GY9GaKbxfjaWumSst8sHVas3dmIlu1D7gIfgG-MF3ipEx4ttvzVsvRHSzTeWILR3tdZjEs905l8TtiXmWQR6tWXPptVUiNa5TvPtqZ8JJYC5PXAufovq5l3tcfDNiAXAnfrhfiPKJMboP1H1W_sYexq5pBYOac2JR9NK7RUh7IfXdjltwdaM2-mfKNFiG8FfhPmfMf0vxGgiT1qBLQooocMJiaG0oRXdWnvP1g1aNlPVD9Kfw9KWrT57n8orJgD_VICRETR4W8rmm6FSm08Qvo720zefb3RDmdFZip07f1VzffsAZqP1qUbgll1uT6MoCeQG5F14pQqCalVroBgyCB_Yv9V40Yr2kCQAu9C9SGsxF7V-0400F__0m00)
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V57B3e8m4BptAnhk_e8X0fwD9jvNs91gQSbsqH3Zbtdma_m5gIRAezXRPoOxExFF-oDs3CHDfKKD-GbAbD7ADgO0QcMYmJbqaRmAsRtSV-KMQqkSa68a1MjBrOJSAxpqm1sSyKEa2hGjnKtyp3B3YcUiighMjaLCWQ47RyWUCMUF7i3Xn7umFx66oMgDz3VELnNSkqTtiyUON2n3hSpBtls4w47Wa60SFRIYrqqgZz4K_iWl0000__y30000)

# Login
### 1. Boundary Classes:
- LoginForm: Giao diện nhập thông tin đăng nhập
   - Các trường nhập: username, password
- LoginErrorDialog: Dialog hiển thị thông báo lỗi
### 2. Entity Classes:
- UserAccount: Lưu trữ thông tin tài khoản người dùng
   - Username
   - Password (đã mã hóa)
   - Role/Permission
   - AccountStatus
- UserSession: Quản lý phiên đăng nhập
   - SessionID
   - LoginTime
   - LastAccessTime
   - SessionStatus
### 3. Controller Classes:
- LoginController: Điều khiển quá trình đăng nhập
   - verifyCredentials(): Kiểm tra thông tin đăng nhập
   - createUserSession(): Tạo phiên đăng nhập mới
   - handleLoginError(): Xử lý các trường hợp lỗi
   - logLoginAttempt(): Ghi log đăng nhập
- AuthenticationManager: Quản lý xác thực
   - validateUser(): Xác thực người dùng
   - hashPassword(): Mã hóa mật khẩu
   - checkAccountStatus(): Kiểm tra trạng thái tài khoản
### 4. Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/d59BJiGm3Dtd55x2OYxG1PfgEiE6GOWH1p2fAP7I13aE8yx6WYDn1PAsL5MLOK4NaVhizx7bxy-lRH1aYRrLgCKpF0LYfV8Bcnkuyvrn1yzz1NidD9OTzWJeMdZ04CwUMpMtpPoTTyBUMk8AJl6vDpBYqA2WMhLaLXtbbPmOZMAyEwB3BdCNC5qDgJHJcn6quLefjBAY9ZkjAOINQ1MahoYS7RDQhRMFJYfu9653xmGJ0Wq96Xi6YKKdR2vdJHgHNL7XGeZIjihJ32g5jULefrHFhHNicDAQu9xEC65p_Ec_RFbR7Fdj9Q_5CTmofWdhCHhPGElOXpJwfFJ_sRD8PFeppvxPSvEkmNSLD2QyMVo00OHZ2fUy5BbMgMrwyvN_0000__y30000)
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V94n3i8m34Ntd2BgpXLGIoaJJAW7iDAeHAGnijq18Kx6m96u0kbGDLGjtcn_F_lBdzSxPm6IllFg1kOAhTNP3llG0DrrwO7PSgOVIiSmGwgFsBfmGEhcjOe8QU_0OwkUQi9LGPoim6gsL1WJ5ygiUhRC3iCFgSGWXDvR-dFQ94ewHIyN6-ym815wWX1vDB1d8tgpJGokDLEd2vhKrEBYKJHwp6reXWzy0G00__y30000)

# Maintain Employee Information
### 1. Boundary Classes:
- EmployeeMaintenanceUI: Giao diện chính quản lý nhân viên
- EmployeeFormView: Form chi tiết nhân viên
- DeleteConfirmDialog: Dialog xác nhận xóa
### 2. Entity Classes:
- Employee: Lưu trữ thông tin nhân viên
   - employeeId
   - personalInfo 
   - employmentType 
   - paymentInfo 
   - deductions 
   - status (active/deleted)
- PayrollSettings: Quản lý cấu hình lương
   - paymentMethods
### 3. Controller Classes:
- EmployeeMaintenanceController: Điều khiển chức năng quản lý
   - addEmployee(): Thêm nhân viên mới
   - updateEmployee(): Cập nhật thông tin
   - deleteEmployee(): Đánh dấu xóa nhân viên
   - generateEmployeeId(): Tạo mã nhân viên mới
- EmployeeValidator: Kiểm tra tính hợp lệ
   - validatePersonalInfo(): Kiểm tra thông tin cá nhân
   - validatePayrollInfo(): Kiểm tra thông tin lương
### 4.Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/d5L1Ri8m4Bpx5Vu0uXuf5LKJ92HG9H3SLydIMdBio7P0lAs7FgbVw8O0SKDCKd99v5tFZcT6pi_NzymwCAug98FCQSDVyq8eniulFddXQL5AVK9SWL0E5QWCjuk8xmGURpM-5DQntiu0n9jMpcWfqKHygI5leH9mq0VLxl0X8xv6PmGUC426JuO944HbrF1fV0fXPH9XImcd3XoBOv8sdwQvS6rfeVRQ5E24LZoE1qNVeCJCtUCCIp-dCRLb4NylqJjglNu_jkrE2Svuvg038IthDlgRTo153XGb2adpYG5tRvr_v6o7N-grE6kqbIGLGJf_ULDb6LhBE3sFE0MCty2Xoyr76f6-RLcVRqgEFC0Paq7wtWjJU81Zg8IZqk1qGeZIeY_VdCoi3Fv7FZ_X7b9gZ3QMeShFIKyegFxqvtBUGGcdl6cyI9W8aFg3G3xryIfhCxcfjDDxjrsDQ8gifsT4i4Om3zzdXRvBvJD9EdEWOpz_a_LcYCt8vFftyGi00F__0m00)
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/Z5512i903BplAnRlVa6ARGKFWY3s7jfO5jDisKsH8hxCWq_o2tOljiMgpIsPJ2QPFE-Fo0iuQIfIDUHdA54lrhRX0bohOmBlqI_qLUakyf3gjAh9jeWxC2p8m3aUjnFunhegCtWPG0aI2iQMJyPLYG6ofRgfNZXbCV97Tb3QG-iiqG5539T-DAeJaG2Yctr5Jvdeou1C0M9TKFb9rilL5uzcqzxMpMQeZpr7Q8HSX1U_0000__y30000)

# Maintain Purchase Order
### 1. Boundary Classes:
- PurchaseOrderMainUI: Giao diện chính quản lý đơn hàng
- PurchaseOrderFormView: Form chi tiết đơn hàng
- DeletePOConfirmDialog: Dialog xác nhận xóa
### 2. Entity Classes:
- PurchaseOrder: Lưu trữ thông tin đơn hàng
   - orderID
   - customerInfo (contact, billing address)
   - products
   - orderDate
   - status (open/closed)
   - commissionedEmployeeID
- Customer: Thông tin khách hàng
   - customerID
   - contactInfo
   - billingAddress
- Product: Thông tin sản phẩm
   - productID
   - name
   - price
   - quantity
### 3. Controller Classes:
- PurchaseOrderController: Xử lý nghiệp vụ đơn hàng
- POValidator: Kiểm tra tính hợp lệ
- POAccessController: Kiểm soát quyền truy cập
### 4. Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/p5RDRi8m3BxdAV82q-v8J4EKJPCsWK1mpngpHaiRvAHCFDiEUwIzmbnIklwbm4xZW22sltosFxlz_lowjqwWorFDHEmCyhK5PApuvZTtV95Zd0WBSvI0Bq9bwwSHtoZug2pyQEBFoZhMuzq1cPhCeT4QSCIVZP0j8Ci2tXsW4L-2GmLxEC-5tmpH89mSis1mdKEe996oEoqETGms7lE9bBSpgLoRuNWyNE4LQ8XTA3nOv_aaZi7QUcxJ1E9txi_vKhqbZYhSyGidLaO-eiWSo8iw_60mBIGoulCTPEtK2sj_yhznCxeBI_y8d52w9OkJgyzw8xIIWiHBqlG_JvT5mWbMS-Zc-NjfwQHCHeAmkQOE2ktgnwlyM0p6wHEc4rBPIkmRj3eeJQrFS-jCMWHk0DNsK1rK5Ia0giD1WRT3EHct2bDgw1aM2pGoZrr5elpF9tl24QzAAtVm6ALXa4TVz1LScjDV3CTwrsvs1-DCPVpbt0FT4kOmYz2OB66BO9Fw_8CcpTVKyq0vvmXNgAUzN6fWCqH3kn8oUTmp4UqBrzc35swPtk3_jsCypSMyR5caX3Plb4HYFavjzBNnbYhrGDofyqSpXR5Uly69lg1mPvvVgMdkX3yej-9_jMORm-CVMVSagE9Lu0S00F__0m00)
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/Z58n3i8m3DppYgWxNq250X83QXUwMuc1Y3H1ZYE442zZu4byWR902grKRxuxtrcMd_T77XY8OsF52TGHzYYpkOzE0rraOI4439cy2jcMUhUoYgGE4B0aZRG1uxRh8NRbgQaDdXD-WHOPgxBmRcUeMHYmVYzkufk-T6nuJ7Q25p6mRpfGHLv7nHthDfJ9MuiqmluhJXLb3TPeODz5PqfX2Cb86plW9YVJtXkEbN-EEdP094ltaR-x_sjoTFhz8Iy0003__mC0)

# Run Payroll
### 1. Boundaries:
- PayrollSystemUI: Giao diện người dùng
- BankSystemInterface: Giao tiếp với hệ thống ngân hàng
- EmployeeDAO: Truy cập dữ liệu
- PaycheckPrinter: In ấn séc
### 2. Entities:
- Chứa các lớp dữ liệu cốt lõi: Employee, TimeCard, PurchaseOrder, Paycheck
### 3. Controllers (Điều khiển):
- PayrollController: Xử lý logic chạy payroll chính
- TimeCardController: Quản lý thẻ chấm công
- PurchaseOrderController: Quản lý đơn hàng
### 4. Biểu đồ:
- SD diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/Z5H1Rjim4Bpp5Nji3_c000T9h3RmAOBJzBwXrZKHYXB8LG2_BOSygLyeAL4oROb5JgB8dTcTuNB_VdpUEKRBVQC5IcujL7YohTRtTQEC4EaVtDnEfyydnzIyx0hO6SKAcQOJsFT6N4Kbm6rhE7p95l0S4i-uohQId1DYivdMy4ir15kqjOFDHYme0cy82H4fyPxOAdedG5F3RzIg3WMUoSGI5AX-D9rkJqJb_LC1FudbSTvAmKaOtEGhwAqvew14njMqwzPCHTVN5C6TBMhPw-ZveF6H3Dcu8Oyat_9-NOYSZPfr3ack5QuK60LUubOJLhsLHtJqP6koASNey9uqlQFXEGw6G0VVr06mwxII-AhfkyZmB58agYufeIH6fTqbqoWmLsEK6V63nbmPEP-Yl9HYrQPuSqLolUjNAwPLBkS4gMVCkNTAvRmvh_sNUkK1pTluXdU6oHvGad-rvAigbIN9tj6kTOf7-fNeN8KX5Fp6GTa6MRNc_vvKLWN60eO5LCUJyrsXLoo9aRcymx4oVtnktxZaBHeVLFoRPr7EaCNqytPssZ_22HYPlA8mtRXtor5ufXc6Qd4z0DFQxhpNOJB_0m00__y30000)
- Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/V51B3e8m4Dtt58qdGP05AqZK0qpQKGZza6bPD8QJkV18Na4QOoWHdTtCctcVUTuVcVD0VjIA3I1wk2BVvNOq4YZmGe5pw7RynlXS8hQyWK1MgMDm7lMvIf0SJFyULyOZNK1WWfPwK3OW7lRrcasqAFg6kdZ39hRuA8tl_0yN7xPaTEeq5a0oPHz9jE2m9ZbpVwkkv0fhV4o6z3VuihQXlGckN2GR4ylGoFZw5m000F__0m00)




