# 📊 SMH Analytics - Power BI Executive Dashboard

An interactive and visually rich Power BI dashboard designed to analyze sales performance, customer insights, and business trends.

---

## 🚀 Project Overview

This dashboard provides a complete business intelligence solution including:

- Sales performance tracking
- Customer and product analysis
- Regional insights
- Calendar-based data visualization

Built using **Power BI**, this dashboard helps stakeholders make data-driven decisions efficiently.

## 📂 Project Files

### 📊 Power BI Dashboard
[Download Executive Dashboard](https://github.com/msameerhanif/SMH-Analytics-PowerBI-Dashboard/blob/main/Dashboard/Executive%20Dashboard.pbix)

---

### 📸 Screenshots

- [View Dashboard Overview](https://github.com/msameerhanif/SMH-Analytics-PowerBI-Dashboard/blob/main/Screenshots/dashboard_overview.PNG)
- [View Calendar View](https://github.com/msameerhanif/SMH-Analytics-PowerBI-Dashboard/blob/main/Screenshots/calendar_view.PNG)


---

## 📌 Key Features

### 📈 KPI Metrics
- Total Sales: 1.20M
- Total Quantity Sold: 567K
- Total Cost: 483.62K
- Total Profit: 715.69K

### 📊 Visual Insights
- Top 10 Products by Sales & Orders
- Top 10 Customers Analysis
- Store-wise Sales Performance
- Region-wise Sales Distribution
- Store Type Contribution (Donut Chart)

### 📅 Calendar View
- Dynamic monthly calendar
- Week-wise date alignment
- Integrated slicers for filtering

---

## 🛠 Tools & Technologies

- Microsoft Power BI
- DAX (Data Analysis Expressions)
- Data Modeling
- Data Visualization

---

## 🧠 Key DAX Concepts Used

- VAR (Variables)
- CALCULATE
- DIVIDE
- Time Intelligence Functions
- Custom Calendar Table

Example:

```DAX
Sales Change = 
VAR Curr = [Total Sales Tooltip]
VAR Prev = [Sales Prev Day]
RETURN
IF(
    ISBLANK(Curr), BLANK(),
    FORMAT( DIVIDE( Curr - Prev, ABS( Prev ), 0 ), "0.0%" ) & " | " &
    FORMAT( Curr - Prev, "#,##0" )
)
