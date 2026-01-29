# superstore-data-analysis
Sales performance analysis using Excel, SQL and Power BI
# 📊 Superstore Sales & Profit Analysis

## 📌 Project Overview
This project analyses retail sales data from a Superstore dataset to identify sales trends, profitability drivers, and loss-making areas.  
The analysis follows a complete end-to-end data analytics workflow using **Excel**, **MySQL**, and **Power BI**, with a strong focus on turning data into actionable business insights.

This repository demonstrates practical data analysis skills, clear documentation, and business-focused storytelling.

---

## 🗂️ Data Source
- Dataset: **SuperStoreOrders.csv**
- Granularity: Order-level transactional data
- Key attributes include:
  - Order and ship dates
  - Customer and regional information
  - Product category and sub-category
  - Sales, profit, quantity, and discount values

---

## 🧮 Step 1: Excel Analysis

### Excel File
- **excel/superstore_analysis.xlsx**

### Sheets
- **Raw_Data** – Original dataset (unchanged)
- **Cleaned_Data** – Cleaned and standardised data
- **Pivot_Analysis** – Pivot tables for exploratory analysis

### Key Excel Activities
- Data type validation (dates, numeric fields)
- Removal of inconsistencies and formatting issues
- Pivot table analysis for:
  - Sales and profit by category and sub-category
  - Regional performance
  - Profitability patterns
- Excel served as the first validation layer before SQL analysis

---

## 🗄️ Step 2: SQL Analysis (MySQL)

### Database
- MySQL (via MySQL Workbench)

### Purpose
SQL was used to validate Excel findings, perform aggregations, and analyse trends in a structured and repeatable way.

### Key Operations
- Table creation and data loading
- Aggregation of sales and profit metrics
- Identification of loss-making sub-categories
- Monthly sales trend analysis using MySQL-compatible date functions

### Example Query
```sql
SELECT
    DATE_FORMAT(Order_Date, '%Y-%m-01') AS Month,
    SUM(Sales) AS Total_Sales
FROM superstore
GROUP BY Month
ORDER BY Month;
All SQL queries used in this project are stored in sql/queries.sql.

📊 Step 3: Power BI Dashboard
File
powerbi/superstore_dashboard.pbix

Dashboard Pages
Executive Overview

Total Sales

Total Profit

Profit Margin

Order Count

Monthly Sales Trend

Category & Sub-Category Analysis

Sales contribution by category

Profitability by sub-category

Identification of loss-making products

Regional Performance

Sales and profit by region

Regional efficiency comparison

Power BI Focus
Clean, business-friendly layout

KPI-driven storytelling

Clear insights for non-technical stakeholders

📈 Key Insights
Technology generates high sales but does not always deliver the highest profit margins

Several sub-categories consistently record losses despite strong sales volume

Discounting has a clear negative impact on overall profitability

Regional performance varies significantly, indicating operational inefficiencies

💡 Business Recommendations
Re-evaluate discount strategies for loss-making sub-categories

Prioritise high-margin products over high-volume, low-profit items

Investigate cost structures in underperforming regions

Use profit margin as a primary performance metric alongside sales

🛠 Tools & Technologies
Excel – Data cleaning, validation, and exploratory analysis

MySQL – Structured querying and aggregation

Power BI – Data modelling, visualisation, and dashboard storytelling

GitHub – Version control and project documentation

📁 Repository Structure
├── data/
│   └── SuperStoreOrders.csv
├── excel/
│   └── superstore_analysis.xlsx
├── sql/
│   └── queries.sql
├── powerbi/
│   └── superstore_dashboard.pbix
├── images/
│   └── dashboard_screenshots.png
└── README.md
🏃‍♂️ How to Explore This Project
Review the dataset in data/

Open the Excel file to see cleaning and pivot analysis

Run queries in sql/queries.sql using MySQL Workbench

Open the Power BI file to explore interactive dashboards
