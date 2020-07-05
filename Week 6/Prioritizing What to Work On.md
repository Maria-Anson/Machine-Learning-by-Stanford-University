# Prioritizing What to Work On
> 
> **System Design Example:**
> 
> Given a data set of emails, we could construct a vector for each email. Each entry in this vector represents a word. The vector normally contains 10,000 to 50,000 entries gathered by finding the most frequently used words in our data set. If a word is to be found in the email, we would assign its respective entry a 1, else if it is not found, that entry would be a 0\. Once we have all our x vectors ready, we train our algorithm and finally, we could use it to classify if an email is a spam or not.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Ys5NKOLJEeaPWBJZo44gSg_aba93cf4ce4507175d7e47ab5f9b7ce4_Screenshot-2017-01-24-22.29.45.png?expiry=1594080000000&hmac=nISP_97s3yJcR2TuWnlfX4kLH-12aCR__7egiDfwfds)
> 
> So how could you spend your time to improve the accuracy of this classifier?
> 
> *   Collect lots of data (for example "honeypot" project but doesn't always work)
> *   Develop sophisticated features (for example: using email header data in spam emails)
> *   Develop algorithms to process your input in different ways (recognizing misspellings in spam).
> 
> It is difficult to tell which of the options will be most helpful.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/0uu7a/prioritizing-what-to-work-on#main
