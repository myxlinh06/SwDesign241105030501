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
### 4. Biểu đồ tuần tự:
![Diagram](

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

# Login
### 1. Boundary Classes:
- LoginForm: Giao diện nhập thông tin đăng nhập
- LoginErrorDialog: Dialog hiển thị thông báo lỗi
### 2. Entity Classes:
- UserAccount: Lưu trữ thông tin tài khoản người dùng
- UserSession: Quản lý phiên đăng nhập
### 3. Controller Classes:
- LoginController: Điều khiển quá trình đăng nhập
- AuthenticationManager: Quản lý xác thực

# Maintain Employee Information
### 1. Boundary Classes:
- EmployeeMaintenanceUI: Giao diện chính quản lý nhân viên
- EmployeeFormView: Form chi tiết nhân viên
- DeleteConfirmDialog: Dialog xác nhận xóa
### 2. Entity Classes:
- Employee: Lưu trữ thông tin nhân viên
- PayrollSettings: Quản lý cấu hình lương
### 3. Controller Classes:
- EmployeeMaintenanceController: Điều khiển chức năng quản lý
- EmployeeValidator: Kiểm tra tính hợp lệ

# Maintain Purchase Order
1. Boundary Classes:
PurchaseOrderMainUI: Giao diện chính quản lý đơn hàng
PurchaseOrderFormView: Form chi tiết đơn hàng
DeletePOConfirmDialog: Dialog xác nhận xóa
2. Entity Classes:
PurchaseOrder: Lưu trữ thông tin đơn hàng
Customer: Thông tin khách hàng
Product: Thông tin sản phẩm
3. Controller Classes:
PurchaseOrderController: Xử lý nghiệp vụ đơn hàng
POValidator: Kiểm tra tính hợp lệ
POAccessController: Kiểm soát quyền truy cập

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


