# DataCo Global Supply Chain Analysis: Optimizing Delivery Performance and Demand Planning

# Project Background
This project analyzes the supply chain operations of DataCo Global, a multinational e-commerce company active in North America, South America, Europe, Africa, and Pacific-Asia. DataCo Global's business model connects customers with a wide range of products, including fitness equipment, apparel, electronics, and outdoor gear. The company serves over 30,000 unique customers with more than 10,000 different products. 

DataCo Global is facing significant challenges with delivery performance and demand forecasting, which affect customer satisfaction and operational efficiency. In the competitive e-commerce market, good supply chain management is crucial for delivering orders on time and meeting customer demand, but DataCo Global is struggling in both areas.

The supply chain team currently depends on ad-hoc daily and weekly reports. This has led to three main issues: inconsistent data sources that hinder demand planning, lack of real-time visibility into operations, and a consistently high late delivery rate that reached its peak in early 2017. By examining 180,519 orders across different shipping methods and market regions from January to September 2017, this project aims to provide data-driven insights to improve the shipping process and refine demand planning strategies.

Insights and recommendations are provided on the following key areas:

- **Shipping Performance Analysis:** Evaluation of on-time and late delivery rates for different shipping modes and time periods
- **Delivery Mode Efficiency:** A close look at the performance of First Class, Second Class, Same Day, and Standard Class shipping
- **Product Demand Patterns:** Analysis of revenue, profit, and order volumes for products, regions, and categories
- **Operational Metrics:** Review of delivery lead times, profit margins, and regional performance variations

The Python notebook used to clean and wrangle the data for this analysis can be found [here](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/1ac98501385ca31cb6243818f2fb5aaa8b599eed/Python%20Notebook/Supply_Chain_Dataset_Wrangling.ipynb).

