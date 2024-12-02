# Bank System

### Mô tả:
Xử lý các giao dịch ngân hàng, bao gồm việc gửi tiền lương.

- **Thành phần chính:**  
  `BankSystemProxy`, `IBankSystem`, `BankInformation`, `Paycheck`
- **Input:**  
  Paycheck từ Payroll Processing System.
- **Output:**  
  Gửi tiền vào tài khoản ngân hàng (BankInformation).
- **Interface:**  
  `IBankSystem`

### Biểu đồ:
![Bank System Diagram](https://www.planttext.com/api/plantuml/png/l58nRiCm3Dpr2Y9J0xHvWD0X2Bfu2GBa1RJ4988joP2ee4QRbtNea_g5oB63AeNdSg28Ev1t9FJpzRsEZ86JRKM7gi4ZmMA3he5z7vdi0Zu4v32EAHnG4LG3Ev8JDuQcpaV3JntswaIgaR2RgcUeSqlb3bx2Pgg2HJRUBIMSlT6tCHTnUrIBCSAlo2xuznwCxLgov3Z-au5xRo7n0cXzSYpXpQUwfOBGo9JXd0kGicVV4rLQmfw3SSVvFGixZsfA3NBRP6iA3oD6VbXgYvPcgE0JPsIcTL8lZ_ZwkLhzFRYuY3KvFNoBAm000F__0m00)

---

# Timecard Management System

### Mô tả:
Quản lý thời gian làm việc của nhân viên (timecards).

- **Thành phần chính:**  
  `TimecardController`, `Timecard`, `Employee`
- **Input:**  
  Yêu cầu từ nhân viên để nhập hoặc cập nhật thông tin chấm công (Timecard).
- **Output:**  
  Lưu thông tin chấm công vào cơ sở dữ liệu.
- **Interface:**  
  `TimecardController`

### Biểu đồ:
![Timecard Management System Diagram](https://www.planttext.com/api/plantuml/png/T54n3i8m3Dpp2ei9XdwW0we430nC8367rYeHILmbBbA5-Z86diGN26e3hIWU8kjyPv-Tv_sHUPQEQwD59VEBB15c1sKmbww0dRG1C6WPzerdD3Eu2GYHQ-azHDwAB3lI6brVxg94ZemvcafJWvZ2fiyMwKS_qDHL8Ha_CkwJBpV8hgGwIIicp0mi9F1kbi8wl0FmJBNpHt8N37tNL9_qi1gTRaDnpqxPydTMt64qIuq57MYbmGcu8gzOaPqQCN7L95cEZ_M74ts9LcHeY_UdlW000F__0m00)

---

# Project Management Database System

### Mô tả:
Quản lý dữ liệu liên quan đến dự án và mã chấm công (charge codes).

- **Thành phần chính:**  
  `ProjectManagementDatabase`
- **Input:**  
  Truy vấn dữ liệu mã dự án (Charge Codes) và thông tin nhân viên.
- **Output:**  
  Cung cấp dữ liệu liên quan cho hệ thống khác (Timecard hoặc Payroll).
- **Interface:**  
  `ProjectManagementDatabase`

### Biểu đồ:
![Project Management Database System Diagram](https://www.planttext.com/api/plantuml/png/T91D3e9038NtdA9XXGikO0mX0HSccfXmWWeDZZ8pXDO5CPpCXKVo2gBy9zfTs-_blVRrU8OiMCbD5qw9wHLp0lTOsGkb0WSqRQ_92CGeU48cI6eMqYxS7MWhBP0PUdx2HxgZkif9eZDMEKKs8_PMQzWhbaqYbJ9vi0ItkYniJHIJe2hOexxVPMle1AryWBxInfa56ZOpVn_Kg9qD3MhwCIujAr7MB5QznVzhVJ-OGZLEI2Rx_FKD003__mC0)

---

# Payroll Processing System

### Mô tả:
Tính toán và xử lý bảng lương cho nhân viên.

- **Thành phần chính:**  
  `PayrollController`, `Paycheck`, `SystemClock`
- **Input:**  
  Timecard, thông tin nhân viên từ cơ sở dữ liệu.
- **Output:**  
  Bảng lương được xử lý (Paycheck).
- **Interface:**  
  `PayrollController`

### Biểu đồ:
![Payroll Processing System Diagram](https://www.planttext.com/api/plantuml/png/R94nRiCm34LtdOB8b0Br1JmK0TmEtGAa5s1fmWrCIG553KQHatNeaNg5ohK3A4suY13v7p-bdw_lNJ9KorxS2Md4WM6pnqcZ2Emr4gTq30CSfcJiD_3fe0G9fWHhMnU3pIVhMbs2K2WB6fUsBVkJn8cvXPSrUmGxUYRKleMtDNjePoPzC8qLQE30kd3-IdTW_uLdLzbSh7SIQRmoEB1rMPM3pVEtXV5SfjpgB-HAt03wc8CLISplmbMXBuoAj5nU7B-MPG-cvK7hCRVls3HFrmlTRwasSsUtuz3Ft_WB003__mC0)

---

# Print Service

### Mô tả:
Tạo và in báo cáo lương.

- **Thành phần chính:**  
  `PrintService`
- **Input:**  
  Bảng lương (Paycheck) từ Payroll Processing System.
- **Output:**  
  In bảng lương hoặc lưu báo cáo.
- **Interface:**  
  `PrintService`

### Biểu đồ:
![Print Service Diagram](https://www.planttext.com/api/plantuml/png/X90n3i8m34NtdCBg14Cla05rO66hu0GciKhLj8aIjrA5UZ86ZiGLI26WCE71ilwpzMq_RlSgC7eUUoCSgWuRWgBsxS1m8Z-rYWgu2eYX38O0BvH80kzmAwXnLXTItSQbGi97sagORAkpYO0J7SbPpt_Q5v4la1eoynAmj-F04lPsF1lAW4QcACUSYTGxOsUYWvPmuhXtazlyN5YMkw-ZM4H5Wru_zGG00F__0m00)
