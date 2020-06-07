# Linear Regression with Multiple Variables
> 
> Total points 5
> 
>  1.Question 1
> 
> Suppose _m_=4 students have taken some class, and the class had a midterm exam and a final exam. You have collected a dataset of their scores on the two exams, which is as follows:
> 
> midterm exam(midterm exam)2^22final exam89792196725184749488368769476178
> 
> You'd like to use polynomial regression to predict a student's final exam score from their midterm exam score. Concretely, suppose you want to fit a model of the form hθ(x)=θ0+θ1x1+θ2x2h_\theta(x) = \theta_0 + \theta_1 x_1 + \theta_2 x_2hθ​(x)=θ0​+θ1​x1​+θ2​x2​, where x1x_1x1​ is the midterm score and x2x_2x2​ is (midterm score)2^22. Further, you plan to use both feature scaling (dividing by the "max-min", or range, of a feature) and mean normalization.
> 
> What is the normalized feature x1(3)x_1^{(3)}x1(3)​? (Hint: midterm = 94, final = 87 is training example 3.) Please round off your answer to two decimal places and enter in the text box below.
> 
> 1 point 
> 
>  2.Question 2
> 
> You run gradient descent for 15 iterations
> 
> with α=0.3\alpha = 0.3α=0.3 and compute
> 
> J(θ)J(\theta)J(θ) after each iteration. You find that the
> 
> value of J(θ)J(\theta)J(θ) **decreases slowly** and is still
> 
> decreasing after 15 iterations. Based on this, which of the
> 
> following conclusions seems most plausible?
> 
> 1 point 
> 
>  Rather than use the current value of α\alphaα, it'd be more promising to try a smaller value of α\alphaα (say α=0.1\alpha = 0.1α=0.1). 
> 

      Rather than use the current value of α\alphaα, it'd be more promising to try a larger value of α\alphaα (say α=1.0\alpha = 1.0α=1.0). 
> 
>  α=0.3\alpha = 0.3α=0.3 is an effective choice of learning rate. 
> 
>  3.Question 3
> 
> Suppose you have m=14m = 14m=14 training examples with n=3n = 3n=3 features (excluding the additional all-ones feature for the intercept term, which you should add). The normal equation is θ=(XTX)−1XTy\theta = (X^TX)^{-1}X^Tyθ=(XTX)−1XTy. For the given values of mmm and nnn, what are the dimensions of θ\thetaθ, XXX, and yyy in this equation?
> 
> 1 point 
> 
>  XXX is 14×414\times414×4, yyy is 14×414\times414×4, θ\thetaθ is 4×44\times44×4 
> 

      XXX is 14×414\times414×4, yyy is 14×114\times114×1, θ\thetaθ is 4×14\times14×1 
> 
>  XXX is 14×314\times314×3, yyy is 14×114\times114×1, θ\thetaθ is 3×33\times33×3 
> 
>  XXX is 14×314\times314×3, yyy is 14×114\times114×1, θ\thetaθ is 3×13\times13×1 
> 
>  4.Question 4
> 
> Suppose you have a dataset with m=50m = 50m=50 examples and n=15n = 15n=15 features for each example. You want to use multivariate linear regression to fit the parameters θ\thetaθ to our data. Should you prefer gradient descent or the normal equation?
> 
> 1 point 
> 

      Gradient descent, since (XTX)−1(X^TX)^{-1}(XTX)−1 will be very slow to compute in the normal equation. 
> 
>  The normal equation, since gradient descent might be unable to find the optimal θ\thetaθ. 
> 
>  Gradient descent, since it will always converge to the optimal θ\thetaθ. 
> 
>  The normal equation, since it provides an efficient way to directly find the solution. 
> 
>  5.Question 5
> 
> Which of the following are reasons for using feature scaling?
> 
> 1 point 
> 
>  It speeds up gradient descent by making each iteration of gradient descent less expensive to compute. 
> 
>  It is necessary to prevent the normal equation from getting stuck in local optima. 
> 
>  It prevents the matrix XTXX^TXXTX (used in the normal equation) from being non-invertable (singular/degenerate). 
> 

      It speeds up gradient descent by making it require fewer iterations to get to a good solution.
>
> -- https://www.coursera.org/learn/machine-learning/exam/7pytE/linear-regression-with-multiple-variables/attempt#Tunnel Vision Close
