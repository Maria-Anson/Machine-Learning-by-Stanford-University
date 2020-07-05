# Error Analysis
> 
> The recommended approach to solving machine learning problems is to:
> 
> *   Start with a simple algorithm, implement it quickly, and test it early on your cross validation data.
> *   Plot learning curves to decide if more data, more features, etc. are likely to help.
> *   Manually examine the errors on examples in the cross validation set and try to spot a trend where most of the errors were made.
> 
> For example, assume that we have 500 emails and our algorithm misclassifies a 100 of them. We could manually analyze the 100 emails and categorize them based on what type of emails they are. We could then try to come up with new cues and features that would help us classify these 100 emails correctly. Hence, if most of our misclassified emails are those which try to steal passwords, then we could find some features that are particular to those emails and add them to our model. We could also see how classifying each word according to its root changes our error rate:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kky-ouM6EeacbA6ydECl3A_01b1fa64fcc9a7eb5da8e946f6a12636_Screenshot-2017-01-25-12.08.23.png?expiry=1594080000000&hmac=s06AL1MZRbUkELi1Gn6LLuZVq3FQbvU189uHA_VLYWQ)
> 
> It is very important to get error results as a single, numerical value. Otherwise it is difficult to assess your algorithm's performance. For example if we use stemming, which is the process of treating the same word with different forms (fail/failing/failed) as one word (fail), and get a 3% error rate instead of 5%, then we should definitely add it to our model. However, if we try to distinguish between upper case and lower case letters and end up getting a 3.2% error rate instead of 3%, then we should avoid using this new feature. Hence, we should try new things, get a numerical value for our error rate, and based on our result decide whether we want to keep the new feature or not.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/Z11RP/error-analysis#main
