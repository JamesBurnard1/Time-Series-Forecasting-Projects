This project explores time series analysis and forecasting techniques using real-world data. The goal is to fit and evaluate different models for univariate and multivariate time series forecasting and determine the best approach for predicting future values.

The project is divided into two main parts:

Time Series Modeling & Forecasting – Working with historical birth rate data in New York City, applying statistical methods to analyze trends, seasonality, and stationarity, and fitting forecasting models.
Linear Regression with Multivariate Time Series – Building a regression model to analyze and forecast personal consumption expenditure in relation to economic indicators.

Technologies & Libraries Used

R Programming – Data processing, visualization, and modeling
Libraries:
ggplot2 – Visualization
zoo – Handling missing data
forecast – Time series modeling
tseries – Stationarity tests (ADF, KPSS)
knitr – Table rendering
TTR – Time series transformation

Part 1: Exploring and Modeling Time Series

Dataset
NYC Birth Rate Data (1948-1959) – Monthly birth rate observations over 12 years.
Key Steps:
Data Processing: Handling missing values using interpolation (na.approx).
Time Series Visualization: Using ts() and autoplot() to explore trends and seasonality.
Stationarity Tests: Augmented Dickey-Fuller (ADF) and KPSS tests to determine if differencing is needed.
Modeling:

Baseline Models: Mean Forecast (meanf()), Seasonal Naïve Forecast (snaive()).
ETS (Error-Trend-Seasonal) Models: Holt-Winters (hw()).
ARIMA Models: Using auto.arima() for parameter selection.
Evaluation:
Splitting data into training (1948-1957) and test set (1958-1959).
Assessing performance with RMSE & MAE using accuracy().
Cross-validation with tsCV().

Part 2: Linear Regression and Multivariate Time Series

Dataset:
US Economic Indicators (1970-2016, Quarterly Data)
Includes variables: Consumption, Income, Production, Savings, and Unemployment.
Key Steps:
Data Preparation: Creating time series objects for each variable.
Stationarity Check: ADF and KPSS tests to ensure valid regression.
Modeling:

Simple Regression: Forecasting Consumption using Income as the sole predictor.
Multiple Regression: Including all economic indicators as predictors.
Evaluation:
Train-Test Split: 148 training observations, 39 test observations.
Residual Analysis: Checking for autocorrelation and normality.
Forecast Accuracy Comparison: RMSE & MAE for both models.

Findings & Takeaways

 ARIMA models outperformed benchmark models in univariate time series forecasting.
 Holt-Winters performed well for seasonal data but had minor autocorrelation issues.
 Multivariate regression provided better predictions for economic indicators compared to simple 
