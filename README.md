
# 📈 Stock Price Movement Predictor using GRU/LSTM

This project builds a deep learning pipeline to **predict whether a stock's price will go up or down the next day** using historical price and volume data from Yahoo Finance. The model uses advanced time series feature engineering, recurrent neural networks (GRUs), regularization, and evaluation techniques to approach a production-grade alpha signal in quantitative finance.

---

## 🚀 Features

- ✅ Yahoo Finance data ingestion
- ✅ Robust Scaling
- ✅ Lag features (Close_lag1, Volume_lag3, etc.)
- ✅ Rolling statistics (MA7, MA30, rolling std, etc.)
- ✅ Technical indicators (MACD, RSI, Bollinger Bands)
- ✅ Derived features (returns, volatility, volume shocks)
- ✅ Categorical labeling for up/down movement
- ✅ Sequence construction for LSTM/GRU
- ✅ Model built using Bidirectional GRUs
- ✅ Regularization via Dropout, ElasticNet (L1 + L2)
- ✅ Class imbalance handling using class weights
- ✅ Evaluation using precision, recall, F1-score

---

## 📌 Key Sections

### 1. 📥 Data Collection
- Downloaded day-wise stock OHLCV data from Yahoo Finance

### 2. 🧮 Feature Engineering
- Lag features: `Close_lag1`, `Volume_lag3`, etc.
- Rolling window stats: `MA_7`, `Rolling_std_10`, etc.
- Technical indicators: `MACD`, `RSI`, `Bollinger Bands`
- Derived metrics: daily returns, momentum, volatility
- Volume-based metrics: shocks, VWAP

### 3. 📏 Normalization
- Robust-Scaling

### 4. 🔁 Sequence Construction
- 30-day rolling window → predict 31st day's movement (1/0)

### 5. 🧠 Model Architecture
- Bidirectional GRUs
- Dropout + BatchNormalization
- ElasticNet regularization
- Final dense sigmoid output for binary classification

### 6. 🧪 Advanced Tricks
- Class balancing & weighted loss

### 7. 📊 Evaluation
- Classification report (precision, recall, F1)
- Accuracy on training vs validation
- Plotting loss/accuracy curves
- Plotting the confidence curve

---


## 🛠 Requirements

Install dependencies via:

```bash
pip install -r requirements.txt
