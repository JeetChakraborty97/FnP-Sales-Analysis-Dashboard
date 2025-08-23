# This GitHub repository contains the following files:  

FnP Dashboard Project.xlsx - The main Excel dashboard file

customers.csv, orders.csv, products.csv - The three source datasets

Ferns and Petals Sales Analysis Problem Statement.pdf - Project requirements document

Ferns and Petals Sales Analysis Dashboard Screenshot.png - Visual preview of the dashboard

FnP Sales Analysis Dashboard - Complete Analysis of Key Processes and Methods.pdf

Executive Summary -  Ferns and Petals Sales Analysis Dashboard.pdf

# FOR EASE OF LOOKING, THE CONTENT OF THE LAST 2 ITEMS HAVE BEEN PROVIDED BELOW👇


# FnP-Sales-Analysis-Dashboard

📊 Executive Summary: Ferns and Petals Sales Analysis Dashboard
🎯 Objective

The project analyzes Ferns & Petals’ 2023 sales data with the goal of uncovering insights on revenue, customer behavior, product performance, and seasonal demand patterns. The dashboard addresses ten key business questions outlined in the problem statement
 to guide strategic decisions on product promotion, customer engagement, and operational efficiency.

🔑 Key Insights
1. Overall Revenue & Performance

Total Revenue exceeded expectations with strong order volumes during festival seasons and Valentine’s week.

Customer Spending: The average order value is around ₹3,500, highlighting customers’ willingness to spend for special occasions.

Delivery Efficiency: Average delivery time is ~5–6 days, but larger orders tend to experience delays, indicating scope for logistics optimization.

2. Monthly Sales Trends

Sales peaked in February (Valentine’s Day), contributing the highest monthly revenue.

Other strong months: August (Raksha Bandhan), October–November (Diwali), and December (Christmas/New Year gifting).

Slower months such as April–June suggest opportunities for off-season promotional campaigns.

3. Product Performance

Top Revenue Generators include premium items such as cakes, flower bouquets, and gift hampers.

Product categories like plants and soft toys performed moderately but show growth potential during personalized gifting occasions.

Top 5 Products consistently contributed a significant share of revenue, justifying focused marketing on these items.

4. Customer & City Analysis

Top 10 Cities (e.g., Delhi, Mumbai, Bangalore, Hyderabad, Pune) accounted for the majority of orders, reflecting strong metro demand.

Tier-2 cities like Indore, Lucknow, and Chandigarh also showed rising adoption, suggesting a growing market outside metros.

High-value customers (spending above average) are largely concentrated in urban centers.

5. Occasion-Based Insights

Valentine’s Day generated the highest revenue, dominated by flowers, cakes, and personalized gifts.

Diwali & Raksha Bandhan drove strong demand for sweets, hampers, and home décor items.

Birthdays & Anniversaries contributed steady year-round revenue, ensuring business stability beyond festival peaks.

6. Operational Insights

Order Quantity vs. Delivery Time: Larger orders correlated with slightly delayed deliveries, stressing the need for supply chain improvements.

Delivery timelines during festive rush periods were longer, suggesting a need for seasonal staffing and better logistics partnerships.

📌 Strategic Recommendations

Boost Seasonal Campaigns: Double down on marketing around Valentine’s, Diwali, and Raksha Bandhan while creating attractive offers for lean months.

Product Mix Optimization: Continue promoting best-sellers (cakes, flowers, hampers) while expanding personalization in categories like plants and soft toys.

Customer Segmentation: Focus loyalty programs on high-value urban customers while tailoring discounts for Tier-2 growth cities.

Logistics Efficiency: Reduce delivery delays by partnering with additional couriers and implementing demand forecasting for festive surges.

Cross-Selling & Upselling: Encourage higher spending by bundling products (e.g., flowers + chocolates, plants + personalized notes).

Occasion-Specific Marketing: Curate collections for each major festival/occasion to match product popularity trends.

🏆 Business Impact

By implementing the insights from this dashboard:

FNP can increase customer retention through better delivery and personalized offers.

Strategic targeting of high-revenue occasions can boost annual revenue significantly.

Expanding into Tier-2 and Tier-3 cities can unlock untapped growth markets.

Operational improvements in logistics and inventory planning will ensure higher customer satisfaction and repeat purchases.


# FnP Sales Analysis Dashboard: Complete Analysis of Key 

Processes and Methods:

Core Data Processing Methods: 

1. Power Query for Data Extraction and Transformation 

Data Extraction: 

• Folder-based data loading: Used Power Query's "Get Data > From Folder" feature to extract data from multiple CSV files simultaneously. 

