# 🚀 Cryptocurrency Liquidity Prediction for Market Stability

This project uses machine learning to predict the liquidity levels of cryptocurrencies based on various market signals like price, trading volume, and volatility. Liquidity prediction helps traders and platforms manage risk more effectively in volatile crypto markets.

---

## 📌 Problem Statement

Cryptocurrency markets are highly volatile. Predicting liquidity levels early can help reduce sudden crashes and ensure smooth trading. This project aims to:

- Predict crypto liquidity ratios
- Visualize trends in market activity
- Build an interactive prediction tool

---

## 📁 Dataset

- Source: [CoinGecko API & Downloads]
- Data: Historical price, % change, volume, and market cap
- Files Used: `coin_gecko_2022-03-16.csv`, `coin_gecko_2022-03-17.csv`

---

## 🧪 Data Processing

- Handled missing values using forward fill
- Min-Max scaling for numerical consistency
- Engineered new features:
  - Moving Averages (3-day, 7-day)
  - Price Volatility (rolling std dev)
  - Liquidity Ratio = Volume / Market Cap

---

## 🤖 Model

- **Model Used**: RandomForestRegressor (Scikit-Learn)
- **Tuning**: GridSearchCV for best hyperparameters
- **Metrics**:
  - R² Score ≈ 0.89
  - MAE ≈ 0.0142
  - RMSE ≈ 0.0265

---

## 🖥️ Deployment

Built an interactive prediction tool using **Streamlit**:

### Run Locally:

```bash
pip install -r requirements.txt
streamlit run app.py
