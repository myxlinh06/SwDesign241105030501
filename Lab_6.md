# 1. **BankSystem::deposit**
1. **Xác định lớp và thuộc tính**:
   - `BankSystem`: Đại diện hệ thống ngân hàng.
   - `BankTransaction`: Quản lý giao dịch.
   - `Paycheck`: Đại diện bảng lương, chứa số tiền và thông tin nhân viên.
   - `BankInformation`: Thông tin ngân hàng (tên, số định tuyến).

2. **Xác định phương thức (operations)**:
   - `BankSystem.deposit(Paycheck, BankInformation)`
   - `BankTransaction.create(op, amount, routingNum)`
   - `BankTransaction.submit()`
  
  ## Class diagram:
  ![Diagram](https://www.planttext.com/api/plantuml/png/T951Ri8m44NtFiKiGKeka0L2NLHYWoh11IREj8s8FP5dl8WG9sF1aRW22Ks20TNBxpzl_hUlvyjQ58D6rnZRe0Xye3_iEb5oS3HmFnMrBBKklh2plsGFsTsqyTyS76hDVcbE9XdV1_I2ThYP6JOGAYsuBM2deVO_6Q3ZwBM0puPHCmWSjTUtqKsMvJWhiNJz-cJBb6J4vy-iKIFNDjmHRQe9-1mpAJ1pobxVegDvuaz-P2iffBJajV9yzTQ-W2WavbKUh7E50jh0bkG_uslKaRacNms_TWC00F__0m00)

3. **Biểu đồ trạng thái**:
   - Trạng thái của giao dịch từ *Khởi tạo* → *Đang xử lý* → *Hoàn tất*.
     ![Diagram](https://www.planttext.com/api/plantuml/png/T951Ri8m44NtFiKiGKeka0L2NLHYWoh11IREj8s8FP5dl8WG9sF1aRW22Ks20TNBxpzl_hUlvyjQ58D6rnZRe0Xye3_iEb5oS3HmFnMrBBKklh2plsGFsTsqyTyS76hDVcbE9XdV1_I2ThYP6JOGAYsuBM2deVO_6Q3ZwBM0puPHCmWSjTUtqKsMvJWhiNJz-cJBb6J4vy-iKIFNDjmHRQe9-1mpAJ1pobxVegDvuaz-P2iffBJajV9yzTQ-W2WavbKUh7E50jh0bkG_uslKaRacNms_TWC00F__0m00)

---

# 2. **PrintService::print**
1. **Xác định lớp và thuộc tính**:
   - `PrintService`: Quản lý việc in.
   - `PaycheckPrinterImage`: Tạo hình ảnh in từ bảng lương.
   - `PrinterInterface`: Kết nối với máy in.
   - `Employee`: Thông tin nhân viên.

2. **Xác định phương thức (operations)**:
   - `PrintService.print(Paycheck, String)`
   - `PaycheckPrinterImage.buildPrintImage(fromPaycheck)`
## Clas diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/T951Ri8m44NtFiKiGKeka0L2NLHYWoh11IREj8s8FP5dl8WG9sF1aRW22Ks20TNBxpzl_hUlvyjQ58D6rnZRe0Xye3_iEb5oS3HmFnMrBBKklh2plsGFsTsqyTyS76hDVcbE9XdV1_I2ThYP6JOGAYsuBM2deVO_6Q3ZwBM0puPHCmWSjTUtqKsMvJWhiNJz-cJBb6J4vy-iKIFNDjmHRQe9-1mpAJ1pobxVegDvuaz-P2iffBJajV9yzTQ-W2WavbKUh7E50jh0bkG_uslKaRacNms_TWC00F__0m00)
3. **Biểu đồ trạng thái**:
   - Trạng thái in: *Chuẩn bị in* → *Đang in* → *Hoàn thành*.
![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3XUGKPAge1HGb5gGM9IPbwwaa5Yi0E8XP3BpIX0IG0vCnZa_jo0djIGr1Ipbaf-NoiKLhHMheAjh1p41H41vG6qALWh1gNaf2YNv2WKWVceH5qGSf0Aa6wZ0BJClipW38W-qayi1g07aIW00003__mC0)
---

# 3. **ProjectManagementDatabase::getChargeNumbers**
1. **Xác định lớp và thuộc tính**:
   - `ProjectManagementDatabase`: Đại diện hệ thống cơ sở dữ liệu.
   - `ChargeNumList`: Danh sách số tính phí.
   - `ChargeNum`: Đối tượng số tính phí, chứa tên dự án và giá trị.

2. **Xác định phương thức (operations)**:
   - `getChargeNumbers(String)`: Truy vấn danh sách số tính phí.
   - `ChargeNumList.add(theChargeNum)`.
  
    ## Class diagram:
   ![Diagram](https://www.planttext.com/api/plantuml/png/T51B2i8m4Dtd55dQHI_GXHGKGT0YU89fCiHAaafcuaOycGkFv1MiDIrMT9RlEpEFsxqaXi3HMQ4i4CbTQ8-eU0iU33hql0I66WZbHSX-3FBY0C5W5LsDWMQdjsMj2xddq7YJ5N9KR1fYSHKfVGAFYQ3rJ0tCXpVxOKocNARM2XmElOavWuqTjh8jzDN_Jyhp-TTAXGp8CNWIKtoYx5IgzGnD9olHwzVtdW000F__0m00)

4. **Biểu đồ trạng thái**:
   - Trạng thái danh sách số: *Rỗng* → *Đang cập nhật* → *Hoàn tất*.
  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3XUGKPAgeEIQMr1IgQIGMAm0Pi64GmjI4aioyzB1CZ0EJD8vFxSW9xKaDGKi2-TnSKLhnIhewjf1ZGAJO3xC00Kh1SUK58NaZCIYz5I5lDBSfDIYOYwuB4Wft3IWMhVClCpY38LIa7mgbqDgNWh8uG00003__mC0)

---

# 4. **ProjectManagementDatabase::initialize**
1. **Xác định lớp và thuộc tính**:
   - `DBChargeNumbers`: Kết nối cơ sở dữ liệu.
   - `DriverManager`: Quản lý kết nối.

2. **Xác định phương thức (operations)**:
   - `initialize()`: Thiết lập kết nối.
   - `getConnection(url, user, pass)`: Lấy kết nối đến cơ sở dữ liệu.
## Class diagram:
![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niOABatD6Ob5wgbzfRb9gKR52DPS266JcPPPa9kPaLgLgQ7BLSi5K5sMMfHRv9kObfgSMmTMcfvOuv-VbfIQNPERdQPGMvLWf19SKPUQbwoYK5gSM8NW5G3DWFB2fwBRhwjgXsM45CgAOoo4rBmNaQ000003__mC0)
3. **Biểu đồ trạng thái**:
   - Trạng thái kết nối: *Chưa kết nối* → *Đang kết nối* → *Kết nối thành công*.
![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3XUGKPAgeEIIMPoSdvUNcboIcgAaa5YiW2m0K-GC4SZCImShGN3H542DWFEukAArOXLqTUrGJKNcW6KH1YfOAJWdvkGePEPbbcGcvcHMfN8XIIAf1UgqWklBprCeBarEJYqkJYlDuN98pKi1-H00003__mC0)
---
