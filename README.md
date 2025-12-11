# 📊 Telco Customer Churn Analysis – Power BI Dashboard

<p align="center"> <img src="https://img.shields.io/badge/PowerBI-Analytics-orange?logo=powerbi"> <img src="https://img.shields.io/badge/Status-Completed-success"> <img src="https://img.shields.io/badge/Data-Kaggle-blue?logo=kaggle"> <img src="https://img.shields.io/badge/Visualization-DAX%20%26%20PowerQuery-green"> </p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a1d244d7-7fa8-4584-b88e-0f86d247266f"
       alt="Telco_Customer_Churn"
       width="800">
</p>

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

## ✨ Giới thiệu

Dự án Telco Customer Churn Analysis phân tích hiện tượng khách hàng rời bỏ (Churn) dựa trên dữ liệu viễn thông từ Kaggle.
Sử dụng Power BI để tạo dashboard trực quan, hỗ trợ doanh nghiệp:

Phát hiện nhóm khách hàng có nguy cơ rời bỏ cao

Hiểu dịch vụ nào đang khiến khách hàng không hài lòng

Theo dõi KPI vận hành – dịch vụ – khách hàng

Đưa ra chiến lược giữ chân & tối ưu doanh thu

Dashboard được chia thành 4 trang với luồng phân tích logic từ tổng quan → nguyên nhân → hành vi.

---

## 📌 Mục tiêu dự án

Xác định tỷ lệ churn tổng và theo từng phân khúc khách hàng

Phân tích yếu tố ảnh hưởng mạnh nhất đến churn (Contract, Internet Service, Payment…)

Xây dựng hệ thống KPI bằng DAX Measure

Thiết kế báo cáo đúng chuẩn BI, đầy đủ insight và có khả năng hỗ trợ quyết định kinh doanh

Tạo dashboard 4 trang trực quan, giúp doanh nghiệp hiểu khách hàng nhanh chóng

---

## 📂 Nguồn dữ liệu

Dataset: Telco Customer Churn
📄 Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

Định dạng: CSV

Số dòng: 7043

Số cột: 21

Bao gồm thông tin:

Loại hợp đồng

Loại dịch vụ Internet

Phương thức thanh toán

Tổng phí hàng tháng & tổng phí tích lũy

Giới tính, độ tuổi, tình trạng hôn nhân

Nhãn mục tiêu: Churn (Yes/No)

---

## 🧠 Quy trình thực hiện

1. Làm sạch dữ liệu (Power Query)

Xử lý null

Chuẩn hóa format dữ liệu

Chuyển TotalCharges → số (numeric)

Loại bỏ các dòng lỗi / ký tự không hợp lệ

2. Xây dựng Measure DAX

KPI về churn

KPI nhóm khách hàng đặc biệt: Partner, Senior Citizen, Dependents

Thống kê tenure, chi phí, phân bổ dịch vụ

3. Thiết kế Dashboard (4 trang)

Dùng Card KPI, Bar Chart, Donut, Line Chart

Thêm Tooltip + Slicer điều khiển

Tạo navigation trực quan giữa các trang

4. Xuất file & publish lên GitHub

---

## 📊 Tổng quan Dashboard

Dashboard được chia thành 4 trang:

1️⃣ Home – Trang giới thiệu và điều hướng
2️⃣ Overview Dashboard – KPI & rủi ro tổng quan
3️⃣ Service Analysis – Phân tích theo dịch vụ sử dụng
4️⃣ Customer Insights – Hành vi & phân khúc khách hàng

## 1️⃣ Home

Trang mở đầu gồm:

Logo dự án

Mô tả dataset

Nút điều hướng → 3 trang còn lại

Tóm tắt các mục phân tích

<p align="center">
  <img src="https://github.com/user-attachments/assets/94acfbbc-9368-4333-88ee-17d235e9ae98" 
       alt="Home_Dashboard"
       width="800">
