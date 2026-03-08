# Retail-sales-dashboard
An interactive sales dashboard visualizing $25M in profit and 300K units sold, featuring deep dives into product categories, sales channels, and internal team metrics.


# 📊 Sales & Employee Performance Dashboard

## 📝 Project Overview
This repository contains a Business Intelligence dashboard showcasing overall sales performance, customer demographics, and internal employee metrics. The project demonstrates end-to-end data processing, from raw data cleaning and DAX measure creation to advanced visualization.

## 📂 Key Performance Indicators (KPIs)
The dashboard tracks several critical high-level business metrics:
* **Total Sales**: $71M
* **Total Profit**: $25M
* **Total Quantity**: 300K units
* **Profit Margin**: 35.56%
* **YoY Growth**: -83%
* **Sales LY (Last Year)**: $60.48M
* **Sales YTD (Year to Date)**: $10M

## 🧹 Data Cleaning & Transformation
To ensure accurate reporting, the dataset underwent structural transformations:
* **Product Categorization**: Standardized items into distinct categories such as Clothing, Accessories, Kitchen, Electronics, Outdoors, and Furniture.
* **Channel Normalization**: Cleaned sales channel data to accurately group transactions into Partner, Retail, Online, and Phone segments, which evenly split the revenue at roughly $18M each.
* **Employee Directory Mapping**: Parsed employee hire dates and mapped staff to specific organizational roles including Digital Marketing, Manager, Sales Rep, Support, and Warehouse.

## 🧮 DAX Measures (Data Analysis Expressions)
Custom DAX calculations were built to drive the interactive KPI cards and trend lines. Core measures include:

**1. Core Aggregations**
`Total Sales = SUM('SalesData'[Total_Sales])`
`Total Profit = SUM('SalesData'[Total_profit])`

**2. Profitability & Variance**
`Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)`
`YoY Growth = DIVIDE([Total Sales] - [Sales LY], [Sales LY], 0)`

## 📈 Dashboard Visualizations & Insights
The report is structured across multiple interactive views:

* **Executive Summary**: Line charts tracking `Total Sales by MonthName` to identify seasonal dips and peaks, alongside Donut charts breaking down revenue by sales channel.
* **Customer Demographics**: Bar charts revealing that the 'Bronze' Loyalty Tier generated the vast majority of revenue ($43M), followed by Silver ($17M), Gold ($7M), and Platinum ($4M). Gender distribution shows a balanced demographic split with Female customers accounting for $37M and Male customers $34M.
* **Product Profitability**: Matrix visuals and bar charts analyzing `Total Sales and Profit Margin by ProductName` (e.g., specific item codes like ACC-KEY-184 and ELE-LAP-027).
* **Global & Employee Tracking**: Geospatial maps plotting sales by Country and City, paired with stacked bar charts tracking `Total_Sales by Role` and individual `EmployeeName` performance.

---
**Tools Used**: Power BI, Power Query (M), DAX

```
