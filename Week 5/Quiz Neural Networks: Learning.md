# Neural Networks: Learning
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> You are training a three layer neural network and would like to use backpropagation to compute the gradient of the cost function. In the backpropagation algorithm, one of the steps is to update
> 
> Δij(2):=Δij(2)+δi(3)∗(a(2))j\Delta^{(2)}_{ij} := \Delta^{(2)}_{ij} + \delta^{(3)}_i * (a^{(2)})_jΔij(2)​:=Δij(2)​+δi(3)​∗(a(2))j​
> 
> for every i,ji, ji,j. Which of the following is a correct vectorization of this step?
> 
> 1 / 1 point 
> 

      Δ(2):=Δ(2)+δ(3)∗(a(2))T\Delta^{(2)} := \Delta^{(2)} + \delta^{(3)} * (a^{(2)})^TΔ(2):=Δ(2)+δ(3)∗(a(2))T 
> 
>  Δ(2):=Δ(2)+(a(3))T∗δ(3)\Delta^{(2)} := \Delta^{(2)} + (a^{(3)})^T * \delta^{(3)}Δ(2):=Δ(2)+(a(3))T∗δ(3) 
> 
>  Δ(2):=Δ(2)+δ(3)∗(a(3))T\Delta^{(2)} := \Delta^{(2)} + \delta^{(3)} * (a^{(3)})^TΔ(2):=Δ(2)+δ(3)∗(a(3))T 
> 
>  Δ(2):=Δ(2)+δ(2)∗(a(2))T\Delta^{(2)} := \Delta^{(2)} + \delta^{(2)} * (a^{(2)})^TΔ(2):=Δ(2)+δ(2)∗(a(2))T 
> 
> Check
> 
> Correct
> 
> This version is correct, as it takes the "outer product" of the two vectors δ(3)\delta^{(3)}δ(3) and a(2)a^{(2)}a(2) which is a matrix such that the (i,j)(i,j)(i,j)-th entry is δi(3)∗(a(2))j\delta^{(3)}_i * (a^{(2)})_jδi(3)​∗(a(2))j​ as desired.
> 
>  2.Question 2
> 
> Suppose Theta1\tt{Theta1}Theta1 is a 5x3 matrix, and Theta2\tt{Theta2}Theta2 is a 4x6 matrix. You set thetaVec=[Theta1(:);Theta2(:)]\tt{thetaVec = [Theta1(:) ; Theta2(:)]}thetaVec=[Theta1(:);Theta2(:)]. Which of the following correctly recovers Theta2\tt{Theta2}Theta2?
> 
> 1 / 1 point 
> 

      reshape(thetaVec(16:39),4,6)\tt{reshape(thetaVec(16:39), 4, 6)}reshape(thetaVec(16:39),4,6) 
> 
>  reshape(thetaVec(15:38),4,6)\tt{reshape(thetaVec(15:38), 4, 6)}reshape(thetaVec(15:38),4,6) 
> 
>  reshape(thetaVec(16:24),4,6)\tt{reshape(thetaVec(16:24), 4, 6)}reshape(thetaVec(16:24),4,6) 
> 
>  reshape(thetaVec(15:39),4,6)\tt{reshape(thetaVec(15:39), 4, 6)}reshape(thetaVec(15:39),4,6) 
> 
>  reshape(thetaVec(16:39),6,4)\tt{reshape(thetaVec(16:39), 6, 4)}reshape(thetaVec(16:39),6,4) 
> 
> Check
> 
> Correct
> 
> This choice is correct, since Theta1\tt{Theta1}Theta1 has 15 elements, so Theta2\tt{Theta2}Theta2 begins at index 16 and ends at index 16 + 24 - 1 = 39.
> 
>  3.Question 3
> 
> Let J(θ)=3θ3+2J(\theta) = 3 \theta^3 + 2J(θ)=3θ3+2. Let θ=1\theta=1θ=1, and ϵ=0.01\epsilon = 0.01ϵ=0.01. Use the formula J(θ+ϵ)−J(θ−ϵ)2ϵ\frac{J(\theta + \epsilon) - J(\theta - \epsilon)}{2\epsilon}2ϵJ(θ+ϵ)−J(θ−ϵ)​ to numerically compute an approximation to the derivative at θ=1\theta=1θ=1. What value do you get? (When θ=1\theta = 1θ=1, the true/exact derivative is dJ(θ)dθ=9\frac{dJ(\theta)}{d\theta} = 9dθdJ(θ)​=9.)
> 
> 1 / 1 point 
> 
>  11 
> 
>  9 
> 

      9.0003 