</p>

---

## 2️⃣ Overview Dashboard

Trang quan trọng nhất: cung cấp cái nhìn tổng quan về rủi ro churn.

📌 KPI chính gồm:

Churn Rate

Senior Citizen Count

Partner %

Dependent %

Average Tenure

📌 Biểu đồ Insight:

Churn theo giới tính

Churn theo loại hợp đồng → Hop̀ đồng Month-to-Month là nhóm rủi ro cao nhất

Churn theo Senior Citizen → Người lớn tuổi có tỷ lệ rời bỏ cao hơn

MonthlyCharges vs Churn → Chi phí cao → churn nhiều

<p align="center">
  <img src="https://github.com/user-attachments/assets/5ac3b475-1c17-4e4f-8ce8-f155f8ba7f11"
       alt="Overview_Dashboard"
       width="800">
</p>

---

## 3️⃣ Service Analysis

Trang này tập trung vào dịch vụ mà khách hàng đang dùng.

Bao gồm phân tích:

Internet Service vs Churn

OnlineSecurity / Backup / Device Protection

Contract Type

Payment Method

Insight:

Khách hàng dùng Fiber Optic có tỷ lệ churn cao hơn DSL

Những khách hàng không dùng OnlineSecurity rời bỏ nhiều hơn

Payment bằng Electronic Check là nhóm churn cao nhất

<p align="center">
  <img src="https://github.com/user-attachments/assets/81ac8ad2-3dfa-49a7-84c8-867b8ec1d598"
       alt="Service_Analysis"
       width="800">
</p>

---

## 4️⃣ Customer Insights

Trang cuối tập trung hiểu hành vi khách hàng:

Tenure vs Churn → Khách mới (tenure thấp) dễ rời bỏ nhất

Age Group

Monthly Charges

CLV (Customer Lifetime Value)

Slicer mạnh giúp phân tích theo:

Contract

Gender

Payment Method

Internet Service

<p align="center">
  <img src="https://github.com/user-attachments/assets/f3fd75c0-128c-4c41-869c-a96422cf066c"
       alt="Customer_Insights"
       width="800">
</p>

---

## 🛠️ Các Measure DAX chính

```bash
Customer Count = COUNTROWS(Data)
```

```bash
Churn Count =
CALCULATE(COUNTROWS(Data), Data[Churn] = "Yes")
```

```bash
Churn Rate =
DIVIDE([Churn Count], [Customer Count])
```

```bash
Senior Citizen Count =
CALCULATE(COUNTROWS(Data), Data[SeniorCitizen] = 1)
```

```bash
Partner % =
DIVIDE(
    CALCULATE(COUNTROWS(Data), Data[Partner] = "Yes"),
    [Customer Count]
)
```

```bash
Dependent % =
DIVIDE(
    CALCULATE(COUNTROWS(Data), Data[Dependents] = "Yes"),
    [Customer Count]
)
```

```bash
Average Tenure = AVERAGE(Data[tenure])
```

---

## 📁 Cấu trúc thư mục

```bash
├── powerbi/
│   └── Telco_Customer_Churn.pbix
├── data/
│   └── Telco_Customer_Churn.csv
├── images/
│   ├── Telco_Customer_Churn.png
│   ├── Telco.png
└── documents/
    └── Telco_Customer_Churn_Report.docx
```

---

## 🔮 Hướng phát triển

Tích hợp Machine Learning dự đoán khả năng churn

Kết nối SQL Server / Azure / BigQuery để tự động refresh dữ liệu

Thêm trang Recommendation System – gợi ý giữ chân khách hàng

Publish lên Power BI Service và tạo dashboard real-time

---

## 👨‍💻 Tác giả

Họ tên: **Võ Văn Minh Trí**

Email: **vovanminhtri2002@gmail.com**

Công cụ: **Power BI, Power Query, DAX**

---

## 📜 License

MIT License © 2025

---
