# Regularized Linear Regression
> 
> **Note:** [8:43 - It is said that X is non-invertible if m ≤\leq≤ n. The correct statement should be that X is non-invertible if m < n, and may be non-invertible if m = n.
> 
> We can apply regularization to both linear regression and logistic regression. We will approach linear regression first.
> 
> ### Gradient Descent
> 
> We will modify our gradient descent function to separate out θ0\theta_0θ0​ from the rest of the parameters because we do not want to penalize θ0\theta_0θ0​.
> 
> Repeat {    θ0:=θ0−α 1m ∑i=1m(hθ(x(i))−y(i))x(i)0    θj:=θj−α [(1m ∑i=1m(hθ(x(i))−y(i))x(i)j)+λmθj]}          j∈{1,2...n}\begin{align*} & \text{Repeat}\ \lbrace \newline & \ \ \ \ \theta_0 := \theta_0 - \alpha\ \frac{1}{m}\ \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})x_0^{(i)} \newline & \ \ \ \ \theta_j := \theta_j - \alpha\ \left[ \left( \frac{1}{m}\ \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})x_j^{(i)} \right) + \frac{\lambda}{m}\theta_j \right] &\ \ \ \ \ \ \ \ \ \ j \in \lbrace 1,2...n\rbrace\newline & \rbrace \end{align*}
> 
> The term λmθj\frac{\lambda}{m}\theta_jmλ​θj​ performs our regularization. With some manipulation our update rule can also be represented as:
> 
> θj:=θj(1−αλm)−α1m∑i=1m(hθ(x(i))−y(i))xj(i)\theta_j := \theta_j(1 - \alpha\frac{\lambda}{m}) - \alpha\frac{1}{m}\sum_{i=1}^m(h_\theta(x^{(i)}) - y^{(i)})x_j^{(i)}θj​:=θj​(1−αmλ​)−αm1​∑i=1m​(hθ​(x(i))−y(i))xj(i)​
> 
> The first term in the above equation, 1−αλm1 - \alpha\frac{\lambda}{m}1−αmλ​ will always be less than 1\. Intuitively you can see it as reducing the value of θj\theta_jθj​ by some amount on every update. Notice that the second term is now exactly the same as it was before.
> 
> ### **Normal Equation**
> 
> Now let's approach regularization using the alternate method of the non-iterative normal equation.
> 
> To add in regularization, the equation is the same as our original, except that we add another term inside the parentheses:
> 
> θ=(XTX+λ⋅L)−1XTywhere  L=⎡⎣⎢⎢⎢⎢⎢⎢011⋱1⎤⎦⎥⎥⎥⎥⎥⎥\begin{align*}& \theta = \left( X^TX + \lambda \cdot L \right)^{-1} X^Ty \newline& \text{where}\ \ L = \begin{bmatrix} 0 & & & & \newline & 1 & & & \newline & & 1 & & \newline & & & \ddots & \newline & & & & 1 \newline\end{bmatrix}\end{align*}
> 
> L is a matrix with 0 at the top left and 1's down the diagonal, with 0's everywhere else. It should have dimension (n+1)×(n+1). Intuitively, this is the identity matrix (though we are not including x0x_0x0​), multiplied with a single real number λ.
> 
> Recall that if m < n, then XTXX^TXXTX is non-invertible. However, when we add the term λ⋅L, then XTXX^TXXTX + λ⋅L becomes invertible.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/pKAsc/regularized-linear-regression#main
