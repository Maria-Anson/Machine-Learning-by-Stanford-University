# Simplified Cost Function and Gradient Descent
> 
> **Note:** [6:53 - the gradient descent equation should have a 1/m factor]
> 
> We can compress our cost function's two conditional cases into one case:
> 
> Cost(hθ(x),y)=−ylog⁡(hθ(x))−(1−y)log⁡(1−hθ(x))\mathrm{Cost}(h_\theta(x),y) = - y \; \log(h_\theta(x)) - (1 - y) \log(1 - h_\theta(x))Cost(hθ​(x),y)=−ylog(hθ​(x))−(1−y)log(1−hθ​(x))
> 
> Notice that when y is equal to 1, then the second term (1−y)log⁡(1−hθ(x))(1-y)\log(1-h_\theta(x))(1−y)log(1−hθ​(x)) will be zero and will not affect the result. If y is equal to 0, then the first term −ylog⁡(hθ(x))-y \log(h_\theta(x))−ylog(hθ​(x)) will be zero and will not affect the result.
> 
> We can fully write out our entire cost function as follows:
> 
> J(θ)=−1m∑i=1m[y(i)log⁡(hθ(x(i)))+(1−y(i))log⁡(1−hθ(x(i)))]J(\theta) = - \frac{1}{m} \displaystyle \sum_{i=1}^m [y^{(i)}\log (h_\theta (x^{(i)})) + (1 - y^{(i)})\log (1 - h_\theta(x^{(i)}))]J(θ)=−m1​i=1∑m​[y(i)log(hθ​(x(i)))+(1−y(i))log(1−hθ​(x(i)))]
> 
> A vectorized implementation is:
> 
> h=g(Xθ)J(θ)=1m⋅(−yTlog(h)−(1−y)Tlog(1−h))\begin{align*} & h = g(X\theta)\newline & J(\theta) = \frac{1}{m} \cdot \left(-y^{T}\log(h)-(1-y)^{T}\log(1-h)\right) \end{align*}
> 
> ### **Gradient Descent**
> 
> Remember that the general form of gradient descent is:
> 
> Repeat{θj:=θj−α∂∂θjJ(θ)}\begin{align*}& Repeat \; \lbrace \newline & \; \theta_j := \theta_j - \alpha \dfrac{\partial}{\partial \theta_j}J(\theta) \newline & \rbrace\end{align*}
> 
> We can work out the derivative part using calculus to get:
> 
> Repeat{θj:=θj−αm∑i=1m(hθ(x(i))−y(i))x(i)j}\begin{align*} & Repeat \; \lbrace \newline & \; \theta_j := \theta_j - \frac{\alpha}{m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)}) x_j^{(i)} \newline & \rbrace \end{align*}
> 
> Notice that this algorithm is identical to the one we used in linear regression. We still have to simultaneously update all values in theta.
> 
> A vectorized implementation is:
> 
> θ:=θ−αmXT(g(Xθ)−y⃗)\theta := \theta - \frac{\alpha}{m} X^{T} (g(X \theta ) - \vec{y})θ:=θ−mα​XT(g(Xθ)−y​)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/0hpMl/simplified-cost-function-and-gradient-descent#main
