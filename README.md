# [![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel) SALE ANALYSIS EXCEL DASHBOARD 

---
## 📁 Dữ liệu

File dữ liệu thô gồm 2 Sheet:

+ **Sheet Data** bao gồm:
    - Mã SP
    - Sản Phẩm
    - Danh Mục
    - Đơn Vị
    - Giá Mua
    - Giá Bán
+ **Sheet Sale** bao gồm:
    - Mã SP
    - Số Lượng
    - Hình Thức
    - Bán	Thanh Toán
    - % Giảm Giá
+ Tạo thêm 2 Sheet mới:
    - **Sheet Calculate** bao gồm các phần tính toán, chủ yếu là các phần Pivot Table.
    - **Sheet Dashboard** để trực quan hóa các biểu đồ báo cáo dạng động. 

---

## ⚙️ Các bước thực hiện 

### 1. Chuẩn bị dữ liệu
- Lấy các cột: _Sản Phẩm, Danh Mục, Đơn Vị, Giá Mua, Giá Bán_ ở sheet **Data** sang sheet **Sale** bằng hàm **VLOOKUP**.
- Tạo thêm các cột mới:
  + **Tiền mua** = Số Lượng * Tiền Mua
  + **Tiền bán** = Số Lượng * Tiền Bán * (100% - Giảm Giá)
  + **Day** = DAY(Ngày)
  + **Month** = TEXT(Ngày, "mmm"), cột tháng sẽ hiển thị dưới dạng 3 chữ cái đầu trong Tiếng Anh. 
  + **Year** = YEAR(Ngày)
- Tạo thêm 2 sheet: **Calculate**(chứa các phần tính toán) và **Dashboard**(vẽ biểu đồ và dashboard hoàn chỉnh).
### 2. Tính toán các chỉ số cần thiết và phân tích 
Ở sheet Calculate, tạo các hàm tính toán các chỉ số cần thiết phục vụ cho phần vẽ biểu đồ ở bước tiếp theo ở sheet Dashboard. 
### 3. Vẽ biểu đồ và tạo Dashboard hoàn thiện
Các biểu đồ cần có:
- **Bộ lọc (Filters)**
  + Year: Lọc theo năm
  + Month: Lọc theo tháng trong năm
  + Hình thức bán
  + Phương thức thanh toán
- **Chỉ số tổng quan (KPIs)**
  + Doanh thu
  + Lợi nhuận
  + % Lợi nhuận
- **Biểu đồ**
  + Monthly Bar Chart: Hiển thị doanh thu, lợi nhuận và tỷ lệ lợi nhuận theo từng tháng
  + Daily Area Chart: Biểu đồ theo ngày giúp theo dõi xu hướng biến động trong tháng
  + Top sản phẩm: Liệt kê sản phẩm có doanh số cao nhất
  + Top danh mục: Danh mục có doanh số cao nhất
  + Pie Chart - Hình thức bán: Tỷ lệ giữa các hình thức bán
  + Pie Chart - Phương thức thanh toán
  + Pie Chart - Danh mục theo các danh mục sản phẩm 

  ---
  
## 📊 Dashboard hoàn thiện 

![image](https://github.com/user-attachments/assets/fdc62780-9f36-4a15-b93e-c0e6ad90e96e)
