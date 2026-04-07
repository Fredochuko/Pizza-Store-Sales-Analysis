## Pizza Store Sales and Operations Analysis Using PowerBI
## Project Overview
This project analyses the sales, operational efficiency, and customer purchasing behaviour of a pizza restaurant using Power BI.
The objective of this analysis was to transform the raw transactional data into actionable business insights that support revenue growth, staffing optimization, menu performance improvement, and the overall growth of the restaurant.
The management has requested a single page centralized dashboard to help improve the restaurant daily operations and strategic decisions making.
## Business Executive Summary
This project analyzes pizza store operations using Power BI to identify peak sales periods, product performance, and operational efficiency opportunities. The dashboard provides actionable insights that can improve staffing decisions, increase Average Order Value, and reduce inventory waste.
## Dashboard Preview
<img width="611" height="345" alt="Pizza_Sales_ _Operation_Performance_Dashboard" src="https://github.com/user-attachments/assets/b57ec489-dd46-4de0-963f-0d0b3bd749c3" />

## Skills Demonstrated
1.  Data Cleaning and Transformation
2.  Data Modelling – Star Schema design and relationship management.
3.  DAX Calculations – KPI creation, aggregation measures, and time-based analysis.
4.  Business Intelligence – KPI definition and performance tracking.
5.  Data Visualization – Interactive dashboard design in Power BI.
6.  Business Analysis – Translating operational questions into analytical insights.
7.  Operational Analytics – Staffing, product performance, and capacity analysis.
8.  Dashboard Storytelling – Converting insights into management recommendations
## Tools Used
1.  Power Query Editor (Data Cleaning).
2.  Power BI (Data Modelling and Visualization).
3.  DAX (Business Calculations)'
4.  GitHub (Project Documentation)
## Business Problem
The restaurant collects transactional order data daily but has no visibility into:
1.  What days and times do we tend to be busiest?
2.  How many pizzas are made during peak periods?
3.  What are the best and worst selling pizzas?
4.  What is our average order value?
5.  How well are we utilizing seating capacity?
## Business Objectives
The objective was to answer key business questions by:
1.	Identify busiest days and hours.
2.	Measure operational capacity during rush periods.
3.	Analyse product performance.
4.	Evaluate revenue trends.
5.	Assess seating utilization efficiency.
## Dataset Description
The dataset contains transactional sales records including:
1.  Order Date and Time.
2.  Quantity.
3.  Pizza Size.
4.  Pizza Type.
5.  Price.
6.  Category
## Data Preparation / Cleaning Process
The following steps were performed:
1.  The fields were checked to ensure they were properly formatted.
2.  The field (column) headers were properly assigned.
3.  Duplicate records were checked for/removed where present.
4.  The fields were also verified for null values.
5.  A Calendar-Auto date table was created.
## Data Modelling
The dataset was modeled using a Star Schema to optimize performance and scalability.
## Fact Table
1.	order_details table.
## Dimension Tables
1.	orders table
2.	pizza_types table
3.	pizzas table and,
4.	date_table.

## Relationship
<img width="580" height="291" alt="Pizza Sales Model" src="https://github.com/user-attachments/assets/229d55d8-fce5-4e70-8204-b5dbe162039a" />

## Key DAX Function Created
1.  Total Revenue: This calculates total business income by aggregating transactional sales.
DAX: SUMX (order_details, order_details[quantity] * RELATED (pizzas[price]))
2.  Total Orders: This gives the total value of orders made taking into consideration individual unique orders.
DAX: DISTINCTCOUNT (orders[order_id])
3.  Average Order Value (AOV): This gives the average amount customers spend per pizza purchase/transaction.
DAX: DIVIDE ([total_revenue], [total_orders],0)
4.  Total Pizza Sold: This gives the overall count of pizza sold within a given period.
DAX: SUM (order_details[quantity])
5.  Peak Period Pizza: This shows the number of pizzas sold during peak hours.
DAX: CALCULATE ([total_pizza_sold], 'orders'[order_hours] IN {12,13,17,18}) 
## Analysis and Insights
## Busiest Times and Days
1.	The store experiences clear lunch (12:00noon – 13:00pm) and dinner (17:00pm – 18:00pm) rush periods with the highest orders recorded on Friday (over 3,500), followed by Thursday (over 3,200) and Saturday (over 3,150).
2.	This indicates that customers purchase pizzas as a full meal rather than as snacks to be eaten and mostly during the weekends.
3.	Pizzas sold during peak hours contribute over 40% of daily revenue. Increasing the numbers of staff during peak hours could reduce customer wait time and increase the number of pizzas ordered.

