# Cost Function
> 
> We cannot use the same cost function that we use for linear regression because the Logistic Function will cause the output to be wavy, causing many local optima. In other words, it will not be a convex function.
> 
> Instead, our cost function for logistic regression looks like:
> 
> J(θ)=1m∑i=1mCost(hθ(x(i)),y(i))Cost(hθ(x),y)=−log(hθ(x))Cost(hθ(x),y)=−log(1−hθ(x))if y = 1if y = 0\begin{align*}& J(\theta) = \dfrac{1}{m} \sum_{i=1}^m \mathrm{Cost}(h_\theta(x^{(i)}),y^{(i)}) \newline & \mathrm{Cost}(h_\theta(x),y) = -\log(h_\theta(x)) \; & \text{if y = 1} \newline & \mathrm{Cost}(h_\theta(x),y) = -\log(1-h_\theta(x)) \; & \text{if y = 0}\end{align*}
> 
> When y = 1, we get the following plot for J(θ)J(\theta)J(θ) vs hθ(x)h_\theta (x)hθ​(x):
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Q9sX8nnxEeamDApmnD43Fw_1cb67ecfac77b134606532f5caf98ee4_Logistic_regression_cost_function_positive_class.png?expiry=1592006400000&hmac=OVZBhoJbQRK-qTspi7Cjyb2zdj07-ZAI7jrAj8lzDk4)
> 
> Similarly, when y = 0, we get the following plot for J(θ)J(\theta)J(θ) vs hθ(x)h_\theta (x)hθ​(x):
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Ut7vvXnxEead-BJkoDOYOw_f719f2858d78dd66d80c5ec0d8e6b3fa_Logistic_regression_cost_function_negative_class.png?expiry=1592006400000&hmac=vJYyjCXABC4itPYYMv0iTan7z528camTep-cmvRWFBE)Cost(hθ(x),y)=0 if hθ(x)=yCost(hθ(x),y)→∞ if y=0andhθ(x)→1Cost(hθ(x),y)→∞ if y=1andhθ(x)→0\begin{align*}& \mathrm{Cost}(h_\theta(x),y) = 0 \text{ if } h_\theta(x) = y \newline & \mathrm{Cost}(h_\theta(x),y) \rightarrow \infty \text{ if } y = 0 \; \mathrm{and} \; h_\theta(x) \rightarrow 1 \newline & \mathrm{Cost}(h_\theta(x),y) \rightarrow \infty \text{ if } y = 1 \; \mathrm{and} \; h_\theta(x) \rightarrow 0 \newline \end{align*}
> 
> If our correct answer 'y' is 0, then the cost function will be 0 if our hypothesis function also outputs 0\. If our hypothesis approaches 1, then the cost function will approach infinity.
> 
> If our correct answer 'y' is 1, then the cost function will be 0 if our hypothesis function outputs 1\. If our hypothesis approaches 0, then the cost function will approach infinity.
> 
> Note that writing the cost function in this way guarantees that J(θ) is convex for logistic regression.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/bgEt4/cost-function#main
