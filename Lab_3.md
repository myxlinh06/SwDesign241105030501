# 1.Subsystem context diagrams
## BankSystem Subsystem
### Biểu đồ ngữ cảnh:

### Giải thích:
- BankSystem là hệ thống xử lý giao dịch ngân hàng. Nó có nhiệm vụ xử lý các khoản thanh toán của nhân viên thông qua việc gửi lệnh chuyển khoản đến ngân hàng.
- IBankSystem là một interface cho phép hệ thống Payroll giao tiếp với BankSystem, cung cấp phương thức deposit để thực hiện chuyển khoản trực tiếp.
- PayrollController gọi phương thức deposit để xử lý lương cho nhân viên.

## PrintService Subsystem
### Biểu đồ ngữ cảnh:

### Giải thích:
- PrintService là hệ thống xử lý việc in các phiếu lương (checks) cho nhân viên.
- IPrintService là một interface cho phép hệ thống Payroll gọi hàm print để in phiếu lương, sau đó phiếu lương sẽ được gửi đến nhân viên bằng phương thức gửi thư hoặc nhận trực tiếp.
- PayrollController gọi print thông qua IPrintService để thực hiện việc in phiếu lương.

##  ProjectManagementDatabase Subsystem
### Biểu đồ ngữ cảnh:

### Giải thích:
ProjectManagementDatabase là hệ thống xử lý dữ liệu dự án, lưu trữ và quản lý thông tin liên quan đến các dự án mà nhân viên đang làm việc, dùng để tính toán lương cho nhân viên theo dự án (nếu cần).
Hệ thống này cung cấp các phương thức addProjectData, updateProjectData, và deleteProjectData để PayrollController có thể thêm, cập nhật và xóa dữ liệu dự án.
PayrollController tương tác với ProjectManagementDatabase để quản lý dữ liệu dự án của nhân viên khi tính lương hoặc khi cần thiết.

# 2.Analysis class to design element map
| Lớp Phân Tích              | Phần Tử Thiết Kế                         |
|----------------------------|------------------------------------------|
| LoginForm                  | LoginForm                                |
| MaintainTimecardForm       | MainEmployeeForm, TimecardForm, MainApplicationForm |
| TimecardController         | TimecardController                       |
| SystemClockInterface       | SystemClockInterface                     |
| PayrollController          | PayrollController                        |
| Paycheck                   | Paycheck                                 |
| Employee                   | Employee, EmployeeForm, EmployeeController |
| PurchaseOrder              | PurchaseOrder, PurchaseOrderForm, PurchaseOrderController |
| BankSystemInterface        | BankSystemInterface, BankSystemProxy     |
| PrintService               | PrintService, PrintController            |
| ProjectManagementDatabase  | ProjectManagementDatabase, DatabaseController |
| PaycheckCalculator         | PaycheckCalculator, SalaryCalculator     |
| CommissionedEmployee       | CommissionedEmployeeForm, CommissionedEmployeeController |
| EmployeeDatabase           | EmployeeDatabase, DatabaseService        |
| PayrollDatabase            | PayrollDatabase, DatabaseController      |
| PaymentMethod              | PaymentMethod, DirectDeposit, CheckPayment |
| Timecard                   | Timecard, TimecardEntryForm             |
| BankInformation            | BankInformation, BankService             |

# 3.Design element to owning package map
| Design Element            | Owning Package                          |
|---------------------------|-----------------------------------------|
| LoginForm                 | Middleware::Security:GUI Framework      |
| MainEmployeeForm          | Applications::Employee Activities       |
| TimecardForm              | Applications::Employee Activities       |
| MainApplicationForm       | Middleware::Security:GUI Framework      |
| TimecardController        | Applications::Employee Activities       |
| SystemClockInterface      | Applications::Payroll                   |
| PayrollController         | Applications::Payroll                   |
| Paycheck                  | Business Services::Payroll Artifacts    |
| Employee                  | Applications::Employee Activities       |
| PurchaseOrder             | Business Services::Purchase Management  |
| BankSystemInterface       | Business Services::Bank Integration     |
| PrintService              | Business Services::Printing             |
| ProjectManagementDatabase | Infrastructure::Database Management     |
| PaycheckCalculator        | Business Services::Payroll Artifacts    |
| CommissionedEmployee      | Applications::Employee Activities       |
| EmployeeDatabase          | Infrastructure::Database Management     |
| PayrollDatabase           | Infrastructure::Database Management     |
| PaymentMethod             | Business Services::Payment Integration  |
| Timecard                  | Applications::Employee Activities       |
| BankInformation           | Business Services::Bank Integration     |

# 4.Architectural layers and their dependencies
![Diagram](https://www.planttext.com/api/plantuml/png/T5CnJiCm5Drz2giBKw-0gXQGa5eHgMoemyVz9AQE7TaEKeGu0GihOc9WOE806HZeHN82he13Y8eT9qkKzv_VU_hF-Qu_PyQ2jcKkI05i1odIIQBHeBHWkP9q2HNg2Rqdr3rNIvLoUQPqlg4TS9eNGbM8lrW7hO3B27p9SsIWjntqG0v-yz9mYSRGLfq5ZWbKMWcnKDAsRzGRttWmw7q60wV4CcIx1GXM2h1A-p4Ir8ORYv9XaA7tEW4Brs1muqKBKQrkaTaLIAUQkps6yrApp7rUw2q62NfcOD_3QzHtdFKwSv2xTUNovkVIehw1TkBKZkZ-gQaVPKPbcktVWRAlLqQBhAdVgCtAfdvcDELD_V4t4KtzKf3_pKwdnz6z3vljgB4g_BexNgmP4Zljonxs5mdbXVMPOTaZL38qwfY3jG_EZl96hy3e2UzIZB5YbOzmoGpbjlshVm000F__0m00)