## Product Performance Analysis
1.	Total pizza sold during peak hours (highest selling hours) were 24,000 pieces, which represent 48% of pizzas made and were concentrated within four (4) peak hours.
2.	The best-selling pizzas were the “Classic Deluxe, Barbecue Chicken, Hawaiian, Pepperoni, and Thai Chicken pizzas”.
3.	The worst-selling pizzas were the “Soppressata, Spinach Supreme, Calabrese, Mediterranean, and Brie Carre pizzas”.
4.	Top 5 pizzas generate around 24.19% of total sales while the bottom 5 pizzas only contributed a mere 8.54% of the total sales.
5.	The Bottom-performing pizzas exhibit low turnover and may increase inventory waste.
## Revenue and Customer Spending Behaviour
1.	The total sales reveals that a small number of pizzas produce majority of total revenue, and weekend sales significantly outperforms weekdays.
2.	Average Order Value (AOV) reveals customer spending habits. Customers typically purchase two to three pizzas per order. Introducing combo deals and upsell strategies of pizzas on order can increase the AOV without inflating the price.
3.	The analysis of the total pizza by size shows that large pizza had the most sales. This allows the restaurant to understand customer preference and spending behaviour, and identifies the most profitable pizza size. This helps in guiding pricing strategy, promotion, and operational planning.
## Seating Utilization
1.	Seat utilization reaches 85 - 95% during lunch and dinner rush, but 7 - 30% in the morning. This indicates that the seating capacity is well utilized during the afternoon and evening sales and underutilized during morning sales.
## Business Recommendations
1.	Increase staffing during peak hours, this will help to cushion the effect of staff burnout and increase staff productivity and efficiency.
2.	Promote weekday lunch deals, and introduce pizza discounts to improve sales and seat utilization on weekdays.
3.	Remove or bundle consistently underperforming pizzas. This will help regulate costs or reduce losses.
4.	Implement upselling strategies to increase AOV. This can be done by adjusting prices for high-volume but low-profit pizzas and promote high-profit low-demand pizzas.
5.	Seat utilization trends should be monitored for expansion decisions.
## Business Impact
The analysis enables management to:
1.	Optimize staffing especially during lunch and dinner hours is expected to reduce waiting time by 20% and increase daily revenues.
2.	Upselling strategies will increase profitability of the store.
3.	Optimize staffing, removing or bundling of consistently underperforming pizzas from the menu will also improve operational efficiency.
4.	Removing or bundling consistently underperforming pizzas will reduce ingredient waste and increase inventory turnover.
5.	Optimizing seating capacity, upselling strategies, and increase number of staff especially during peak hours will enhance customer experience.
## Dashboard Features / Functionality
The dashboard was designed as a centralized operational monitoring tool featuring:
1.	KPI summary cards.
2.	Busiest times and days.
3.	Best/Worst selling pizza performance charts.
4.	Seat utilization gauge.
5.	Total pizza made by size.
## How to Reproduce this Project
1.	Download the dataset from the /data folder.
2.	Open the .pbix file in Power BI Desktop.
3.	Refresh the data model.
4.	Interact with slicers and filters.








## Author
Disi, Ogheneochuko Fredrick

Data Analyst | Business Intelligence Enthusiast
