# Machine Learning System Design
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> You are working on a spam classification system using regularized logistic regression. "Spam" is a positive class (y = 1) and "not spam" is the negative class (y = 0). You have trained your classifier and there are m = 1000 examples in the cross-validation set. The chart of predicted class vs. actual class is:
> 
> **Actual Class: 1****Actual Class: 0****Predicted Class: 1**85890**Predicted Class: 0**1510
> 
> For reference:
> 
> *   Accuracy = (true positives + true negatives) / (total examples)
> *   Precision = (true positives) / (true positives + false positives)
> *   Recall = (true positives) / (true positives + false negatives)
> *   F1F_1F1​ score = (2 * precision * recall) / (precision + recall)
> 
> What is the classifier's accuracy (as a value from 0 to 1)?
> 
> Enter your answer in the box below. If necessary, provide at least two values after the decimal point.
> 
> 1 / 1 point 
> 

     0.095
> 
> Check
> 
> Correct
> 
> The classifier correctly predicted the true positives and the true negatives = 85 + 10, so the accuracy is 95/1000 = 0.095
> 
>  2.Question 2
> 
> Suppose a massive dataset is available for training a learning algorithm. Training on a lot of data is likely to give good performance when two of the following conditions hold true.
> 
> Which are the two?
> 
> 1 / 1 point 
> 

      Our learning algorithm is able to represent fairly complex functions (for example, if we train a neural network or other model with a large number of parameters. 
> 
> Check
> 
> Correct
> 
> You should use a complex, "low bias" algorithm, as it will be able to make use of the large dataset provided. If the model is too simple, it will underfit the large training set.
> 
>  When we are willing to include high
> 
> order polynomial features of xxx (such as x12x_1^2x12​, x22x_2^2x22​,
> 
> x1x2x_1x_2x1​x2​, etc.). 
> 

      A human expert on the application domain can confidently predict yyy when given only the features xxx (or more generally, if we have some way to be confident that xxx contains sufficient information to predict yyy accurately). 
> 
> Check
> 
> Correct
> 
> It is important that the features contain sufficient information, as otherwise no amount of data can solve a learning problem in which the features do not contain enough information to make an accurate prediction.
> 
>  The classes are not too skewed. 
> 
>  3.Question 3
> 
> Suppose you have trained a logistic regression classifier which is outputing hθ(x)h_\theta(x)hθ​(x).
> 
> Currently, you predict 1 if hθ(x)≥thresholdh_\theta(x) \geq \text{threshold}hθ​(x)≥threshold, and predict 0 if hθ(x)<thresholdh_\theta(x) \lt \text{threshold}hθ​(x)<threshold, where currently the threshold is set to 0.5\.
> 
> Suppose you **decrease** the threshold to 0.3\. Which of the following are true? Check all that apply.
> 
> 1 / 1 point 
> 
>  The classifier is likely to have unchanged precision and recall, but
> 
> higher accuracy. 
> 

      The classifier is likely to now have lower precision. 
> 
> Check
> 
> Correct
> 
> Lowering the threshold means more y = 1 predictions. This will increase both true and false positives, so precision will decrease.
> 
>  The classifier is likely to now have lower recall. 
> 
>  The classifier is likely to have unchanged precision and recall, and
> 
> thus the same F1F_1F1​ score. 
> 
>  4.Question 4
> 
> Suppose you are working on a spam classifier, where spam
> 
> emails are positive examples (y=1y=1y=1) and non-spam emails are
> 
> negative examples (y=0y=0y=0). You have a training set of emails
> 
> in which 99% of the emails are non-spam and the other 1% is
> 
> spam. Which of the following statements are true? Check all
> 
> that apply.
> 
> 1 / 1 point 
> 

      If you always predict spam (output y=1y=1y=1), your classifier will have a recall of 100% and precision of 1%. 
> 
> Check
> 
> Correct
> 
> Since every prediction is y = 1, there are no false negatives, so recall is 100%. Furthermore, the precision will be the fraction of examples with are positive, which is 1%.
> 
>  If you always predict spam (output y=1y=1y=1),
> 
> your classifier will have a recall of 0% and precision
> 
> of 99%. 
> 

      If you always predict non-spam (output y=0y=0y=0), your classifier will have a recall of 0%. 
> 
> Check
> 
> Correct
> 
> Since every prediction is y = 0, there will be no true positives, so recall is 0%.

      If you always predict non-spam (output y=0y=0y=0), your classifier will have an accuracy of 99%. 
> 
> Check
> 
> Correct
> 
> Since 99% of the examples are y = 0, always predicting 0 gives an accuracy of 99%. Note, however, that this is not a good spam system, as you will never catch any spam.
> 
>  5.Question 5
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 / 1 point 
> 
>  After training a logistic regression
> 
> classifier, you **must** use 0.5 as your threshold
> 
> for predicting whether an example is positive or
> 
> negative. 
>

      The "error analysis" process of manually examining the examples which your algorithm got wrong can help suggest what are good steps to take (e.g., developing new features) to improve your algorithm's performance. 
> 
> Check
> 
> Correct
> 
> This process of error analysis is crucial in developing high performance learning systems, as the space of possible improvements to your system is very large, and it gives you direction about what to work on next.
> 
>  If your model is underfitting the
> 
> training set, then obtaining more data is likely to
> 
> help. 
> 
>  It is a good idea to spend a lot of time
> 
> collecting a **large** amount of data before building
> 
> your first version of a learning algorithm. 
> 

    Using a **very large** training set makes it unlikely for model to overfit the training data. 
> 
> Check
> 
> Correct
> 
> A sufficiently large training set will not be overfit, as the model cannot overfit some of the examples without doing poorly on the others.
>
> -- https://www.coursera.org/learn/machine-learning/exam/vrjOT/machine-learning-system-design/attempt?redirectToCover=true#Tunnel Vision Close
