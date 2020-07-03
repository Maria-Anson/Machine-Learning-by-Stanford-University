# Advice for Applying Machine Learning
> 
> Total points 5
> 
>  1.Question 1
> 
> You train a learning algorithm, and find that it has unacceptably high error on the test set. You plot the learning curve, and obtain the figure below. Is the algorithm suffering from high bias, high variance, or neither?
> 
> ![](http://spark-public.s3.amazonaws.com/ml/images/10.1-c.png)
> 
> 1 point 
> 
>  High bias 
> 

      High variance 
> 
>  Neither 
> 
>  2.Question 2
> 
> Suppose you have implemented regularized logistic regression
> 
> to classify what object is in an image (i.e., to do object
> 
> recognition). However, when you test your hypothesis on a new
> 
> set of images, you find that it makes unacceptably large
> 
> errors with its predictions on the new images. However, your
> 
> hypothesis performs **well** (has low error) on the
> 
> training set. Which of the following are promising steps to
> 
> take? Check all that apply.
> 
> 1 point 
> 
>  Try adding polynomial features. 
> 

      Try using a smaller set of features. 
> 

      Get more training examples. 
> 
>  Use fewer training examples. 
> 
>  3.Question 3
> 
> Suppose you have implemented regularized logistic regression
> 
> to predict what items customers will purchase on a web
> 
> shopping site. However, when you test your hypothesis on a new
> 
> set of customers, you find that it makes unacceptably large
> 
> errors in its predictions. Furthermore, the hypothesis
> 
> performs **poorly** on the training set. Which of the
> 
> following might be promising steps to take? Check all that
> 
> apply.
> 
> 1 point 
> 
>  Use fewer training examples. 
> 

      Try adding polynomial features. 
> 

      Try decreasing the regularization parameter λ\lambdaλ. 
> 
>  Try evaluating the hypothesis on a cross validation set rather than the test set. 
> 
>  4.Question 4
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 point 
> 
>  Suppose you are training a regularized linear regression model. The recommended way to choose what value of regularization parameter λ\lambdaλ to use is to choose the value of λ\lambdaλ which gives the lowest **test set** error. 
> 
>  Suppose you are training a regularized linear regression model.The recommended way to choose what value of regularization parameter λ\lambdaλ to use is to choose the value of λ\lambdaλ which gives the lowest **training set** error. 
> 

      The performance of a learning algorithm on the training set will typically be better than its performance on the test set. 
> 

      Suppose you are training a regularized linear regression model. The recommended way to choose what value of regularization parameter λ\lambdaλ to use is to choose the value of λ\lambdaλ which gives the lowest **cross validation** error. 
> 
>  5.Question 5
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 point 
> 
>  If a neural network has much lower training error than test error, then adding more layers will help bring the test error down because we can fit the test set better. 
> 

      A model with more parameters is more prone to overfitting and typically has higher variance. 
> 

      If a learning algorithm is suffering from high bias, only adding more training examples may **not** improve the test error significantly. 
> 

      When debugging learning algorithms, it is useful to plot a learning curve to understand if there is a high bias or high variance problem.
>
> -- https://www.coursera.org/learn/machine-learning/exam/w1FgU/advice-for-applying-machine-learning/attempt#Tunnel Vision Close
