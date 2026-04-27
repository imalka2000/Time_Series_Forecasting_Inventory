# 📈 Time Series Forecasting: Wikipedia Page Views Analysis

This notebook performs a comprehensive analysis of Wikipedia page view trends for Peyton Manning (2007-2016), leveraging descriptive statistics, time series decomposition, advanced forecasting techniques, and model evaluation metrics.

## Project Objectives

- Understand temporal patterns in page view data (trends, seasonality, volatility)
- Decompose time series into trend, seasonal, and residual components
- Build and compare multiple forecasting models (Moving Average, Exponential Smoothing, ARIMA)
- Evaluate model performance using MAE and MAPE metrics
- Generate actionable forecasts to support resource planning and content strategy

## Contents

1. Initial Setup & Library Imports
2. Data Loading & Cleaning
3. Exploratory Data Analysis (EDA)
4. Time Series Decomposition
5. Train-Test Split
6. Forecasting Models
   - Model 1: Simple Moving Average
   - Model 2: Exponential Smoothing (Holt-Winters)
   - Model 3: ARIMA
7. Model Performance Comparison
8. Final Forecast & Confidence Bands
9. Business Insights & Recommendations
10. Export Results

---

## 📊 Key Findings

### Data Characteristics

| Metric | Value |
|--------|-------|
| Time Period | December 2007 - January 2016 |
| Total Records | 2,905 daily observations |
| Monthly Aggregation | 98 months |
| Data Volatility | High (Coefficient of Variation: 96%) |

### Model Performance

| Model | MAE (Views) | MAPE |
|-------|-------------|------|
| Moving Average | 74,106 | 51.1% |
| ARIMA | 72,010 | 56.7% |
| Exponential Smoothing | 137,465 | 177.4% |

**🏆 Best Model: Moving Average (3-month window)**

> The Moving Average model performed best due to the dataset's high volatility and sudden event-driven spikes.

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

## 💡 Business Recommendations

### Server Capacity Planning
- Maintain 30% buffer above historical peak demand (237,300 concurrent capacity)

### Seasonal Resource Allocation
- **Football Season (Sept-Jan):** Increase capacity by 40%
- **Off-Season (Feb-Aug):** Maintain baseline levels

### Alert Triggers

| Traffic Level | Action |
|---------------|--------|
| Below 50,000 | Normal operations |
| 50,000 - 100,000 | Increase monitoring |
| 100,000 - 200,000 | Scale resources |
| Above 200,000 | Emergency protocols |

---

## 🛠️ Technologies Used

| Tool/Library | Purpose |
|--------------|---------|
| Python 3.12 | Core programming language |
| pandas | Data manipulation |
| NumPy | Numerical computing |
| Matplotlib / Seaborn | Data visualization |
| statsmodels | Time series modeling |
| scikit-learn | Performance metrics |
| Google Colab | Development environment |

---

## 📐 Statistical Techniques

| Technique | Purpose |
|-----------|---------|
| Time Series Decomposition | Separate trend, seasonality, residuals |
| Moving Average | Baseline model for volatile data |
| Holt-Winters Exponential Smoothing | Capture trend + seasonality |
| ARIMA | Capture autocorrelation patterns |
| Train-Test Split (80/20) | Model validation |
| MAE / MAPE | Error metrics |
| Confidence Bands (±20%) | Uncertainty quantification |

---
