# Short-Term Electricity Demand Forecasting
This repository contains an end-to-end machine learning pipeline for a project that focuses on predicting the next hour's electricity demand for a national power grid using historical consumption patterns, environmental data, and macroeconomic indicators.
# Objective
The primary goal is to build a robust predictive model that forecasts grid demand at time t+1 using information available up to time t.
Accuracy is critical, as overestimation leads to financial losses, while underestimation threatens grid stability.
# Dataset Overview
The pipeline integrates three distinct data sources:
* PGCB Power Demand - Hourly historical demand and generation data (Target Variable: demand_mw).
* Weather Data - Hourly environmental factors such as temperature, humidity, precipitation etc.
* Economic Indicators - Annual macroeconomic data from the World Bank.
# Evaluation & Results
* Validation Strategy - A strict chronological hold-out test set (2025 data) was used to prevent data leakage from the future into the training process.
* Primary Metric - Mean Absolute Percentage Error (MAPE).
* Final Performance - The model achieved a MAPE of 2.97% on the unseen test set.
# Feature Importance
The visualization (included in the notebook) highlights the strongest drivers of future grid load. This confirms that the grid exhibits strong daily seasonality and short-term momentum.
# How to Run
* Clone the repository.
* Ensure you have the datasets (PGCB_date_power_demand.xlsx, weather_data.xlsx, economic_full_1.csv) in the root directory.
* Install required libraries (pandas, numpy, scikit-learn)
* Run the Jupyter Notebook: AI2.ipynb.
