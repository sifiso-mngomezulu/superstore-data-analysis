# superstore-data-analysis
Sales performance analysis using Excel, SQL and Power BI
# 📊 Superstore Sales Analysis

## 📌 Project Overview
This project analyses retail sales data from a Superstore dataset to uncover sales trends, profitability drivers, and loss-making areas.  
The analysis follows a complete analytics workflow using **Excel**, **MySQL**, and **Power BI**, with a strong focus on translating data insights into actionable business recommendations.

The goal of this project is to demonstrate end-to-end data analysis skills, from raw data exploration to dashboard storytelling.

---

## 🔹 Step 1: Data Source
- Dataset: **SuperStoreOrders.csv**
- Granularity: Order-level data
- Key fields include:
  - Order and ship dates
  - Customer, segment, and regional information
  - Product category and sub-category
  - Sales, profit, quantity, and discount values

---

## 🔹 Step 2: Excel Analysis

### Excel File
- File name: **superstore_analysis.xlsx**
- Sheets created:
  - **Raw_Data** – Original dataset imported without modifications
  - **Cleaned_Data** – Data cleaned and standardised
  - **Pivot_Analysis** – Pivot tables used for exploratory analysis

### Key Excel Activities
- Data type validation (dates, numeric fields)
- Handling missing and inconsistent values
- Creation of pivot tables to analyse:
  - Sales and profit by category and sub-category
  - Regional performance
  - High-level profitability trends
- Excel was used as the first validation layer before SQL analysis

---

## 🔹 Step 3: SQL Analysis (MySQL)

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
All SQL queries used in this project are stored in the sql/queries.sql file.

##🔹 Step 4: Power BI Dashboard
Data Model

Source data imported from cleaned CSV / SQL outputs

Relationships validated and data types corrected in Power Query

Dashboard Pages

Executive Overview

Total Sales

Total Profit

Profit Margin

Orders Count

High-level trends and KPIs

Category & Sub-Category Analysis

Sales and profit contribution by category

Identification of underperforming sub-categories

Regional Performance

Sales and profit by region

Comparison of regional efficiency

Power BI Focus Areas

Clean and simple layout

Business-focused KPIs

Clear storytelling for non-technical stakeholders

## 📊 Key Insights

Technology generates the highest sales, but not always the highest profit margin

Certain sub-categories consistently generate losses despite strong sales volume

Discounts have a noticeable negative impact on profitability

Regional performance varies significantly, indicating operational inefficiencies

## 💡 Business Recommendations

Re-evaluate discount strategies for loss-making sub-categories

Focus marketing and inventory efforts on high-margin products

Investigate operational costs in underperforming regions

Use profit margin rather than sales volume as a primary performance metric

## 🛠 Tools & Technologies

Excel – Data cleaning, validation, and exploratory analysis

MySQL – Structured querying and aggregation

Power BI – Data modelling, visualisation, and dashboard storytelling

GitHub – Version control and project documentation

