# Task-6-sales-queries
Task 6 - Sales Trend Analysis Using SQL

 📋 Objective
Analyze monthly revenue and order volume from an e-commerce sales dataset.

 🛠 Tools Used
- DB Browser for SQLite
- SQLite
- GitHub

 📁 Files Included
- `online_sales.csv`: Sales dataset
- `task6_queries.sql`: SQL script with queries for monthly trend analysis
- `screenshots/`: Screenshots of SQL query results
- `README.md`: 

 🔍 SQL Tasks Performed

 1. Monthly Revenue and Order Volume
```sql
SELECT 
    STRFTIME('%Y', order_date) AS year,
    STRFTIME('%m', order_date) AS month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS order_volume
FROM online_sales
GROUP BY year, month
ORDER BY year, month;
