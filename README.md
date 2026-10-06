# RFM-customer-segmentation
RFM customer segmentation analysis using Python and Power BI
Overview
This project performs RFM (Recency, Frequency, Monetary) analysis on an e-commerce 
transaction dataset to segment customers based on their purchasing behavior, and 
visualizes the results in an interactive Power BI dashboard.

 Dataset
- ~34,500 e-commerce transaction records (Sept 2023 - Sept 2025)
- Columns: order_id, customer_id, product_id, category, price, discount, quantity, 
  payment_method, order_date, delivery_time_days, region, returned, total_amount, 
  shipping_cost, profit_margin, customer_age, customer_gender

 Approach
1. Data Cleaning** (Python/Pandas): Converted dates to proper datetime format, 
   checked for missing values, and removed returned orders (34,500 → 32,597 valid transactions)
2. RFM Calculation**: Computed Recency (days since last order), Frequency (distinct 
   order count), and Monetary (total spend) per customer — resulting in 7,877 unique customers
3. Scoring & Segmentation**: Scored each metric into quartiles (1-4) and classified 
   customers into 8 segments: Champions, Loyal Customers, At Risk, Lost, Needs Attention, 
   Cant Lose Them, New/Promising, Others
4. Visualization** (Power BI): Built an interactive dashboard with segment distribution, 
   revenue-by-segment, and a Recency vs Frequency scatter plot

 Key Insight
Champions represent only 23% of customers (1,826 of 7,877) but generated the largest 
share of total revenue (₹23.5L of ₹54.8L)** — highlighting the value of retention-focused 
marketing over broad, undifferentiated campaigns.

 Tools Used
Python (Pandas), Power BI

Recommendation
Focus retention efforts (loyalty programs, personalized offers) on Champions and Loyal 
Customers, while running win-back campaigns for the "Cant Lose Them" segment — high-value 
customers who've gone quiet.