Interactive Tableau dashboards used to monitor shipping performance and product demand can be found [here](https://public.tableau.com/views/SupplyChainDashboard_17694004638230/ShippingPerformance?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).



# Data Structure & Initial Checks

The dataset used in this analysis comes from the [DataCo Smart Supply Chain for Big Data Analysis](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis) available on Kaggle. The supply chain dataset consists of a single table with 180,519 order records from 2015 to 2018. This analysis focuses on January through September 2017 because of data completeness. The original dataset included 53 columns. After validating and cleaning the data, 32 columns were selected for analysis. The dataset captures the full order lifecycle from placement to delivery. There are no duplicate values or missing data. 

![Data Structure](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/f17e7abfad01c65fd690c10db7fafae8547e3e1d/Images/Data%20Structure.png)
<p align="center"><em>Dataset Structure showing the 32 columns organized by category</em></p>

Key data components:

- **Order Information:** Order ID, date, quantity, customer details, and product information
- **Shipping Details:** Shipping mode, scheduled vs actual shipping days, delivery status
- **Financial Metrics:** Order value, product price, profit per order, and discount information
- **Geographic Data:** Customer location, market region (North America, South America, Europe, Africa, Pacific-Asia)
- **Product Attributes:** Product name, category, department

The data wrangling process involved checking data types and quality issues, and ensuring the dataset was clean and ready for analysis in Tableau. There, calculated fields for important performance metrics, including late delivery rate, on-time delivery rate, late delivery period in days, total revenue, total profit, and profit margin were created.



# Executive Summary

### Overview of Findings

The supply chain analysis reveals critical performance issues that need immediate attention, along with noticeable patterns in product demand and profitability.

**Shipping Performance:** Delivery performance has worsened throughout 2017. Late deliveries increased from 53.61% in January to 54.23% by September. The analysis found major differences across shipping methods. First Class delivery has a 94.48% late delivery rate, even though it is the most profitable option. Same Day delivery has a strong 45.13% on-time rate, but it only makes up 5% of order volume. Standard Class, the most popular shipping method at 60% of orders, shows the best reliability with just a 37.82% late delivery rate.

**Product Demand and Financial Performance:** While delivery metrics fell, revenue and profit grew. Revenue went up from around 925K in January to 1.03M by September, and profit increased from 114.8K to 122.5K during the same time. The analysis showed that high order volume does not always lead to high profitability. For example, products like the Perfect Fitness Perfect Rip Deck ranked in the top 5 for demand, revenue, and profit, while other high-demand items had lower margins due to pricing strategies.

**Regional Variations:** South America accounts for 56% of total orders, but Europe leads in revenue per order at 175 USD compared to South America's 112 USD. North America, despite being the smallest market by volume, achieves the highest profit per order at 39 USD. This suggests that there are significant opportunities for targeted strategies in different regions.

These findings indicate opportunities for substantial improvement through careful reallocation of shipping resources, targeted process improvements, and region-specific product and pricing strategies.

![Dashboard Tab 1](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/a5693ac196deac1e75e900807431877fe4338930/Images/Dashboard%20Tab%201.png)
<p align="center"><em>Dashboard Tab 1: Shipping Performance - showing KPIs for late delivery rate, on-time delivery rate, and delivery trends</em></p>

![Dashboard Tab 2](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/a5693ac196deac1e75e900807431877fe4338930/Images/Dashboard%20Tab%202.png)
<p align="center"><em>Dashboard Tab 2: Product Demand - showing revenue, profit, and demand metrics across products and regions</em></p>



# Insights Deep Dive
### Shipping Performance Trends:

* **On-time delivery performance is declining.** The on-time delivery rate fell from 18.94% in January to 17.31% by September 2017. This 1.63 percentage point drop shows that delivery reliability is getting worse over time, suggesting ongoing problems in the fulfillment process.
  
* **Late delivery rates are rising throughout 2017.** Late deliveries went up from 53.61% in January to a high of 56.44% in August, finally settling at 54.23% in September. This trend is alarming because it affects more than half of all orders, which directly influences customer satisfaction and retention.
  
* **Q3 performance shows further deterioration.** The third quarter of 2017 had a late delivery rate of 55.15% and an on-time rate of only 17.27%. This is a 1.56% increase in late deliveries compared to Q2. The average late delivery period also rose from 0.54 days in Q2 to 0.58 days in Q3.

![Quarterly comparison of shipping performance](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/f42100e5d80b31c00a3d654f6f5d0cb02ac921d1/Images/Quarterly%20comparison%20of%20shipping%20performance.png)
<p align="center"><em>Quarterly comparison of shipping performance metrics across Q1, Q2, and Q3 2017</em></p>

* **Regional variations in delivery reliability exist.** North America leads with the highest on-time delivery rate at 24.58%. In contrast, Pacific-Asia has the highest late delivery rate at 55.68%. These regional differences suggest that delivery challenges may stem from geographic factors, the quality of infrastructure, or partnerships with carriers.

![Monthly trends showing delivery rate](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/573fbec43947f1cf4e7d8e7598e6b7f426c97976/Images/Monthly%20trends%20showing%20delivery%20rate.png)
<p align="center"><em>Monthly trends showing late delivery rate and on-time delivery rate from January to September 2017</em></p>

![Quarterly breakdown of on-time delivery rates](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/322bb98c649f2913b4cb8fb01a49faa9ff1ab658/Images/Quarterly%20breakdown%20of%20on-time%20delivery%20rates.png)
<p align="center"><em>Quarterly breakdown of on-time delivery rates by market region and shipping mode</em></p>


### Shipping Mode Analysis:

* **First Class delivery is critically underperforming.** It makes up 15% of all orders and is the most profitable shipping mode, yet it has a troubling 94.48% late delivery rate this year, with effectively 0% on-time deliveries. This situation indicates a major operational failure that could harm customer relationships and the brand's reputation.
  
* **Second Class shows moderate reliability issues.** It has a 75.82% late delivery rate and accounts for 19% of order volume. Second Class also has the longest median late delivery time at 2 days. Although this is not as bad as First Class, it still does not meet acceptable standards.
  
* **Same Day delivery shows strong performance but has low adoption.** It has the highest on-time rate at 45.13% and is the second most profitable option, but it only represents 5% of total orders. This indicates a big opportunity to improve customer value and profitability by increasing the use of Same Day shipping.
  
* **Standard Class is the most reliable for bulk volume.** It is the most popular choice, making up 60% of all orders. Standard Class has the lowest late delivery rate at 37.82% and a median late delivery period of 0 days, ranging from 2 days early to 2 days late. Its mix of reliability and popularity makes it the operational backbone of the delivery network.

![Year-to-date on-time delivery rates](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/6b6281b2c41c82c0634e4569911ed55dc17f0c46/Images/Year-to-date%20on-time%20delivery%20rates.png)
<p align="center"><em>Year-to-date on-time delivery rates by market region and shipping mode</em></p>

![Quarterly breakdown showing late delivery rates](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/87ecd435853cfb40d728f2c93bfd49e28ca20d10/Images/Quarterly%20breakdown%20showing%20late%20delivery%20rates.png)
<p align="center"><em>Quarterly breakdown showing late delivery rates across regions and shipping modes</em></p>

![Year-to-date late delivery rates](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/70385d5ffdee9e9b1af3eab5ff3cf666fc3a9e30/Images/Year-to-date%20late%20delivery%20rates.png)
<p align="center"><em>Year-to-date late delivery rates by market region and shipping mode</em></p>

![Distribution of late delivery periods](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/afecc4aec3169d8dee9efcc5d4121dc379be1b8b/Images/Distribution%20of%20late%20delivery%20periods.png)
<p align="center"><em>Distribution of late delivery periods showing histogram (overall) and box plots (by shipping mode)</em></p>


### Product Demand and Revenue Patterns:

* **Top performers show consistency across metrics.** Three products, Perfect Fitness Perfect Rip Deck, Nike Men's Dri-FIT Victory Golf Polo, and Nike Men's Free 5.0+ Running Shoe, ranked in the top 5 for demand, revenue, and profit at the same time. This consistency indicates a strong fit between the product and the market, along with optimized pricing.
  
* **High demand doesn't always mean high profitability.** Products like O'Brien Men's Neoprene Life Vest and Under Armour Girl's Toddler Surge Running Shoes had high order volumes but did not make it into the top 5 for revenue or profit due to lower price points and profit margins. This shows the need to balance volume and margins in product strategy.
  
* **Premium products drive significant revenue despite lower volume.** Field & Stream Sportsman 16 Gun Fire Safe and Diamondback Women's Serene Classic Comfort Bike did not rank in the top 5 for demand but achieved high revenue and profit through premium pricing and strong margins. This demonstrates the value of having a varied product portfolio.
  
* **Revenue and profit grew while margins stayed stable.** From January to September 2017, revenue increased from about 925K to 1.03M, while profit grew from 114.8K to 122.5K. Profit margins remained relatively stable, ranging between 11.51% and 13.32%, with the latest figure at 12.56% in September.

![Monthly revenue, profit, and profit margin trends](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/956eec53a8ab12011f45501fb13490a2a2929acc/Images/Monthly%20revenue%2C%20profit%2C%20and%20profit%20margin%20trends.png)
<p align="center"><em>Monthly revenue, profit, and profit margin trends from January to September 2017</em></p>

![Top 5 products ranked](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/3f1ee934212fc43c1a393171f9b0eb0984f54041/Images/Top%205%20products%20ranked.png)
<p align="center"><em>Top 5 products ranked by demand (products ordered), revenue, and profit</em></p>


### Regional and Market Performance:

* **South America leads in order volume.** The Latin America region accounts for 55,654 units ordered year-to-date, which is 56% of the total volume. This figure is much higher than Europe, which has 38,421 units, or 39%. However, this advantage in volume does not directly result in higher revenue because of differences in regional pricing and product mix.
  
* **Standard Class is the preferred shipping choice in all regions.** Standard Class delivery handles about 60% of all ordered products, totaling 59,818 units year-to-date. It is clearly the most popular shipping option. Following this are Second Class at 19%, which amounts to 19,222 units, First Class at 15%, with 14,961 units, and Same Day at only 5%, totaling 5,454 units. The strong preference for Standard Class shows that customers value cost-effectiveness and reliability more than speed.
  
* **Shipping mode preferences reflect affordability and reliability.** The way order volume is spread across shipping methods highlights customer priorities. The dominance of Standard Class indicates that most customers are willing to wait longer for delivery in exchange for lower costs and greater reliability, with a late delivery rate of 37.82%. The low usage of Same Day delivery, even though it has a high on-time rate of 45.13%, suggests limited availability, higher costs that discourage customers, or a lack of awareness about this option.
  
* **Europe tops in revenue per order.** European orders generate the highest median revenue at 175 USD per order, compared to just 112 USD for South American orders. This 56% difference in order value points to opportunities for pricing improvement and promoting premium products in high-performing regions.

* **North America shows the highest profitability per transaction.** Although it has the smallest market by volume, with only 266 units, North American orders generate the highest median profit at 39 USD per order, compared to 18 USD for South American orders. This suggests better margin management or a different customer segment willing to pay more.

* **Geographic expansion opportunities are available.** Africa, with 2,795 units, and Pacific-Asia, with 2,319 units, represent smaller markets that can grow, especially given their moderate performance metrics. These regions have on-time delivery rates of 22.42% and 19.46%, respectively, indicating they have the operational capability to support expansion.

![Quarterly breakdown of order volumes](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/68a7856b5a6229365cfe7ff459402663fefaf0c7/Images/Quarterly%20breakdown%20of%20order%20volumes.png)
<p align="center"><em>Quarterly breakdown of order volumes by market region and shipping mode</em></p>

![Year-to-date order volume distribution](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/95439d1ce4edb9aeb244a5cb974941a4dfc16d7b/Images/Year-to-date%20order%20volume%20distribution.png)
<p align="center"><em>Year-to-date order volume distribution across market regions and shipping modes</em></p>

![Box plots showing revenue and profit distributions](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/3f1a59e5dd10b3114f1498e66247bcf74be32cd8/Images/Box%20plots%20showing%20revenue%20and%20profit%20distributions.png)
<p align="center"><em>Box plots showing revenue and profit distributions by market region and shipping mode</em></p>



# Recommendations:

Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following: 

* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  
* Specific observation that is related to a recommended action. **Recommendation or general guidance based on this observation.**
  


# Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

* Assumption 1 (ex: missing country records were for customers based in the US, and were re-coded to be US citizens)
  
* Assumption 1 (ex: data for December 2021 was missing - this was imputed using a combination of historical trends and December 2020 data)
  
* Assumption 1 (ex: because 3% of the refund date column contained non-sensical dates, these were excluded from the analysis)
