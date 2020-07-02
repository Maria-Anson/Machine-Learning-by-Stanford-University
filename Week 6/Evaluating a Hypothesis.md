# Evaluating a Hypothesis
> 
> Once we have done some trouble shooting for errors in our predictions by:
> 
> *   Getting more training examples
> *   Trying smaller sets of features
> *   Trying additional features
> *   Trying polynomial features
> *   Increasing or decreasing λ
> 
> We can move on to evaluate our new hypothesis.
> 
> A hypothesis may have a low error for the training examples but still be inaccurate (because of overfitting). Thus, to evaluate a hypothesis, given a dataset of training examples, we can split up the data into two sets: a **training set** and a **test set**. Typically, the training set consists of 70 % of your data and the test set is the remaining 30 %.
> 
> The new procedure using these two sets is then:
> 
> 1.  Learn Θ\ThetaΘ and minimize Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) using the training set
> 2.  Compute the test set error Jtest(Θ)J_{test}(\Theta)Jtest​(Θ)
> 
> ## The test set error
> 
> 1.  For linear regression: Jtest(Θ)=12mtest∑i=1mtest(hΘ(xtest(i))−ytest(i))2J_{test}(\Theta) = \dfrac{1}{2m_{test}} \sum_{i=1}^{m_{test}}(h_\Theta(x^{(i)}_{test}) - y^{(i)}_{test})^2Jtest​(Θ)=2mtest​1​∑i=1mtest​​(hΘ​(xtest(i)​)−ytest(i)​)2
> 2.  For classification ~ Misclassification error (aka 0/1 misclassification error):
> 
> err(hΘ(x),y)=10if hΘ(x)≥0.5 and y=0 or hΘ(x)<0.5 and y=1otherwiseerr(h_\Theta(x),y) = \begin{matrix} 1 & \mbox{if } h_\Theta(x) \geq 0.5\ and\ y = 0\ or\ h_\Theta(x) < 0.5\ and\ y = 1\newline 0 & \mbox otherwise \end{matrix}
> 
> This gives us a binary 0 or 1 error result based on a misclassification. The average test error for the test set is:
> 
> Test Error=1mtest∑i=1mtesterr(hΘ(xtest(i)),ytest(i))\text{Test Error} = \dfrac{1}{m_{test}} \sum^{m_{test}}_{i=1} err(h_\Theta(x^{(i)}_{test}), y^{(i)}_{test})Test Error=mtest​1​∑i=1mtest​​err(hΘ​(xtest(i)​),ytest(i)​)
> 
> This gives us the proportion of the test data that was misclassified.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/aFpD3/evaluating-a-hypothesis#main
