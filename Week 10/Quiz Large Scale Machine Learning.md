# Large Scale Machine Learning
> 
> Total points 5
> 
>  1.Question 1
> 
> Suppose you are training a logistic regression classifier using stochastic gradient descent. You find that the cost (say, cost(θ,(x(i),y(i)))cost(\theta,(x^{(i)}, y^{(i)}))cost(θ,(x(i),y(i))), averaged over the last 500 examples), plotted as a function of the number of iterations, is slowly increasing over time. Which of the following changes are likely to help?
> 
> 1 point 
> 
>  This is not an issue, as we expect this to occur with stochastic gradient descent. 
> 

      Try using a smaller learning rate α\alphaα. 
> 
>  Try using a larger learning rate α\alphaα. 
> 
>  Try averaging the cost over a larger number of examples (say 1000 examples instead of 500) in the plot. 
> 
>  2.Question 2
> 
> Which of the following statements about stochastic gradient
> 
> descent are true? Check all that apply.
> 
> 1 point 
> 
>  Stochastic gradient descent is particularly well suited to problems with small training set sizes; in these problems, stochastic gradient descent is often preferred to batch gradient descent. 
> 
>  Suppose you are using stochastic gradient descent to train a linear regression classifier. The cost function J(θ)=12m∑i=1m(hθ(x(i))−y(i))2J(\theta) = \frac{1}{2m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2J(θ)=2m1​∑i=1m​(hθ​(x(i))−y(i))2 is guaranteed to decrease after every iteration of the stochastic gradient descent algorithm. 
> 

      One of the advantages of stochastic gradient descent is that it can start progress in improving the parameters θ\thetaθ after looking at just a single training example; in contrast, batch gradient descent needs to take a pass over the entire training set before it starts to make progress in improving the parameters' values. 
> 

      In each iteration of stochastic gradient descent, the algorithm needs to examine/use only one training example. 
> 
>  3.Question 3
> 
> Which of the following statements about online learning are true? Check all that apply.
> 
> 1 point 
> 

      Online learning algorithms are usually best suited to problems were we have a continuous/non-stop stream of data that we want to learn from. 
> 
>  Online learning algorithms are most appropriate when we have a fixed training set of size mmm that we want to train on. 
> 

      One of the advantages of online learning is that if the function we're modeling changes over time (such as if we are modeling the probability of users clicking on different URLs, and user tastes/preferences are changing over time), the online learning algorithm will automatically adapt to these changes. 
> 
>  When using online learning, you must save every new training example you get, as you will need to reuse past examples to re-train the model even after you get new training examples in the future. 
> 
>  4.Question 4
> 
> Assuming that you have a very large training set, which of the
> 
> following algorithms do you think can be parallelized using
> 
> map-reduce and splitting the training set across different
> 
> machines? Check all that apply.
> 
> 1 point 
> 
>  Logistic regression trained using stochastic gradient descent. 
> 

      Computing the average of all the features in your training set μ=1m∑i=1mx(i)\mu = \frac{1}{m} \sum_{i=1}^m x^{(i)}μ=m1​∑i=1m​x(i) (say in order to perform mean normalization). 
> 
>  Linear regression trained using stochastic gradient descent. 
> 

      Logistic regression trained using batch gradient descent. 
> 
>  5.Question 5
> 
> Which of the following statements about map-reduce are true? Check all that apply.
> 
> 1 point 
> 
>  If we run map-reduce using NNN computers, then we will always get at least an NNN-fold speedup compared to using 1 computer. 
> 

      Because of network latency and other overhead associated with map-reduce, if we run map-reduce using NNN computers, we might get less than an NNN-fold speedup compared to using 1 computer. 
> 

      If you have only 1 computer with 1 computing core, then map-reduce is unlikely to help. 
> 

      When using map-reduce with gradient descent, we usually use a single machine that accumulates the gradients from each of the map-reduce machines, in order to compute the parameter update for that iteration.
>
> -- https://www.coursera.org/learn/machine-learning/exam/rpoYY/large-scale-machine-learning/attempt#Tunnel Vision Close
