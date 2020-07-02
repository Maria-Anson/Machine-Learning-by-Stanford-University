# Model Selection and Train/Validation/Test Sets
> 
> Just because a learning algorithm fits a training set well, that does not mean it is a good hypothesis. It could over fit and as a result your predictions on the test set would be poor. The error of your hypothesis as measured on the data set with which you trained the parameters will be lower than the error on any other data set.
> 
> Given many models with different polynomial degrees, we can use a systematic approach to identify the 'best' function. In order to choose the model of your hypothesis, you can test each degree of polynomial and look at the error result.
> 
> One way to break down our dataset into the three sets is:
> 
> *   Training set: 60%
> *   Cross validation set: 20%
> *   Test set: 20%
> 
> We can now calculate three separate error values for the three different sets using the following method:
> 
> 1.  Optimize the parameters in Θ using the training set for each polynomial degree.
> 2.  Find the polynomial degree d with the least error using the cross validation set.
> 3.  Estimate the generalization error using the test set with Jtest(Θ(d))J_{test}(\Theta^{(d)})Jtest​(Θ(d)), (d = theta from polynomial with lower error);
> 
> This way, the degree of the polynomial d has not been trained using the test set.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/XHQqO/model-selection-and-train-validation-test-sets#main
