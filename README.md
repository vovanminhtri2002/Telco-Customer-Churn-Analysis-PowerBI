# 📊 Telco Customer Churn Analysis – Power BI Dashboard

<p align="center"> <img src="https://img.shields.io/badge/PowerBI-Analytics-orange?logo=powerbi"> <img src="https://img.shields.io/badge/Status-Completed-success"> <img src="https://img.shields.io/badge/Data-Kaggle-blue?logo=kaggle"> <img src="https://img.shields.io/badge/Visualization-DAX%20%26%20PowerQuery-green"> </p>

---

## 📖 Mục lục

- [✨ Giới thiệu](#-giới-thiệu)
- [📌 Mục tiêu dự án](#-mục-tiêu-dự-án)
- [📂 Nguồn dữ liệu](#-nguồn-dữ-liệu)
- [🧠 Quy trình thực hiện](#-quy-trình-thực-hiện)
- [📊 Tổng quan Dashboard](#-tổng-quan-dashboard)
- [1️⃣ Home](#1️⃣-home)
- [2️⃣ Overview Dashboard](#2️⃣-overview-dashboard)
- [3️⃣ Service Analysis](#3️⃣-service-analysis)
- [4️⃣ Customer Insights](#4️⃣-customer-insights)
- [🛠️ Các Measure DAX chính](#-các-measure-dax-chính)
- [📁 Cấu trúc thư mục](#-cấu-trúc-thư-mục)
- [🔮 Hướng phát triển](#-hướng-phát-triển)
- [👨‍💻 Tác giả](#-tác-giả)
- [📜 License](#-license)

---

✨ Giới thiệu

Dự án Telco Customer Churn Analysis sử dụng Microsoft Power BI để phân tích hành vi khách hàng rời bỏ (Churn) của một công ty viễn thông.

Dashboard được thiết kế theo hướng trực quan – logic – dễ đưa ra quyết định, hỗ trợ doanh nghiệp:

Xác định nhóm khách hàng có nguy cơ rời bỏ cao

Phân tích dịch vụ ảnh hưởng đến churn

Theo dõi KPI tổng quan

Tìm insight theo độ tuổi, giới tính, hợp đồng, phương thức thanh toán,...

📌 Mục tiêu dự án

Tính toán tỷ lệ churn tổng & theo từng phân khúc

Xác định yếu tố rủi ro cao (Internet Service, Contract, Payment, Senior Citizen…)

Tạo dashboard 4 trang đầy đủ thông tin

Ứng dụng DAX để xây KPI chuyên nghiệp

Trình bày báo cáo theo chuẩn BI

📂 Nguồn dữ liệu

Dataset: Telco Customer Churn

Nguồn: Kaggle

Định dạng: .csv

Gồm 7043 dòng – 21 cột thông tin khách hàng

🧠 Quy trình thực hiện

Làm sạch dữ liệu trong Power Query

Xử lý giá trị null

Định dạng lại dữ liệu (Text / Number / Decimal)

Chuyển TotalCharges → kiểu số

Tạo các Measure DAX

Churn Rate, Retention Rate

Senior Citizen Count

Partner %

Dependents %

Average Tenure

Thiết kế 4 trang báo cáo chuẩn BI

Thêm Tooltip, Slicer, Card KPI

Xuất file (.pbix) và lưu repository

📊 Tổng quan Dashboard
1️⃣ Home

Trang mở đầu bao gồm:

Logo dự án

Tên báo cáo

Mô tả dataset

Nút điều hướng sang 3 trang tiếp theo

2️⃣ Overview Dashboard

Trang tổng quan KPI:

📌 KPI chính (4 Card):

Churn Rate

Senior Citizen Count

Partner %

Dependent %

Average Tenure

📌 Biểu đồ:

Churn by Gender

Churn by Contract

Churn by Senior Citizen

Churn by MonthlyCharges

Trang này giúp đánh giá tổng quan rủi ro rời bỏ khách hàng.

3️⃣ Service Analysis

Phân tích sâu các dịch vụ:

Internet Service vs Churn

Online Security / Backup / Device Protection

Contract Type

Payment Method

Giúp tìm ra dịch vụ làm khách hàng rời bỏ nhiều nhất.

4️⃣ Customer Insights

Phân tích hành vi khách hàng:

Tenure vs Churn

Age Group

Monthly Charges

Customer Lifetime Value (CLV)

Slicer lọc theo:

Contract

Gender

Payment

Internet Service

Giúp đưa ra gợi ý chiến lược giữ chân khách hàng.

🛠️ Các Measure DAX chính
Customer Count = COUNTROWS(Data)

Churn Count =
CALCULATE(COUNTROWS(Data), Data[Churn] = "Yes")

Churn Rate =
DIVIDE([Churn Count], [Customer Count])

Senior Citizen Count =
CALCULATE(COUNTROWS(Data), Data[SeniorCitizen] = 1)

Partner % =
DIVIDE(
    CALCULATE(COUNTROWS(Data), Data[Partner] = "Yes"),
    [Customer Count]
)

Dependent % =
DIVIDE(
    CALCULATE(COUNTROWS(Data), Data[Dependents] = "Yes"),
    [Customer Count]
)

Average Tenure = AVERAGE(Data[tenure])

📁 Cấu trúc thư mục
├── powerbi/
│   └── Telco_Customer_Churn.pbix
├── data/
│   └── Telco_Customer_Churn.csv
├── images/
│   ├── Telco_Customer_Churn.png
│   ├── Telco.png
└── documents/
    └── Telco_Customer_Churn_Report.docx

🔮 Hướng phát triển

Thêm Machine Learning dự đoán Churn

Kết nối SQL Database thay vì import CSV

Tự động refresh dữ liệu

Thêm trang Recommendation – gợi ý giữ khách hàng

Publish lên Power BI Service cho phép chia sẻ online

👨‍💻 Tác giả

Họ tên: Võ Văn Minh Trí

Email: vovanminhtri2002@gmail.com

Công cụ: Power BI, Power Query, DAX

📜 License

MIT License © 2025
