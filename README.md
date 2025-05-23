# Dự án Xây dựng Data Warehouse và Báo cáo Power BI từ file detail.xlsx

## Mô tả dự án

Dự án này thực hiện các bước xây dựng hệ thống phân tích dữ liệu (Business Intelligence) từ file nguồn `Traffic_Accidents.csv`, bao gồm:

- Thiết kế và xây dựng **Data Warehouse** trên SQL Server
- ETL dữ liệu bằng **SSIS (SQL Server Integration Services)**
- Xây dựng mô hình phân tích đa chiều với **SSAS (SQL Server Analysis Services)**
- Trực quan hóa và xây dựng báo cáo động bằng **Power BI**

## Quy trình thực hiện

### 1. Thiết kế Data Warehouse

- Phân tích dữ liệu nguồn từ file `Traffic_Accidents.csv`
- Thiết kế lược đồ **Star Schema** hoặc **Snowflake Schema** phù hợp (các bảng Fact và Dimension)
- Tạo các bảng trong SQL Server

### 2. ETL với SSIS

- Tạo project SSIS mới
- Sử dụng Data Flow để:
  - Đọc dữ liệu từ file `Traffic_Accidents.csv`
  - Làm sạch, chuyển đổi dữ liệu (Data Cleansing, Transformation)
  - Nạp dữ liệu vào các bảng Data Warehouse trên SQL Server

### 3. Xây dựng mô hình phân tích với SSAS

- Tạo project SSAS mới (Multidimensional hoặc Tabular)
- Kết nối đến Data Warehouse vừa xây dựng
- Thiết lập các **Dimension** và **Measure** (ví dụ: doanh thu, số lượng, thời gian, sản phẩm, khách hàng, khu vực...)
- Triển khai (Deploy) và xử lý (Process) mô hình lên SSAS Server

### 4. Trực quan hóa với Power BI

- Kết nối Power BI đến mô hình SSAS hoặc trực tiếp đến Data Warehouse
- Xây dựng các báo cáo, dashboard động:
  - Báo cáo tổng quan (doanh thu, số lượng, tăng trưởng...)
  - Phân tích theo chiều thời gian, sản phẩm, khách hàng, khu vực...
  - Drill-down, lọc động, biểu đồ trực quan (bar, line, map...)

## Yêu cầu hệ thống

- SQL Server (khuyến nghị bản Enterprise hoặc Developer)
- SSIS, SSAS đã cài đặt
- Power BI Desktop
- File dữ liệu nguồn: `Traffic_Accidents.csv`

## Hướng dẫn sử dụng

1. **Chuẩn bị dữ liệu**
   - Đặt file `Traffic_Accidents.csv` vào thư mục dữ liệu dự án

2. **Tạo Data Warehouse**
   
   - Generate code sql để tạo Data Warehouse bằng Dimensional Modeling Workbook
   - Thiết kế và tạo các bảng trên SQL Server theo lược đồ đã phân tích

3. **ETL với SSIS**
   - Tạo package SSIS để nạp dữ liệu từ Excel vào SQL Server

4. **Xây dựng mô hình SSAS**
   - Tạo project, kết nối đến Data Warehouse, thiết lập các Dimension/Measure

5. **Trực quan hóa với Power BI**
   - Kết nối đến SSAS/Data Warehouse, xây dựng báo cáo và dashboard

## Kết quả

- Hệ thống Data Warehouse chuẩn hóa, dễ dàng mở rộng
- Quy trình ETL tự động, đảm bảo dữ liệu sạch và đồng nhất
- Mô hình phân tích đa chiều mạnh mẽ, hỗ trợ truy vấn nhanh
- Báo cáo Power BI trực quan, hỗ trợ ra quyết định kinh doanh

---

**Tác giả:**  
Nguyen Thanh An  
