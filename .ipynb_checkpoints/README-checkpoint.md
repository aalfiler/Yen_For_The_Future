# Time Series - A Yen for the Future

## Background

The financial departments of large companies often deal with foreign currency transactions while doing international business. As a result, they are always looking for anything that can help them better understand the future direction and risk of various currencies. Hedge funds, too, are keenly interested in anything that will give them a consistent edge in predicting currency movements.

This project aims to test time-series forecasting and linear regression modeling to predict future movements in the value of the Japanese yen versus the U.S. dollar.

## Part 1: Time-Series Forecasting

Use historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

## Part 2: Linear Regression Forecasting

Build a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

## Research Questions:
1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?
4. Using the results of the linear regression analysis and modeling, does the Scikit-Learn linear regression model perform better or worse on out-of-sample data compared to in-sample data?

### Files

[Time-Series](Analysis/time_series_analysis.ipynb)

[Linear Regression](Analysis/regression_analysis.ipynb)

[Yen Data CSV File](Data/yen.csv)



## Summary of Findings:

1.) Based on your time series analysis, would you buy the yen now?
- No, although the GARCH model indicates low volatility overall, additional testing is needed for the ARMA and ARIMA models before I'd invest in the yen now.

2.) Is the risk of the yen expected to increase or decrease? 
- Increase from the last day calculated in the dataset (2019-10-15)

3.) Based on the model evaluation, would you feel confident in using these models for trading?
- I do not feel confident using these models for trading. The p-value for both the ARMA and ARIMA models are quite high (>0.05) and thus not a good fit. 
- The GARCH model, on the other hand, has a low p-value (<0.05) and is a good fit to predict volatility of the yen. 

4.) Does the linear regression model perform better or worse on out-of-sample data compared to in-sample data?
- We should expect a higher out-of-sample RMSE, however, the out-of-sample (0.42) RMSE is lower than the in-sample (0.60) RMSE in this case. But the two values are close to each other and could suggest that the model is fairly stable.
