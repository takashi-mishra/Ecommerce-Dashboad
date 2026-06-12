# 📊 Mobile Sales Analysis Dashboard

## 📌 Project Overview

The Mobile Sales Analysis Dashboard is an interactive Business Intelligence solution developed using Microsoft Power BI. The project analyzes sales data of a mobile showroom business operating across multiple cities in India.

The dashboard provides valuable insights into sales performance, customer behavior, product demand, payment preferences, and year-over-year growth trends. It enables management to make data-driven decisions through dynamic visualizations and KPI tracking.

---

## 🎯 Project Objectives

- Monitor overall sales performance.
- Track Total Revenue, Transactions, and Units Sold.
- Analyze monthly, quarterly, and yearly sales trends.
- Compare current year sales with previous year performance.
- Measure Month-to-Date (MTD) sales growth.
- Identify top-performing mobile brands and models.
- Analyze customer ratings and satisfaction.
- Study customer payment preferences.
- Provide interactive filtering and drill-down capabilities.

<div align="center"> <img src="https://github.com/takashi-mishra/Ecommerce-Dashboad/blob/main/Screenshot%202026-06-09%20155049.png" height="600" /> </div>
---

## 🗂 Dataset Information

The dataset contains transactional sales data from a mobile showroom business.

### Key Attributes

- Transaction ID
- Date
- Brand
- Mobile Model
- Units Sold
- Price Per Unit
- Customer Name
- Customer Age
- City
- Payment Method
- Customer Rating

---

## 🛠 Data Preprocessing

Before building the dashboard, the dataset was cleaned and transformed using Power Query.

### Steps Performed

- Removed duplicate records
- Handled missing values
- Standardized categorical values
- Converted data types
- Validated data quality
- Created calculated columns
- Prepared data for analysis

---

## 🏗 Data Modeling

A custom Calendar Table was created to support time intelligence calculations.

### Data Model Features

- Star Schema Design
- Relationship Management
- Custom Date Table
- Time Intelligence Support
- Optimized Query Performance

The Calendar Table was linked with the Sales Table using Date relationships for advanced analysis.

---

## 📐 DAX Measures Used

Several DAX measures were created to perform business calculations.

### Total Sales Amount

```DAX
Total Sales Amount =
SUMX(
Sales,
Sales[Units Sold] * Sales[Price Per Unit]
)
Total Units Sold
Total Units Sold =
SUM(Sales[Units Sold])
Transaction Count
Transaction Count =
COUNT(Sales[Transaction ID])
Average Price Per Unit
Average Price =
AVERAGE(Sales[Price Per Unit])
Last Year Sales
Last Year Sales =
CALCULATE(
[Total Sales Amount],
SAMEPERIODLASTYEAR(Calendar[Date])
)
Month-To-Date Sales
MTD Sales =
TOTALMTD(
[Total Sales Amount],
Calendar[Date]
)
📈 Dashboard Pages

1️⃣ Main Dashboard

Provides an overview of:

Total Sales Amount
Average Price Per Unit
Total Transactions
Total Units Sold
Sales by Month
Sales by Day
Customer Ratings
Payment Method Analysis
Sales Distribution by City
2️⃣ MTD Dashboard

Displays:

Month-To-Date Sales
Daily Sales Progression
Monthly Growth Tracking
Interactive Drill-Down Analysis
3️⃣ Last Year Dashboard

Provides:

Year-over-Year Comparison
Quarterly Analysis
Monthly Analysis
Historical Sales Trends
📊 Key KPIs
KPI	Description
Total Sales Amount	Total Revenue Generated
Average Price Per Unit	Average Selling Price
Transaction Count	Total Sales Transactions
Total Units Sold	Total Quantity Sold
Last Year Sales	Previous Year Revenue
MTD Sales	Current Month Progress
🔍 Insights Generated
Revenue exceeded 769 Million.
More than 19K mobile units were sold.
Digital payment methods dominate customer transactions.
Customer ratings indicate high satisfaction levels.
Certain mobile models generate significantly higher sales.
Sales performance varies across cities and months.
Strong Year-over-Year business growth observed.
🚀 Features

✔ Interactive Dashboard

✔ Dynamic Filters & Slicers

✔ Custom Calendar Table

✔ Data Modeling

✔ DAX Calculations

✔ MTD Analysis

✔ Year-over-Year Analysis

✔ Quarterly Trend Analysis

✔ Drill-Down Functionality

✔ Responsive Visualizations

🧰 Tools & Technologies
Microsoft Power BI
Power Query
DAX (Data Analysis Expressions)
Data Modeling
Microsoft Excel

💼 Business Benefits
Faster decision-making
Improved sales monitoring
Better inventory planning
Enhanced customer understanding
Revenue growth tracking
Performance benchmarking
🎓 Learning Outcomes

Through this project, I gained hands-on experience in:

Power BI Dashboard Development
Data Cleaning & Transformation
Data Modeling
Time Intelligence Functions
DAX Calculations
Business Analytics
KPI Development
Data Visualization
👨‍💻 Author

Yogesh Mishra

Full Stack MERN Developer | Data Analyst | Power BI Developer

Skills
Power BI
SQL
Excel
DAX
Power Query
React.js
Node.js
Express.js
MongoDB
⭐ If you found this project useful, don't forget to star the repository.

### GitHub Repository Structure

```text
Mobile-Sales-Dashboard/
│
├── Dataset/
│   └── Mobile_Sales_Data.xlsx
│
├── Dashboard/
│   └── Mobile_Sales_Dashboard.pbix
│
├── Screenshots/
│   ├── Main_Dashboard.png
│   ├── MTD_Dashboard.png
│   └── Last_Year_Dashboard.png
│
├── Report/
│   └── Mobile_Sales_Report.pdf
│
└── README.md

