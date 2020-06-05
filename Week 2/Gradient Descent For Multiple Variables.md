# Gradient Descent For Multiple Variables
> 
> ## **Gradient Descent for Multiple Variables**
> 
> The gradient descent equation itself is generally the same form; we just have to repeat it for our 'n' features:
> 
> }repeat until convergence:{θ0:=θ0−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)0θ1:=θ1−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)1θ2:=θ2−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)2⋯\begin{align*} & \text{repeat until convergence:} \; \lbrace \newline \; & \theta_0 := \theta_0 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_0^{(i)}\newline \; & \theta_1 := \theta_1 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_1^{(i)} \newline \; & \theta_2 := \theta_2 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_2^{(i)} \newline & \cdots \newline \rbrace \end{align*}
> 
> In other words:
> 
> }repeat until convergence:{θj:=θj−α1m∑i=1m(hθ(x(i))−y(i))⋅x(i)jfor j := 0...n\begin{align*}& \text{repeat until convergence:} \; \lbrace \newline \; & \theta_j := \theta_j - \alpha \frac{1}{m} \sum\limits_{i=1}^{m} (h_\theta(x^{(i)}) - y^{(i)}) \cdot x_j^{(i)} \; & \text{for j := 0...n}\newline \rbrace\end{align*}
> 
> The following image compares gradient descent with one variable to gradient descent with multiple variables:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MYm8uqafEeaZoQ7hPZtKqg_c974c2e2953662e9578b38c7b04591ed_Screenshot-2016-11-09-09.07.04.png?expiry=1591488000000&hmac=16dbmrkkFXHADThwEFxv08ca0MENGXqwvIQfVjVQVrE)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/aEN5G/gradient-descent-for-multiple-variables#main
