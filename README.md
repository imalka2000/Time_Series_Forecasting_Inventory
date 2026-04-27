# 📈 Time Series Forecasting for Wikipedia Page Views

## Overview

This project implements a comprehensive time series analysis and forecasting pipeline to predict Wikipedia page view traffic for Peyton Manning (2007-2016). Using historical daily page view data, I built and compared three forecasting models to generate actionable 6-month predictions for resource planning and content strategy optimization.

**Dataset:** Peyton Manning Wikipedia page views (2007-2016) - 2,905 daily records with strong seasonal patterns and occasional event-driven spikes.

**Key components of the project include:**

- **Data Cleaning & Preparation**: Handling missing values, date gaps, and converting log-scale data to actual page views
- **Exploratory Data Analysis**: Visualizing trends, seasonality, and outliers in the traffic data
- **Time Series Decomposition**: Breaking down the series into trend, seasonal, and residual components
- **Forecasting Models**: Implementing and comparing Moving Average, Exponential Smoothing (Holt-Winters), and ARIMA models
- **Model Evaluation**: Using MAE (Mean Absolute Error) and MAPE (Mean Absolute Percentage Error) metrics
- **Business Recommendations**: Translating forecasts into actionable resource planning strategies

---

## 📊 Key Findings

### Data Characteristics
| Metric | Value |
|--------|-------|
| Time Period | December 2007 - January 2016 |
| Total Records | 2,905 daily observations |
| Monthly Aggregation | 98 months |
| Data Volatility | High (Coefficient of Variation: 96%) |

### Model Performance Comparison

| Model | MAE (Views) | MAPE | Best For |
|-------|-------------|------|----------|
| **Moving Average** | 74,106 | **51.1%** | Volatile data with sudden spikes |
| ARIMA | 72,010 | 56.7% | Data with autocorrelation patterns |
| Exponential Smoothing | 137,465 | 177.4% | Data with clear trend + seasonality |

**🏆 Best Model:** Moving Average (3-month window)

> *Why Moving Average won:* The dataset has high volatility and sudden spikes (e.g., news events about the quarterback). Simpler models often outperform complex ones on noisy, event-driven data.

### 6-Month Forecast (Feb 2016 - Jul 2016)

| Month | Forecasted Views | Lower Bound (80%) | Upper Bound (120%) |
|-------|-----------------|-------------------|-------------------|
| 2016-02 | 66,515 | 53,212 | 79,818 |
| 2016-03 | 66,515 | 53,212 | 79,818 |
| 2016-04 | 66,515 | 53,212 | 79,818 |
| 2016-05 | 66,515 | 53,212 | 79,818 |
| 2016-06 | 66,515 | 53,212 | 79,818 |
| 2016-07 | 66,515 | 53,212 | 79,818 |

**Total Projected Views (6 months):** 399,092 views

---

## 📈 Visualizations

### Daily Page Views (2007-2016)
![Daily Page Views](images/daily_views.png)
*Daily traffic showing clear spikes during football season and major news events*

### Time Series Decomposition
![Decomposition](images/decomposition.png)
*Breaking down the series into trend, seasonal, and residual components*

### Monthly Sales Pattern
![Monthly Views](images/monthly_views.png)
*Monthly aggregated views showing seasonal peaks and long-term decline*

### Model Performance Comparison
![Model Comparison](images/model_comparison.png)
*Comparing Moving Average, Exponential Smoothing, and ARIMA predictions against actual test data*

### 6-Month Forecast with Confidence Bands
![Forecast](images/forecast.png)
*Final forecast with 80-120% confidence bands for uncertainty quantification*

---

## 💡 Business Recommendations

Based on the forecast analysis, here are actionable recommendations for resource planning:

### 1. Server Capacity Planning
