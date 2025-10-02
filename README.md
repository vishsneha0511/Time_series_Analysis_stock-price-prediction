# Time_series_Analysis_stock-price-prediction
Time Series Analysis of Amazon Stock Prices (2012–2024) using SARIMA and Holt-Winters forecasting models. Includes EDA, seasonal decomposition, model selection, and performance comparison.


## 📂 Dataset

The dataset used in this project consists of **Amazon (AMZN) historical stock prices from 2012 to 2024**.  
It was obtained from [Yahoo Finance](https://finance.yahoo.com/quote/AMZN/history).

You can download the dataset directly using the Python library **yfinance**:

```python
import yfinance as yf

# Download Amazon stock data (2012–2024)
df = yf.download("AMZN", start="2012-01-01", end="2024-01-01")

# Save to CSV
df.to_csv("amazon_stock.csv", index=True)

---



