Clustering Analysis
===================

Explanation:

We applied K-Means clustering technique to classify the candidates into three clusters based on their Twitters, GDELT, and Polls data. We used Pandas to frame the datas. K-means clustering option from Scikit Learn is used for this analysis. Since k-means is so sensitive to the number of clusters and the initial k-centroids, we alway pick three clusters to classify 5 candidates and use ‘k-means++’ mode as initial guesses option (selects initial cluster centers for k-mean clustering in a smart way to speed up convergence) to keep the consistency. In addition, we also used Matplotlib and Numpy.


Conclusion:

Trump is almost always placed in his own cluster which isn’t surprising considering he generally gets more media coverage than the other candidates and is considered very controversial by the general public. The rest of the candidates vary in which is clustered with which. Cruz and Clinton are in the same cluster more often than the rest, which makes sense because they get similar amounts of media coverage.
