# Retail Business Performance Dashboards (Global Superstore)/PowerBI
A Power BI dashboard analyzing global retail sales to identify top markets and product categories, supporting data-driven expansion and strategy. It covers the full pipeline: data transformation, relationship modeling, and interactive visualization in Microsoft Power BI Desktop.

<img width="1254" height="810" alt="image" src="https://github.com/user-attachments/assets/9a37fcf9-3b82-4b9c-a643-dcdd8c91570d" />

# Project Overview #

## 1. Background & Business Problem
**Business Context**

A global retail company operates across multiple international markets and product categories. As the business continues to expand, Senior Management needs a clear view of business performance to support market expansion and product strategy decisions.

**Senior Management wants to understand**

- How is the company's overall business performance?
- Which markets should receive further investment?
- Which product categories should be prioritized?
- Where should resources be reduced or optimized?

**The analysis focuses on**

- 7 Geographic Markets: LATAM, US, EU, APAC, EMEA, Africa, Canada
- 3 Product Categories: Technology, Furniture, Office Supplies
- 3 Business Tables: Orders, People, Returns
- Key Metrics: Revenue, Profit, Profit Margin, Orders, AOV, Return Rate, YoY Growth

## 2. Project Objective

- Analyze overall business performance using sales and profitability metrics.
- Compare market performance to identify expansion opportunities.
- Evaluate product category performance to support portfolio decisions.
- Monitor year-over-year business growth across different dimensions.
- Build an interactive multi-page dashboard for management reporting.

## 3. Dataset Overview

The project is built on the Global Superstore dataset, consisting of 1 fact table and 2 dimension tables.

- Orders (Fact Table): Stores sales transaction records.
- People (Dimension Table): Contains sales representative information by region.
- Returns (Dimension Table): Records returned orders for return analysis.

# Design Thinking Process #
## Step 1. Empathize ##
- 5W1H <img width="1486" height="728" alt="image" src="https://github.com/user-attachments/assets/3656a758-8d2e-4634-bf64-f2fd5b788019" />
- Empathy Map <img width="1484" height="844" alt="image" src="https://github.com/user-attachments/assets/d91b96e5-9096-4cb6-8657-97ddce6a2e27" />
- Stakeholder Journey Map <img width="1764" height="572" alt="image" src="https://github.com/user-attachments/assets/7426d94b-c5f7-4c46-bd81-51e29f96992a" />

## Step 2: Define Point of View ##
- North Star Metrics <img width="1492" height="626" alt="image" src="https://github.com/user-attachments/assets/ca4bcf8e-c48b-4896-82ba-5cdbac06afeb" />
- Define Point of View <img width="1468" height="624" alt="image" src="https://github.com/user-attachments/assets/a43682e2-d14a-4765-bda0-4624a9248dee" />
- Business Metrics Framework <img width="1480" height="600" alt="image" src="https://github.com/user-attachments/assets/162b0760-f61d-4e57-8add-afe4121bf4ed" />

## Step 3: Ideate ##
<img width="1494" height="696" alt="image" src="https://github.com/user-attachments/assets/054cb50b-3758-41d4-99f0-08a123f2be2e" />

## Stage 4: Prototype ##
<img width="1490" height="780" alt="image" src="https://github.com/user-attachments/assets/72281451-c103-40ef-b4d9-6d7c8935d563" />
<img width="1474" height="832" alt="image" src="https://github.com/user-attachments/assets/1e5d1889-c348-4d1b-86ea-e43a64f46cb5" />
<img width="1484" height="768" alt="image" src="https://github.com/user-attachments/assets/29c1245a-8230-418a-8cec-b8a9353ac36d" />
Note: The prototype was refined before implementation by prioritizing key KPIs, simplifying visual layouts, grouping related analyses into four pages (Overview, Market, Product, and Recommendation), and ensuring a clear navigation flow from business overview to actionable insights.

# Project Workflow #

## 1. Data Collection & Data Cleaning ##
The Global Superstore dataset was imported into Power BI and prepared using **Power Query**. Basic data validation was performed by verifying data types, reviewing missing values where necessary, checking for duplicate records, and ensuring data consistency before building the data model and dashboard.

## 2.Data Transformation ##
The dataset was transformed to improve analytical performance and support interactive reporting. This included separating the raw data into **fact and dimension tables**, creating reusable **DAX measures** for business KPIs, and building a **date hierarchy** for year-, quarter-, month-, and day-level analysis. These transformations provided a scalable foundation for data modeling and dashboard development.

## 3. Data Modeling ##
  A **Snowflake Schema** was designed to optimize reporting performance and simplify business analysis. The Fact_Orders table serves as the central fact table and is connected to multiple dimension tables, including Product, Customer, Date, Country, Region, People, Ship Mode, and Returns. This dimensional model improves query performance, reduces data redundancy, and provides a scalable foundation for interactive Power BI reporting.
<img width="1474" height="856" alt="image" src="https://github.com/user-attachments/assets/bc2dc65f-b05a-4cc0-95dc-41afc71b5ab1" />

## 4.Visualization Development & Insights ##
**Page 1 – Overview** <img width="1780" height="998" alt="image" src="https://github.com/user-attachments/assets/fdf12355-d508-4ceb-b002-b1ada85e1838" />

 The Overview page provides an executive summary of the company's overall performance, highlighting key KPIs, business trends, market distribution, customer segments, and operational efficiency.

Key Insights
- Business performance shows steady year-over-year revenue and profit growth.
- Technology is the leading category in both revenue and profitability.
- APAC, US, and EU are the primary revenue-generating markets.
- Standard Class is the most frequently used shipping method.
- Return Rate remains relatively stable and can be monitored over time for operational performance.

 **Page 2 – Market Analysis** <img width="1730" height="978" alt="image" src="https://github.com/user-attachments/assets/bb205c59-12d7-4b23-9b5f-ad72b7ca8e43" />

The Market page compares business performance across geographic markets to identify growth opportunities, profitability, customer distribution, and regional risks.

Key Insights
- LATAM generates the highest revenue, while profitability varies significantly across markets.
- Some smaller markets achieve relatively high profit margins despite lower sales.
- Revenue growth differs considerably between markets, highlighting expansion opportunities.
- Customer segment distribution varies across regions, suggesting different market characteristics.
- The detailed performance table supports market comparison using revenue, profit, margin, growth, AOV, and return rate.

**Page 3 – Product Analysis** <img width="1778" height="1004" alt="image" src="https://github.com/user-attachments/assets/523cb59d-8104-40ef-b803-2eca41491acf" />

The Product page evaluates category, subcategory, and product performance to identify strategic products, profitability, and potential improvement opportunities.

Key Insights
- Technology contributes the largest share of both revenue and profit.
- Several sub-categories generate high sales but relatively low profit margins.
- The Product Performance Matrix helps identify products with strong sales and profitability simultaneously.
- Return Rate varies across sub-categories, indicating products that require operational attention.
- The detailed product table supports further investigation into sales, profit, margin, AOV, and return performance.

## 5.Business Recommendations ##

<img width="1482" height="824" alt="image" src="https://github.com/user-attachments/assets/c04c794a-4c95-4e88-885b-a21ce4a86f80" />

This project demonstrates an end-to-end Business Intelligence workflow using Power BI, from understanding business requirements through the Design Thinking process to building a dimensional data model, developing interactive dashboards, and generating actionable business recommendations. The final solution enables decision-makers to monitor business performance, identify growth opportunities, and support strategic planning with data-driven insights.

