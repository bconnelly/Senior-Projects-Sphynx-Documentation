Time Series Analysis
====================

Explanation:

Time Series (TS) Analysis is used to capture the data in the time frames. In this project, we use TS to forecast the tweet counts data and figure out the pattern of tweet counts daily. Data is collected hourly and graphed from Apr 11, 2016 to Apr 17, 2016. We use the technique of rolling mean and Dickey-Fuller Test (DFT) to test if TS is stationary. If TS are stationary, we can use the autoregressive integrated moving average (ARIMA) model to forecast the data.
We used Pandas to frame the datas. We used Statsmodels Python library to perform all statistical models and tests. 
In addition, we also used Matplotlib and Numpy.

Conclusion:

We performed this analysis in Tweets counts from April 11, 2016 to April 17, 2016 for all candidates. From the Dickey-Fuller test, all tweets time series are stationary. The test statistic number is much smaller than critical value 1%, there is about 99% confidence that the time series are stationary.

