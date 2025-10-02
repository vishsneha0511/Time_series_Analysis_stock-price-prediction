# 📈 Time Series Analysis - Amazon Stock Price Prediction

This project focuses on forecasting **Amazon stock prices (2012–2024)** using time series techniques.  
It demonstrates exploratory data analysis, model selection, forecasting, and performance evaluation to predict stock prices accurately.

## 🔹 Project Overview
- **Dataset:** Amazon stock prices (2012–2024), monthly resampled.
- **Exploratory Data Analysis (EDA):**
  - Moving averages (3, 6, 12 months)
  - Trend and seasonal decomposition
  - Stationarity check using ADF test
- **Modeling:**
  - Grid search over ARIMA/SARIMA parameters
  - Best model: **SARIMA(2,1,2)(2,1,2,12)** with **AIC = 568.75**
  - Compared SARIMA forecasts with Holt-Winters Exponential Smoothing
- **Results:**
  - **SARIMA:** RMSE = 79.15, MAE = 75.57  
  - **Holt-Winters:** RMSE = 92.87, MAE = 91.14  
  → SARIMA provided higher forecasting accuracy

## 📊 Key Insights
- Stationarity is critical for accurate time series modeling.
- Seasonal patterns significantly impact forecasting performance.
- Model comparison validates SARIMA as the more reliable forecasting method.

## 🛠️ Tech Stack
- Python: Pandas, NumPy, Statsmodels, Matplotlib, Seaborn  
- Jupyter Notebook

## 📂 Dataset
The dataset was sourced from [Yahoo Finance](https://finance.yahoo.com/quote/AMZN/history).  
You can download it directly using **yfinance**:

```python
import yfinance as yf

# Download Amazon stock data (2012–2024)
df = yf.download("AMZN", start="2012-01-01", end="2024-01-01")

# Save to CSV
df.to_csv("data/amazon_stock.csv", index=True)




