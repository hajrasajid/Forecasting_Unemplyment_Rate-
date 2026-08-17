# 📈 Unemployment Rate Forecasting Using ARIMA

> A practical **time-series forecasting project** using the **ARIMA (AutoRegressive Integrated Moving Average)** model to analyze historical unemployment rates and generate future forecasts.

---

## 🎯 Project Objective

The objective of this project is to analyze the historical **Unemployment Rate (%)**, establish stationarity, identify temporal patterns, develop and evaluate an ARIMA model, perform residual diagnostics, and forecast future unemployment rates.

---

## 🔄 Project Workflow

```text
Data Loading
     ↓
Data Exploration
     ↓
Missing Value Handling
     ↓
Trend Analysis
     ↓
ADF Stationarity Test
     ↓
Differencing
     ↓
ACF / PACF Analysis
     ↓
ARIMA Model Development
     ↓
Train-Test Evaluation
     ↓
Residual Diagnostics
     ↓
Future Forecasting
```

---

## 📊 1. Data Exploration

The dataset is initially explored to understand the distribution and characteristics of the unemployment rate.

### Analysis includes:

* Descriptive statistics
* Histogram with KDE
* Skewness
* Kurtosis
* Boxplot
* Time-series visualization

---

## 🧹 2. Data Preprocessing

Missing unemployment-rate observations are handled using **linear interpolation** to maintain continuity in the time series.

```python
df['Unemployment_Rate(%)'] = df['Unemployment_Rate(%)'].interpolate(method='linear')
```

---

## 📉 3. Stationarity Testing

The **Augmented Dickey-Fuller (ADF) test** is used to determine whether the unemployment-rate series is stationary.

If the original series is non-stationary, first-order differencing is applied:

```python
df['Unemployment_diff'] = df['Unemployment_Rate(%)'].diff()
```

The differenced series is then tested again using the ADF test.

---

## 🔍 4. ACF & PACF Analysis

**ACF (Autocorrelation Function)** and **PACF (Partial Autocorrelation Function)** are examined to understand the temporal dependency structure and identify suitable candidate values for the ARIMA parameters.

---

## 🤖 5. ARIMA Model

The selected model in this analysis is:

### `ARIMA(0,1,1)`

Where:

* **p = 0** → Autoregressive component
* **d = 1** → First-order differencing
* **q = 1** → Moving Average component

---

## 📏 6. Model Evaluation

An **80/20 train-test split** is used to evaluate the model.

### Evaluation Metrics

| Metric   | Purpose                                     |
| -------- | ------------------------------------------- |
| **RMSE** | Measures prediction error                   |
| **AIC**  | Evaluates model fit with complexity penalty |
| **BIC**  | Applies a stronger complexity penalty       |

Both training and testing RMSE are examined to assess model performance and generalization.

---

## 🧪 7. Residual Diagnostics

After fitting the model, residuals are analyzed to determine whether meaningful temporal structure remains unexplained.

### Diagnostic Checks

* ✅ Residual plot
* ✅ Residual ACF
* ✅ Ljung-Box test

The **Ljung-Box test** is used to check for significant autocorrelation in the residuals.

---

## 🔮 8. Forecasting

After model evaluation and residual diagnostics, the final ARIMA model is fitted to the complete dataset.

The model generates unemployment-rate forecasts for:

**📅 2026–2030**

along with **95% confidence intervals**.

---

## 📈 Forecast Visualization

The final visualization compares:

* Historical unemployment rates
* Forecasted unemployment rates
* 95% confidence intervals

This provides an intuitive view of the expected future trajectory and forecast uncertainty.

---

## 🛠️ Technologies & Libraries

* 🐍 Python
* 🐼 Pandas
* 🔢 NumPy
* 📊 Matplotlib
* 📉 Seaborn
* 🧪 SciPy
* 📐 Statsmodels
* 📏 Scikit-learn
* ☁️ Google Colab

---

## 💡 Key Takeaway

This project demonstrates that reliable time-series forecasting is not simply about fitting an ARIMA model. A complete workflow involves:

**Data Exploration → Stationarity → ACF/PACF → Model Evaluation → Residual Diagnostics → Forecasting**

The goal is to build a forecasting process that is **statistically evaluated, interpretable, and reproducible**.
