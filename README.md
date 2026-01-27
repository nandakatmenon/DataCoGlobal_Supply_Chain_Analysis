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

The dataset used in this analysis comes from the [DataCo Smart Supply Chain for Big Data Analysis available on Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis). The supply chain dataset consists of a single table with 180,519 order records from 2015 to 2018. This analysis focuses on January through September 2017 because of data completeness. The original dataset included 53 columns. After validating and cleaning the data, 32 columns were selected for analysis. The dataset captures the full order lifecycle from placement to delivery. There are no duplicate values or missing data. 

![Data Structure](https://github.com/nandakatmenon/DataCoGlobal_Supply_Chain_Analysis/blob/f17e7abfad01c65fd690c10db7fafae8547e3e1d/Images/Data%20Structure.png)



# Executive Summary

### Overview of Findings

Explain the overarching findings, trends, and themes in 2-3 sentences here. This section should address the question: "If a stakeholder were to take away 3 main insights from your project, what are the most important things they should know?" You can put yourself in the shoes of a specific stakeholder - for example, a marketing manager or finance director - to think creatively about this section.

[Visualization, including a graph of overall trends or snapshot of a dashboard]



# Insights Deep Dive
### Category 1:

* **Main insight 1.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 2.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 3.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.
  
* **Main insight 4.** More detail about the supporting analysis about this insight, including time frames, quantitative values, and observations about trends.

[Visualization specific to category 1]


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