> 
>  8.9997 
> 
> Check
> 
> Correct
> 
> We compute (3(1.01)3+2)−(3(0.99)3+2)2(0.01)=9.0003\frac{(3(1.01)^3 + 2) - (3(0.99)^3 + 2)}{2(0.01)} = 9.00032(0.01)(3(1.01)3+2)−(3(0.99)3+2)​=9.0003.
> 
>  4.Question 4
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 / 1 point 
> 
>  Using a large value of λ\lambdaλ cannot hurt the performance of your neural network; the only reason we do not set λ\lambdaλ to be too large is to avoid numerical problems. 
> 
>  Gradient checking is useful if we are using gradient descent as our optimization algorithm. However, it serves little purpose if we are using one of the advanced optimization methods (such as in fminunc). 
> 

      If our neural network overfits the training set, one reasonable step to take is to increase the regularization parameter λ\lambdaλ. 
> 
> Check
> 
> Correct
> 
> Just as with logistic regression, a large value of λ\lambdaλ will penalize large parameter values, thereby reducing the changes of overfitting the training set.
> 

      Using gradient checking can help verify if one's implementation of backpropagation is bug-free. 
> 
> Check
> 
> Correct
> 
> If the gradient computed by backpropagation is the same as one computed numerically with gradient checking, this is very strong evidence that you have a correct implementation of backpropagation.
> 
>  5.Question 5
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 / 1 point 
> 

      If we are training a neural network using gradient descent, one reasonable "debugging" step to make sure it is working is to plot J(Θ)J(\Theta)J(Θ) as a function of the number of iterations, and make sure it is decreasing (or at least non-increasing) after each iteration. 
> 
> Check
> 
> Correct
> 
> Since gradient descent uses the gradient to take a step toward parameters with lower cost (ie, lower J(Θ)J(\Theta)J(Θ)), the value of J(Θ)J(\Theta)J(Θ) should be equal or less at each iteration if the gradient computation is correct and the learning rate is set properly.
> 
>  Suppose we are using gradient descent with learning rate α\alphaα. For logistic regression and linear regression, J(θ)J(\theta)J(θ) was a convex optimization problem and thus we did not want to choose a learning rate α\alphaα that is too large. For a neural network however, J(Θ)J(\Theta)J(Θ) may not be convex, and thus choosing a very large value of α\alphaα can only speed up convergence. 
> 
>  Suppose that the parameter Θ(1)\Theta^{(1)}Θ(1) is a square matrix (meaning the number of rows equals the number of columns). If we replace Θ(1)\Theta^{(1)}Θ(1) with its transpose (Θ(1))T(\Theta^{(1)})^T(Θ(1))T, then we have not changed the function that the network is computing. 
> 

      Suppose we have a correct implementation of backpropagation, and are training a neural network using gradient descent. Suppose we plot J(Θ)J(\Theta)J(Θ) as a function of the number of iterations, and find that it is **increasing** rather than decreasing. One possible cause of this is that the learning rate α\alphaα is too large. 
> 
> Check
> 
> Correct
> 
> If the learning rate is too large, the cost function can diverge during gradient descent. Thus, you should select a smaller value of α\alphaα.
>
> -- https://www.coursera.org/learn/machine-learning/exam/3UQTb/neural-networks-learning/attempt?redirectToCover=true#Tunnel Vision Close
