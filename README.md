
# Superstore Sales and Profit Analysis Dashboard

## 1. Data Upload and Cleaning
We started by **uploading the dataset** from a CSV file into Power BI. Using **Power Query**, we performed data cleaning, which included tasks like removing duplicates, fixing data types, and handling any missing values.

## 2. Data Modeling (Star Schema)
To optimize analysis, we restructured the dataset into a **star schema**:
- Derived **dimension tables** from the original dataset, such as:
  - `Product Dimension`
  - `Client Dimension`
  - `Region Dimension`
- Created a **fact table** holding the core transactional data (order information), linked to dimensions via foreign keys.
This star schema helps simplify queries and improve performance.

## 3. Defining Dashboard Purpose
The purpose of this dashboard is to **analyze sales and profit trends** over the years by **customer segments** and **product categories**. The key questions we aimed to answer are:
- What are the **total sales** and **net profit** over time?
- How do the sales and profit compare to the **previous year**?
- Which **products** and **segments** are the most profitable?
- What is the **profitability by category** and **segment**?

## 4. Measures Created with DAX
Several key measures were created using **DAX (Data Analysis Expressions)**:
- **Net Profit %**:  
  \`\`\`DAX
  Net Profit % = DIVIDE(SUM(orders[Profit]) - SUM(orders[Discount]), SUM(orders[Sales]), 0)
  \`\`\`
- **Net Profit $**:  
  \`\`\`DAX
  Net Profit $ = SUM(orders[Profit]) - SUM(orders[Discount])
  \`\`\`
- **Total Sales**:  
  \`\`\`DAX
  Total Sales = SUM(orders[Sales])
  \`\`\`
- **Sales Last Year (LY)**:  
  \`\`\`DAX
  Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
  \`\`\`
- **Percentage Difference from Previous Year (vs PY Sales)**:  
  \`\`\`DAX
  vs PY Sales = DIVIDE([Total Sales]-[Sales LY], [Sales LY])
  \`\`\`

These measures were applied to provide insights on profitability and year-over-year comparisons.

## 5. Interactivity and User Experience
- **Conditional Formatting**: **FX formulas** were applied to set predefined colors for highlighting values above or below certain conditions.
- **Filter Panel**: A **filter panel** was added, allowing users to filter the data by **category, segment, sub-category, shipping mode**, and **year**. The panel can expand and collapse as needed.

## Key Visuals:
- **Sales vs Previous Year over Time**: A line chart comparing total sales and last year’s sales.
- **Profit by Product**: A bar chart showing the most and least profitable products.
- **Net Profit by Segment**: A donut chart showing the contribution of each segment (Consumer, Corporate, Home Office) to total profit.
- **Sales and Net Profit by Category**: A comparison of net profit and total sales across categories like Technology, Office Supplies, and Furniture.

## Conclusion
This dashboard provides **quick and insightful analysis** of sales and profitability trends, allowing stakeholders to identify the most profitable products, segments, and categories. The **interactivity** and **conditional formatting** help highlight key insights and anomalies.

