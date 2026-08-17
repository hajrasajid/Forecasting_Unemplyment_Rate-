📈 Unemployment Rate Forecasting using ARIMA

This project applies a complete time-series forecasting workflow to analyze and forecast the unemployment rate using the ARIMA (AutoRegressive Integrated Moving Average) model.

The analysis covers:

📊 Data Exploration — descriptive statistics, distribution analysis, skewness, kurtosis, and boxplots
🧹 Data Preprocessing — handling missing observations using linear interpolation
📉 Trend Analysis — visualization of unemployment rate over time
📐 Stationarity Testing — Augmented Dickey-Fuller (ADF) test
🔄 Differencing — first-order differencing to achieve stationarity
🔍 ACF/PACF Analysis — identifying temporal dependencies and candidate ARIMA parameters
🤖 ARIMA Modeling — implementation of ARIMA(0,1,1)
📏 Model Evaluation — Train/Test RMSE, AIC, and BIC using an 80/20 split
🧪 Residual Diagnostics — residual plots, residual ACF, and Ljung-Box test
🔮 Forecasting — unemployment rate forecasts for 2026–2030 with 95% confidence intervals

Tools & Libraries: Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels, Scikit-learn

Key objective: Demonstrate how statistical analysis, model evaluation, and residual diagnostics can be combined to build a systematic and interpretable time-series forecasting workflow.
