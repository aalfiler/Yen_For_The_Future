# Unit 10 | Time Series - A Yen for the Future

## Summary of the findings:

### Based on your time series analysis, would you buy the yen now?

- No, although the GARCH model indicates low volatility overall, additional testing is needed for the ARMA and ARIMA models before I'd invest in the yen now.

### Is the risk of the yen expected to increase or decrease? 

- Increase from the last day calculated in the dataset (2019-10-15)

### Based on the model evaluation, would you feel confident in using these models for trading?

- I do not feel confident using these models for trading. The p-value for both the ARMA and ARIMA models are quite high (>0.05) and thus not a good fit. 
- The GARCH model, on the other hand, has a low p-value (<0.05) and is a good fit to predict volatility of the yen. 

### Does the linear regression model perform better or worse on out-of-sample data compared to in-sample data?

- We should expect a higher out-of-sample RMSE, however, the out-of-sample (0.42) RMSE is lower than the in-sample (0.60) RMSE in this case. But the two values are close to each other and could suggest that the model is fairly stable.
