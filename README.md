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


### Category 2:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 2]


### Category 3:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 3]


### Category 4:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 4]



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
