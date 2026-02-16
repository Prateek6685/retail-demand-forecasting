# 🏪 Retail Demand Forecasting System

## 📌 Business Problem
A retail company wants to forecast daily product demand at the store level to optimize inventory planning and reduce stockouts.

This project benchmarks classical time series models against machine learning approaches to identify the most effective forecasting strategy.

---

## 📊 Dataset
Kaggle Competition Dataset:
**Store Sales – Time Series Forecasting (Corporación Favorita)**

- Multi-store
- Multi-product
- Daily sales data
- Promotional indicators included

---

## 🔎 Modeling Approach

### 1️⃣ Classical Time Series Models
- ARIMA
- SARIMA
- SARIMAX (with promotions as exogenous variable)

### 2️⃣ Machine Learning Model
- Random Forest Regressor
- Engineered features:
  - Lag_1 (recent dependency)
  - Lag_7 (weekly seasonality)
  - Lag_14
  - Rolling Mean (7-day)
  - Day of Week
  - Promotion count

---

## 📈 Model Performance (RMSE)

| Model         | RMSE |
|---------------|------|
| ARIMA         | 3212 |
| SARIMA        | 3245 |
| SARIMAX       | 3512 |
| Random Forest | 1700 |

Random Forest reduced forecasting error by nearly **47%** compared to the ARIMA baseline.

---

## 🧠 Key Insights

- Retail demand shows strong weekly seasonality.
- Recent sales trends are strong predictors of future demand.
- Classical statistical models struggle with nonlinear promotional spikes.
- Feature engineering significantly improves forecasting accuracy.

---

## 🚀 Business Impact

Accurate demand forecasting enables:
- Improved inventory allocation
- Reduced stockouts
- Better promotion planning
- More efficient supply chain decisions

---

## 🛠 Technologies Used

- Python
- Pandas
- Statsmodels
- Scikit-Learn
- Matplotlib

---

## 📌 Future Improvements

- Hyperparameter tuning
- XGBoost implementation
- Multi-store deployment pipeline
- Incorporating holiday and macroeconomic indicators
