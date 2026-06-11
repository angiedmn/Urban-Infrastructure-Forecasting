# Urban-Infrastructure-Forecasting
# Urban Infrastructure Forecasting: Delhi 🏙️

## Project Overview
This repository contains a predictive analysis model developed to forecast **[Housing Prices / Energy Consumption / Traffic Congestion]** across various localities in the National Capital Territory of Delhi. 

By combining historical numerical data with spatial boundaries (shapefiles), this project aims to uncover geographical trends and provide actionable urban planning insights.

## Methodology & Evaluation
The project utilizes spatial data joins to map historical records to specific Delhi districts (e.g., South Delhi, Connaught Place). The predictive modeling pipeline tests baseline models (Linear Regression) against advanced gradient boosting algorithms (XGBoost).

Model performance is evaluated primarily using **Root Mean Squared Error (RMSE)** to penalize large prediction errors, and **$R^2$ (Coefficient of Determination)** to measure the variance explained by the spatial and historical features.

The cost function minimized during training is the Mean Squared Error:
$$ MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 $$

## Directory Structure
```text
├── data/
│   ├── raw/                 # Original CSVs and Delhi shapefiles
│   └── processed/           # Cleaned data ready for modeling
├── notebooks/
│   ├── 01_data_cleaning.ipynb     
│   ├── 02_spatial_eda.ipynb       # Exploratory Data Analysis & mapping
│   └── 03_model_training.ipynb    # Algorithm training and evaluation
├── src/
│   ├── data_loader.py       # Helper scripts for path management
│   └── model_utils.py       # Reusable training functions
├── app.py                   # Streamlit dashboard script
├── requirements.txt         # Project dependencies
└── README.md
