
#  Demand Forecasting & Analysis for FMCG Retailer

## Project Overview

This project presents a **data science and forecasting solution** developed for a large offline **FMCG (Fast-Moving Consumer Goods)** retailer. The goal was to extract **business insights** from sales, product, and store data to guide **smarter inventory decisions** and reduce revenue loss.

By combining **exploratory data analysis (EDA)**, **statistical methods**, and a machine learning-based **demand forecasting model**, the system helps business planners understand trends, identify bottlenecks, and anticipate next week’s demand for better stock allocation.


## Business Problem

The retailer faced frequent **inventory misalignments**, leading to:

* Lost revenue from stockouts during high demand periods
* Overstocking, increasing storage and capital costs
* Poor alignment between demand, promotions, and resource planning

The goal: develop a solution that uses **data-driven forecasting and analysis** to guide weekly inventory replenishment and improve decision-making across store operations.


## Data Science Objective

Predict **weekly product demand** at the store-category level using historical data and uncover **patterns** that influence sales — such as promotions, seasonality, and pricing.

This insight helps:

* Reduce inventory waste
* Improve customer satisfaction
* Enable efficient workforce and shelf-space planning

##  Data Sources

The project integrates three key datasets:

* **Sales Data** – Weekly sales volume, discounts, pricing, promotions
* **Product Data** – Category, brand, size, UPC
* **Store Data** – Location, store type, and segment

➡All data was queried and joined using **SQL in BigQuery**, and processed in **Python via Colab** for analysis and modeling.


##  Project Workflow

The project follows the **CRISP-DM framework**, structured into the following phases:

### 1. Data Collection & Exploration

* Connected to **BigQuery** and extracted data using SQL
* Cleaned, merged, and reshaped datasets
* Performed **EDA** to identify seasonal patterns, promotion effects, and pricing trends
* Used statistics and visualizations to uncover category-level sales dynamics

### 2.  Predictive Modeling

* Engineered features such as:

  * **Lag values** (previous week’s sales)
  * **Rolling averages**
  * **Calendar effects** (week, month, etc.)
  * **Promotional flags**
* Trained an **XGBoost regressor** on the structured time-series dataset
* Evaluated performance using **RMSLE** — suitable for handling forecast errors in low-volume sales

### 3. Forecasting App (Streamlit)

* Built a **Streamlit dashboard**, hosted on **AWS EC2**, for end-user access
* Users can:

  * Select product categories
  * View predicted demand for the upcoming week
  * Compare recent performance across stores



## Model Prediction Visualization

Below is a visualization of the model's performance on historical sales data. It highlights how well the model captures weekly demand shifts across training, validation, and forecasted periods:

![Model Prediction](Model_Biulding/Model_evaluation/Model_prediction.png)



## Contact

Feel free to connect or collaborate:

* [LinkedIn](https://www.linkedin.com/in/hadeel-als)
* [Email](mailto:alsaadonhadeel@gmail.com)

