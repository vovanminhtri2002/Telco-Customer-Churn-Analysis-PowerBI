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
- [💡 Insight nổi bật](#-insight-nổi-bật)
- [💡 Các Measure DAX chính](#-các-measure-dax-chính) 
- [📁 Cấu trúc thư mục](#-cấu-trúc-thư-mục)
- [🔮 Hướng phát triển](#-hướng-phát-triển)
- [👨‍💻 Tác giả](#-tác-giả)
- [📜 License](#-license)

---

## ✨ Giới thiệu

Dự án **Telco Customer Churn Analysis** được xây dựng bằng **Microsoft Power BI**, tập trung phân tích hành vi rời bỏ (**Churn**) của khách hàng ngành viễn thông.

Báo cáo giúp doanh nghiệp **trả lời 5 câu hỏi sống còn**:

**1. Ai đang rời bỏ?** (Chân dung khách hàng churn)

**2. Tại sao họ rời bỏ?** (Dịch vụ, chi phí, hợp đồng…)

**3. Dịch vụ nào gây rủi ro nhiều nhất?**

**4. Nhóm khách hàng nào cần ưu tiên giữ chân?**

**5. Chiến lược nào giảm churn hiệu quả nhất?**

**Dashboard** gồm **4 trang chuẩn BI**, thiết kế theo hướng:
👉 _Insight-driven – Business-focused – Actionable KPIs_

---

## 📌 Mục tiêu dự án

- Tính toán **tỷ lệ Churn** tổng & theo từng phân khúc

- Xác định **chân dung khách hàng rời bỏ**

- Tìm nguyên nhân chính ảnh hưởng đến churn

- Xây dựng **Dashboard gồm 4 trang chuyên nghiệp**

- Sử dụng **DAX** để tính KPI mang tính hành động

- Trình bày báo cáo theo chuẩn **Business Intelligence**

---

## 📂 Nguồn dữ liệu

- Dataset: **Telco Customer Churn – Kaggle**

- Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

- Dữ liệu gồm:

  - **7043 khách hàng**

  - **21 biến thông tin**

  - Định dạng: **CSV**

Chủ yếu gồm các trường:

- Nhân khẩu học (**Gender, SeniorCitizen, Partner, Dependents**)

- Thông tin dịch vụ (**InternetService, Security, Backup...**)

- Chi phí (**MonthlyCharges, TotalCharges**)

- Hợp đồng & thanh toán (**Contract, PaymentMethod**)

-  Mục tiêu: **Churn (Yes/No)**

---

## 🧠 Quy trình thực hiện

🔧 **1. Làm sạch dữ liệu – Power Query**

- Xử lý giá trị null

- Loại dòng lỗi

- Chuyển đổi kiểu dữ liệu chính xác

- Convert TotalCharges → Decimal Number

- Tạo cột phân loại tuổi, phân khúc tenure

🔨 **2. Tạo các DAX Measure**

- **Churn Rate**

- **Senior Citizen Count**

- **Average Tenure**

- **Partner %**

- **Dependent %**

- Tổng số khách hàng

- Churn theo dịch vụ / phân khúc

🎨 **3. Thiết kế Dashboard**

- **Card KPI**

- **Bar chart, donut chart, line chart**

- **Slicer lọc động theo giới tính, hợp đồng, internet service**

- **Tooltip custom**

📤 **4. Xuất file & quản lý repo**

- Lưu file .pbix

- Tách thư mục **images, data, documents**

---

## 📊 Tổng quan Dashboard

Dashboard được chia thành 4 trang:

1️⃣ **Home** – Trang giới thiệu và điều hướng <br>
2️⃣ **Overview Dashboard** – KPI & rủi ro tổng quan <br>
3️⃣ **Service Analysis** – Phân tích theo dịch vụ sử dụng <br>
4️⃣ **Customer Insights** – Hành vi & phân khúc khách hàng

---

## 1️⃣ Home

Trang mở đầu gồm:

- Tên dự án

- Mô tả dữ liệu

- Call-to-action dẫn đến các trang phân tích

<p align="center">
  <img src="https://github.com/user-attachments/assets/94acfbbc-9368-4333-88ee-17d235e9ae98" 
       alt="Home_Dashboard"
       width="800">
</p>

---

## 2️⃣ Overview Dashboard

📌 **KPI chính:**

- **Churn Rate**

- **Senior Citizen Count**

- **Partner %**

- **Dependent %**

- **Average Tenure**

📌 **Biểu đồ:**

- **Churn by Gender**

- **Churn by Contract**

- **Churn by Senior Citizen**

- **Churn by MonthlyCharges**

Trang này giúp xác định **bức tranh tổng quan về rủi ro churn.**

<p align="center">
  <img src="https://github.com/user-attachments/assets/5ac3b475-1c17-4e4f-8ce8-f155f8ba7f11"
       alt="Overview_Dashboard"
       width="800">
</p>

---

## 3️⃣ Service Analysis

Phân tích **tác động của dịch vụ** lên churn:

- **Internet Service vs Churn**

- **Online Security / Backup**

- **Device Protection**

- **Contract Type**

- **Payment Method**

<p align="center">
  <img src="https://github.com/user-attachments/assets/81ac8ad2-3dfa-49a7-84c8-867b8ec1d598"
       alt="Service_Analysis"
       width="800">
</p>

---

## 4️⃣ Customer Insights

Tập trung vào **hành vi & vòng đời khách hàng:**

- **Tenure vs Churn**

- **Age Group**

- **Monthly Charges**

- **Customer Lifetime Value (CLV)**

Slicer tùy chọn:

- **Contract**

- **Gender**

- **Payment Method**

- **Internet Service**

<p align="center">
  <img src="https://github.com/user-attachments/assets/f3fd75c0-128c-4c41-869c-a96422cf066c"
       alt="Customer_Insights"
       width="800">
</p>

---

## 💡 Insight nổi bật

🔥 **1. Khách hàng dùng hợp đồng tháng có tỷ lệ churn cao gấp ~3 lần so với hợp đồng 1–2 năm.**

➡️ _Gợi ý:_ Tập trung upsell sang hợp đồng dài hạn.

🔥 **2. Nhóm Senior Citizen có khả năng churn cao hơn đáng kể.**

➡️ _Gợi ý:_ Xây gói hỗ trợ hoặc khuyến mãi riêng.

🔥 **3. Khách hàng có Monthly Charges cao (> 80$) rời bỏ nhiều hơn.**

➡️ _Gợi ý:_ Đề xuất bundle service để giảm chi phí cảm nhận.

🔥 **4. Dịch vụ Online Security và Backup có mức churn cao khi khách hàng Không sử dụng.**

➡️ _Gợi ý:_ Giới thiệu dịch vụ bảo mật như giá trị gia tăng.

🔥 **5. Tenure < 12 tháng → nhóm có rủi ro cao nhất.**

➡️ _Gợi ý:_ Chương trình welcome/retention 90 ngày đầu.

---

## 💡 Các Measure DAX chính

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

Tích hợp **Machine Learning** → dự đoán khách hàng churn

Kết nối **SQL Database**

**Auto-refresh** dữ liệu

Trang **Recommendation Engine** sử dụng **AI**

**Publish** lên **Power BI Service**

Tạo **Dashboard Mobile View**

---

## 👨‍💻 Tác giả

Họ tên: **Võ Văn Minh Trí**

Email: **vovanminhtri2002@gmail.com**

Công cụ: **Power BI, Power Query, DAX**

---

## 📜 License

MIT License © 2025

---
