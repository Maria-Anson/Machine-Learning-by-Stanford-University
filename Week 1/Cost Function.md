 # Cost Function
 
 We can measure the accuracy of our hypothesis function by using a **cost function**. This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's.
 
 J(θ0,θ1)=12m∑i=1m(y^i−yi)2=12m∑i=1m(hθ(xi)−yi)2J(\theta_0, \theta_1) = \dfrac {1}{2m} \displaystyle \sum _{i=1}^m \left ( \hat{y}_{i}- y_{i} \right)^2 = \dfrac {1}{2m} \displaystyle \sum _{i=1}^m \left (h_\theta (x_{i}) - y_{i} \right)^2J(θ0​,θ1​)=2m1​i=1∑m​(y^​i​−yi​)2=2m1​i=1∑m​(hθ​(xi​)−yi​)2
 
 To break it apart, it is 12\frac{1}{2}21​ xˉ\bar{x}xˉ where xˉ\bar{x}xˉ is the mean of the squares of hθ(xi)−yih_\theta (x_{i}) - y_{i}hθ​(xi​)−yi​ , or the difference between the predicted value and the actual value.
 
 This function is otherwise called the "Squared error function", or "Mean squared error". The mean is halved (12)\left(\frac{1}{2}\right)(21​) as a convenience for the computation of the gradient descent, as the derivative term of the square function will cancel out the 12\frac{1}{2}21​ term. The following image summarizes what the cost function does:
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/R2YF5Lj3EeajLxLfjQiSjg_110c901f58043f995a35b31431935290_Screen-Shot-2016-12-02-at-5.23.31-PM.png?expiry=1591142400000&hmac=fLC7MPzZbQ9NLAM5QqzMFBQMWd8-VC3e2N7VBFP7yhw)

> -- https://www.coursera.org/learn/machine-learning/supplement/nhzyF/cost-function#main
