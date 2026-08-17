# 📈 Unemployment Rate Forecasting Using ARIMA

This project focuses on analyzing historical **unemployment rates** and forecasting future values using the **ARIMA (AutoRegressive Integrated Moving Average)** model.

Rather than directly fitting a forecasting model, the project follows a step-by-step time-series analysis workflow to understand the data first and then evaluate whether the model provides reliable forecasts.

## 🔍 What I Did

* 📊 Explored the unemployment rate using descriptive statistics, histograms, KDE, skewness, kurtosis, and boxplots.
* 🧹 Handled missing observations using **linear interpolation**.
* 📈 Visualized the unemployment rate over time to understand its historical behavior.
* 📐 Applied the **Augmented Dickey-Fuller (ADF) test** to check stationarity.
* 🔄 Used **first-order differencing** when the original series was non-stationary.
* 🔎 Examined **PACF** to understand the temporal dependency structure and support ARIMA parameter selection.
* 🤖 Developed an **ARIMA(0,1,1)** model.
* 📏 Evaluated the model using an **80/20 train-test split**, RMSE, AIC, and BIC.
* 🧪 Checked model residuals using residual plots, residual ACF, and the **Ljung-Box test**.
* 🔮 Used the final model to forecast the unemployment rate for **2026–2030**, including 95% confidence intervals.

## 🧠 Why ARIMA?

ARIMA is particularly useful for univariate time-series problems because it models the relationship between current observations and their previous values while using differencing to handle non-stationarity.

In this project, the main focus was not just on obtaining future predictions, but on following a complete workflow:

**Data Exploration → Stationarity Testing → Differencing → ACF/PACF → ARIMA → Evaluation → Residual Diagnostics → Forecasting**

## 🛠️ Tools Used

**Python | Pandas | NumPy | Matplotlib | Seaborn | SciPy | Statsmodels | Scikit-learn | Google Colab**

## 📌 Outcome

The project provides an end-to-end example of how statistical analysis and time-series modeling can be combined to produce an interpretable unemployment-rate forecast.

It also highlights an important principle in forecasting: **a model should be evaluated and diagnosed before its forecasts are trusted.**
