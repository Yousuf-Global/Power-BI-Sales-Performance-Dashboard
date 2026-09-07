# Sales Performance Dashboard | Power BI

## 📊 Project Overview
This project is an interactive Power BI dashboard designed to analyze sales performance across regions, products, salespersons, and time periods.

The dashboard tracks key business KPIs such as total sales, order completion, target achievement, regional performance, and month-over-month sales trends.

## 🛠 Tools & Technologies
- Power BI
- DAX
- Power Query
- Microsoft Excel
- Data Modeling

## 📈 Key KPIs
- Total Sales
- Total Orders
- Target Achievement %
- Completion Rate %
- Total Target
- Previous Month Sales
- Month-over-Month Growth %

## 🔍 Dashboard Features
- Interactive Year, Region, Category, and Status filters
- Regional Sales & Order Summary
- Sales performance by Region
- Sales performance by Salesperson
- Monthly Sales Trend
- Top 5 Products by Sales
- Sales vs Target comparison
- Current vs Previous Month Sales analysis
- Conditional formatting
- Dynamic report title based on Region selection

## 🧮 DAX Measures Used

```DAX
Total Sales =
SUM(SalesDataTable[Sales_Amount])

Total Orders =
COUNT(SalesDataTable[Order_ID])

Completion Rate % =
DIVIDE(
    [Completed Orders],
    [Total Orders]
)

Target Achievement % =
DIVIDE(
    [Total Sales],
    [Total Target]
)

Previous Month Sales =
CALCULATE(
    [Total Sales],
    PREVIOUSMONTH(DateTable[Date])
)

MoM Growth % =
DIVIDE(
    [Total Sales] - [Previous Month Sales],
    [Previous Month Sales]
)

