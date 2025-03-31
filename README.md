# AtliQ Hardware Excel-Project

## 📌 Project Description
This project analyzes customer and market performance data for AtliQ Hardwares across multiple years (2019-2021). It provides insights into sales trends, customer growth, and revenue distribution across different stores and platforms.

### Sales Analysis:
This report evaluates customer net sales growth (2019–2021) and customer sales performance (2019 -2021) to identify high-value customers, sales trends, and growth opportunities.

### Objective:
- __Tracks year-over-year (YoY) net sales per customer.__ 

- __Highlights % growth (21 vs. 20) to assess performance.__

- __Identifies top-growing and declining customers.__

**Business Impact :** Helps optimize sales strategy by focusing on high-value customers, re-engaging declining ones, tailoring marketing efforts based on purchase behavior, and forecasting future sales trends to optimize pricing

### Finance Analysis:
This report evaluates market-wise sales trends (2019–2021) and compares actual sales with 2021 targets to assess performance and growth potential.

### Objective:
- __Tracks YoY market sales and % achievement vs. target.__

- __Identifies high-performing vs. underperforming markets.__

- __Highlights sales trends for strategic planning__

**Business Impact :** Helps allocate resources to high-growth markets, improve weak ones, assess performance gaps, refine sales targets, predict market trends, and optimize expansion plans.

### P & L Market Analysis:
This report analyzes market-wise profitability for fiscal years 2019, 2020 and 2021 by evaluating net sales, cost of goods sold (COGS), and gross margin % to assess financial performance.

### Objective
- __Tracks sales, costs, and profitability across different markets.__

- __Highlights gross margin % to identify high and low-profit markets.__

- __Helps optimize pricing and cost strategies for better profitability.__

**Business Impact :** Focuses on profit optimization by prioritizing high-margin markets, reducing costs in low-margin ones, adjusting pricing strategies, and investing in markets with strong financial performance.

___ 

###  🚀 Key Features

✅ Sales Growth Analysis - Compares yearly revenue changes and trends.

✅ Top Customer Insights - Identifies high-revenue customers like Amazon & Flipkart.

✅ Market Trends - Highlights growing and declining customer segments.

✅ Power BI Dashboard - Visual representation of key customer metrics.

✅ SQL Queries - Ready-to-use SQL scripts for deeper data exploration.

___


## 🛠 Installation  

#### **Clone the Repository**

Install my project, run: 

git clone https://github.com/Swagata-j07/AtliQ_Hardware.git

#### 📂 Dataset  
This project includes sales data for analysis. Download the dataset:  

[Customer Data (CSV)](https://github.com/Swagata-j07/AtliQ_Hardware/blob/main/dim_customer.csv)

[Market Data (CSV)](https://github.com/Swagata-j07/AtliQ_Hardware/blob/main/dim_market.csv)

[Products Data (CSV)](https://github.com/Swagata-j07/AtliQ_Hardware/blob/main/dim_product.csv)

[Fact_sals_monthly (CSV)](https://github.com/Swagata-j07/AtliQ_Hardware/blob/main/fact_sales_monthly.csv.gz)

***

## 📊 Data Analysis Approach  
- **Performed analysis using Excel**, leveraging formulas and pivot tables.
  + Excel Formulas & Methods Used
    * SUM() – Aggregated total net sales and costs.  
    - Division & Subtraction – Calculated percentage growth and profit margins.  
    + Pivot Tables – Summarized and analyzed market-wise performance trends.    
- **Generated insights for business stakeholders** to optimize sales and profitability.  

***

## Key Insights

 ✔ Amazon had the highest net sales in 2021 at $82.1M, with a 218.9% YoY growth—indicating it as the most valuable customer, followed by AtliQ Eclusive with $61.1M, securing second highest revenue-generator.
 
 ✔ Key Growth Drivers: Such a significant increase could be due to bulk orders, stronger partnerships, improved demand, or strategic pricing adjustments.
 
 ✔ Consistent sales growth across customers highlights strong customer retention and opportunities to expand premium offerings.
 
 ✔ India ($161.3M) and the USA ($87.8M) led in total sales, but target gaps (-$9.6M and -$10.2M, respectively) indicate areas for sales strategy improvement.
 
 ✔ In P & L Month Report, total net sales grew from $87.5M (2019) to $598.9M (2021) with (204.5% increase), showing strong business growth.

 ✔ Despite sales growth, gross margin % declined (-2.3%), signaling a need to optimize costs and adjust pricing strategies.


## Usage

1️⃣ Open the Power BI dashboard (Customer_Performance.pbix), (Market_Performance.pbix).
2️⃣ Apply filters to analyze trends in customer sales, market performance, and profitability.
3️⃣ Use SQL queries to extract key insights:
```
-- Calculate YoY growth for each customer
sql
   SELECT customer_name, (sales_2021 - sales_2020) / sales_2020 * 100 AS YoY_growth
     FROM customer_performance
       WHERE sales_2020 > 0
         ORDER BY YoY_growth DESC;

