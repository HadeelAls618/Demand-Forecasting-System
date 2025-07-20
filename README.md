# Demand Forecasting System for FMCG Retailer

## Project Overview

This project presents demand forecasting system developed for a large offline **FMCG (Fast Moving Consumer Goods)** retailer. Using machine learning techniques and historical sales data, the system predicts weekly product demand to optimize inventory levels, reduce waste, and prevent lost sales.

Built following best practices in data engineering, machine learning, and MLOps, the solution includes data ingestion, feature engineering, model training, and an interactive Streamlit app hosted on AWS.


## Business Problem

The retailer struggled with **inventory imbalances**—either ordering too much or too little stock across product categories. This led to:

* **Lost sales** from stockouts during periods of high demand
* **Excess storage costs** due to unsold inventory
* **Poor resource planning** that impacted profitability and customer satisfaction

To address these issues, the business needed a system that could **accurately forecast product demand** on a weekly basis, enabling smarter replenishment strategies and reducing waste across the supply chain.


## ML Problem

Accurately forecast **weekly product demand** at the store level using historical sales, promotional activity, and store characteristics. The model must account for seasonality, pricing, and category-level trends to support smarter stock planning.


## Data Sources

To build a comprehensive modeling pipeline, we integrated the following datasets:

- **Product Data**: SKU, category, brand, size  
- **Sales Data**: Weekly sales units, prices, promotions  
- **Store Data**: Location, size, and segmentation details

> All data was joined and processed using **SQL in Google BigQuery**, enabling a unified time-series dataset for modeling.


## Project Methodology

The forecasting system was developed following the **CRISP-DM** framework and structured into five stages:


### 1. Data Pipeline

- Connected to BigQuery using SQL and Python (via Google Colab)  
- Cleaned and merged product, store, and sales datasets  
- Performed exploratory analysis to identify patterns and outliers  
- Created time-series features such as **lags**, **rolling means**, and **promotional flags**

### 2. Modeling Pipeline

- Trained an **XGBoost regression model** for demand forecasting  
- Target: weekly demand at the product-store level  
- Features: lag-based variables, pricing data, temporal effects  
- Evaluation: **RMSLE (Root Mean Squared Log Error)** to penalize large relative errors

### 3. Deployment & App Interface

- Built an **interactive Streamlit web application**, deployed on **AWS EC2**  
- Users can select product categories and stores to view real-time demand forecasts  
- Designed for usability by planners and business stakeholders
  
###  Model Prediction Visualization

The chart below illustrates the model’s ability to forecast product demand over time. It shows:

This visualization helps stakeholders evaluate how well the model captures real-world demand fluctuations.

![Model Prediction](Model_Biulding/Model_evaluation/Model_prediction.png)

## Contact

If you have any questions or would like to collaborate, feel free to reach out!

-  [LinkedIn](https://www.linkedin.com/in/hadeel-als)  
-  [alsaadonhadeel@gmail.com](mailto:alsaadonhadeel@gmail.com)
