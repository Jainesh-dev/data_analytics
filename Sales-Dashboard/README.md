# 📊 Sales Dashboard Project  

## Overview  
This project analyzes sales data using **SQL** and **Google Sheets** to generate insights on revenue, regional sales, product performance, and customer behavior.  

## Dataset  
A sample dataset `sample_sales.csv` was created with the following fields:  
- OrderID  
- Date  
- Region  
- Category  
- Product  
- Quantity  
- UnitPrice  
- Customer  

## SQL Analysis  
Some example queries:  
```sql
-- Total Sales Revenue
SELECT SUM(Quantity * UnitPrice) AS TotalRevenue FROM sales;

-- Top Selling Products
SELECT Product, SUM(Quantity) AS UnitsSold
FROM sales
GROUP BY Product
ORDER BY UnitsSold DESC
LIMIT 5;

