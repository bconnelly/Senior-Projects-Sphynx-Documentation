Higher Order Regression
=======================

Explanation:

This method works very similarly to linear regression, but uses higher order polynomials to try to fit a curve to the data as opposed to a straight line. We used NumPy to generate the regression line and matplotlib to plot the line along with the data points. Like with linear regression, the data is split into 80% training data used to generate the model and 20% observational data used to check the accuracy of the model’s ability to predict future values

Conclusion:

It didn’t lead to any conclusions about our data, but we did learn about the limited usefulness of high order regression models. When the order is very high (more than 7 for 31 points), the line will pass straight through many of the data points in the training data but it will stray extremely far from the data between each data point. Using regression models of order 3 to 6 was less erratic, but each model has to be tailored to the data set. In one case an order 4 model may be the best fit, and another graph with the same number of points may be better described by an order 6 model. We didn’t use it for analysis in the end because of these challenges.
