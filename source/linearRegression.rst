Linear Regression
=================

Explanation:

Linear Regression generates a line that represents the trend in the data by minimizing the distance between the line and each point. 
We used Numpy to calculate the linear correlation.
We used Pandas to frame the datas. LinearRegression option from Scikit Learn is used for this analysis.
Each candidate has graphs comparing our sources via this regression model. 80% of the data was used to generate the model and the rest is there to see how good the prediction.
In addition, we also used Matplotlib and Numpy.

Conclusion:

In general there was very little correlation between our three data sources. Most of the correlation coefficients were between 0.3 and -0.3. This is particularly surprising in the case of comparing daily tweets to daily articles written, where intuitively one would expect a correlation. But in general this wasn’t the case. It could be that correlations would be easier to identify if the regression was applied on a larger data set; in our case, each graph has only 31 points of data because it was only used to analyze the month of March, 2016.