• Transform approach: Selected "Transform" instead of "Combine" to maintain separate table structures before processing. 

• Query creation: Right-clicked on each binary file to create separate queries for customers, orders, and products tables. 

Data Cleaning and Transformation: 

• Column removal: Eliminated unnecessary description column from products table. 

• Data type conversion: Changed contact numbers to text format to preserve special characters like '+' symbols. 

• Column profiling: Utilized Power Query's data profiling features to check for distinct/unique values, errors, and empty values. 

• Date/time extraction: 

o Extracted month names from order dates using "Add Column > Month > Name of 
Month".  

o Extracted hours from order time and delivery time using "Add Column > Time > Hour".  

• Custom calculations: Created delivery difference column by calculating "Delivery Date - Order Date" and converting duration to days format. 

Data Integration: 

• Merge Queries (Joins): Performed left outer join between orders and products tables using Product ID as the common key. 

• Selective column expansion: Expanded only the price column from the merged products table to avoid data redundancy. 

2. Power Pivot for Data Modeling 

Setup and Configuration: 

• Add-in activation: Enabled Power Pivot through File > Options > Customize Ribbon > Developer > COM Add-ins. 

• Data model creation: Used "Close and Load To" option to load data as tables and add to data model. 

Relationship Management: 

• Star schema implementation: Created a star schema with orders as the fact table and customers/products as dimension tables. 

• Relationship establishment: 

o One-to-many relationship between customers and orders via Customer ID. 

o One-to-many relationship between products and orders via Product ID. 

Advanced Calculations: 

• Revenue calculation: Created new column in Power Pivot Data View: Revenue = [Price] * [Quantity].  

• DAX functions implementation: Used FORMAT([Order Date], "DDDD") to extract day names from order dates. 

3. Pivot Tables for Data Analysis 

Core Analysis Functions: 

• Multi-table data access: Created pivot tables from data model to combine information from multiple tables. 

• Aggregation methods: Used sum, average, and count functions for different metrics. 

• Custom sorting: Implemented chronological month sorting instead of alphabetical ordering. 

• Top N filtering: Applied top 5 filters for product revenue analysis using "Value Filters > Top 10".  

Business Intelligence Measures: 

• Total Revenue: Sum of revenue across all transactions (₹35,02,984).  

• Average Order Value: Average customer spending (₹3,520).  

• Average Delivery Time: Mean days between order and delivery (5.5 days).  

• Monthly Sales Performance: Revenue breakdown by month with November showing highest sales. 

• Top Products Analysis: Identification of highest revenue-generating products. 

• Geographic Analysis: Top 10 cities by order volume. 

• Occasion-based Revenue: Revenue comparison across different occasions (Valentine's Day, Diwali, etc.).  

4. Statistical Analysis Methods 

Correlation Analysis: 

• Excel CORREL function: Used to analyze relationship between order quantity and delivery time. 

• Data interpretation: Identified that larger orders tend to have slightly longer delivery times. 

5. Dashboard Creation and Visualization 

Chart Development: 

• Multiple chart types: Created bar charts for categorical data and line charts for trend analysis. 

• Chart formatting: 

o Removed field buttons and legends for cleaner appearance. 

o Added meaningful titles like "Revenue by Occasions".  

o Adjusted X-axis labels to prevent overcrowding. 

Interactive Elements: 

• Slicers: Added occasion-based slicers for dynamic filtering across multiple charts. 

• Timeline controls: Implemented date range filters for order and delivery dates. 

• Report connections: Linked slicers to relevant pivot tables for synchronized filtering. 

Dashboard Design: 

• KPI cards: Created visual measures displaying total orders, total revenue, average delivery time, and average customer spending. 

• Theme application: Used Excel's Page Layout themes for consistent color schemes. 

• Layout optimization: Arranged charts and measures for optimal visual impact. 

# Technical Skills Demonstrated 

Power Query Expertise: 

• ETL (Extract, Transform, Load) processes. 

• Data profiling and quality assessment. 

• Advanced transformations and custom column creation. 

• Query merging and relationship building. 

Power Pivot Mastery: 

• Data modeling and schema design. 

• DAX function implementation. 

• Relationship management. 

• Advanced calculated columns. 

Pivot Table Proficiency: 

• Multi-dimensional analysis. 

• Custom aggregations and filtering. 

• Dynamic reporting capabilities. 

• Business intelligence metrics creation. 

Dashboard Development: 

• Interactive visualization design. 

• User experience optimization. 

• Professional presentation formatting. 

• Integration of multiple data visualization techniques. 
