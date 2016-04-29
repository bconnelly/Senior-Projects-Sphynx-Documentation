Sentiment Analysis
==================

Explanation:

In order to get the results with the best accuracy, we found the top five people that tweeted the most about each candidate. Then, for each of these people's tweets, we ran the tweet text through a text processing api, located `here`_. We found this tool to be great, as if it cannot decide if the sentiment of the tweet is positive or negative, it classifies it as neutral. Thus, the majority of the tweets we processed were classified as neutral, leading to a closer, safe underestimate versus a potentially erronius one. 

.. _here: http://www.text-processing.com
Sentiment Analysis is used to classify tweets in either three categories: positive, negative, neutral or only two categories: positive and negative depend on the models. 
Our future plan is expanding this analysis to GDELT data and compare them to Tweets sentiment analysis. 
Two models we are using now is Word2Vec associated to Stochastic Gradient Descent Classification (W2V model) and text-processing API (API model). 
We use Gensim library (which is applying deep machine learning) to build the word trees and Stochastic Gradient Descent Method to classify datas. Our W2V model is training from 600,000 tweets that is manually labels from thinknood website. The accuracy is tested from 20% of datas is about 73%.  The disadvantage of this model is that there is no neutral label.. Some tweets is not clearly positive or negative. 
For API model, we write a python script to pass one by one tweets to their website and receive the results back. API model has neutral label. If the tweets cannot be defined clearly positive or negative, they are mostly labeled neutral. The disadvantage is we don’t know the accuracy of this model and there is a limitation of queries from their API. 
In addition, we also used Matplotlib and Numpy.

Conclusion:

We chose to run the models only for top 5 twitter users of each candidates since we can capture the characteristic of the tweets owners and somehow check the accuracy of the models. We can look at the ratio between positive and negative of each users to conclude if he support or anti the candidate. After performing sentiment analysis in top 5 twitter users for each candidates (except Donald Trump), we don’t see clearly the ratio differences between negative and positive for each candidates. The most interesting pattern we found is there are mostly positive from W2V model and positive neutral from API model for Bush although he dropped from the presidential race.  The rest of candidates’ tweets are mostly slipped equally between negative and positive.
To improve the performance of the W2V Model, we may need to manually our tweets for the training datas, Since for most of the training datas that we use from thinknood website is not presidential topics, there maybe has not enough informations for the model to label it correctly as we expected. We also can create neutral tag if we manually label tweets.
For API model, there are many tweets are labeled neutral, so if it is hard to tell clearly the ratio between negative and positive.

