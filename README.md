# About this Project

## Project Overview

**Title**: Superstore Sales and Profit Analysis  
**Period**: January 2011 - December 2014
**Link**: [Link](https://app.powerbi.com/view?r=eyJrIjoiZmNmYjRmM2QtMzc3MS00ZDM4LTk4NzAtY2E2NzBiMGI2NWJjIiwidCI6IjhiYjA1YjAwLTdmNDgtNDc4NS05NjgwLTkzYjgwYTM0NTVhNSJ9)


This project involved creating an interactive Power BI dashboard to analyze sales and profit trends for a Superstore across various segments, categories, and regions. A star schema model was designed in Power Query, comprising 4 dimension tables (`dimRegion`, `dimCustomers`, `dimShipping`, and `dimProducts`) and a central fact table (`FactOrders`). The dashboard enables stakeholders to track performance metrics and identify key drivers of profitability over time.
![image](https://github.com/user-attachments/assets/266c7a33-ce64-4e10-999c-e666ea89f080)


## Key Highlights

### Star Schema Design
- Created dimension tables for Region, Customers, Shipping, and Products, with a `FactOrders` table containing sales and transaction details.

### Dynamic KPIs
- Total Sales, Net Profit %, Total Customers, Orders, and Quantity Sold, with YoY and Prior Year comparisons.

### Sales and Profit Analysis
- Trends over time for total sales and profit.
- Breakdown of sales and net profit by Segment, Category, Shipping Mode, and Region.

### Performance Visualization
- Line charts for sales/profit trends and bar charts for segment-level comparisons.

## Tools Used
- **Power BI**: For data modeling, DAX measures, and visualization.
- **Power Query**: To transform and structure the dataset into a star schema for efficient analysis.

## Outcome (Interpretation of the Analysis)
From this analysis, it was evident that Technology products contributed the highest net profit, while Furniture had a lower profit margin despite high sales volume. Shipping modes also played a significant role, with Standard Class generating the most revenue but at the cost of lower profit margins. Regionally, the West was the strongest performer, while the South lagged in both sales and profitability. These insights suggest opportunities for optimizing operations by focusing on high-margin categories and exploring ways to boost sales in underperforming regions.

