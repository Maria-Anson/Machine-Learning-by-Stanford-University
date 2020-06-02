 # Gradient Descent For Linear Regression
 
 **Note:** [At 6:15 "h(x) = -900 - 0.1x" should be "h(x) = 900 - 0.1x"]
 
 When specifically applied to the case of linear regression, a new form of the gradient descent equation can be derived. We can substitute our actual cost function and our actual hypothesis function and modify the equation to :
 
 repeat until convergence: {θ0:=θ1:=}θ0−α1m∑i=1m(hθ(xi)−yi)θ1−α1m∑i=1m((hθ(xi)−yi)xi)\begin{align*} \text{repeat until convergence: } \lbrace & \newline \theta_0 := & \theta_0 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m}(h_\theta(x_{i}) - y_{i}) \newline \theta_1 := & \theta_1 - \alpha \frac{1}{m} \sum\limits_{i=1}^{m}\left((h_\theta(x_{i}) - y_{i}) x_{i}\right) \newline \rbrace& \end{align*}

 where m is the size of the training set, θ0\theta_0θ0​ a constant that will be changing simultaneously with θ1\theta_1θ1​ and xi,yix_{i}, y_{i}xi​,yi​are values of the given training set (data).
 
 Note that we have separated out the two cases for θj\theta_jθj​ into separate equations for θ0\theta_0θ0​ and θ1\theta_1θ1​; and that for θ1\theta_1θ1​ we are multiplying xix_{i}xi​ at the end due to the derivative. The following is a derivation of ∂∂θjJ(θ)\frac {\partial}{\partial \theta_j}J(\theta)∂θj​∂​J(θ) for a single example :
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/QFpooaaaEea7TQ6MHcgMPA_cc3c276df7991b1072b2afb142a78da1_Screenshot-2016-11-09-08.30.54.png?expiry=1591228800000&hmac=D_jeC735ytWPXi_hS_H5mSE_GEGGQpn4NcGxoDR6604)
 
 The point of all this is that if we start with a guess for our hypothesis and then repeatedly apply these gradient descent equations, our hypothesis will become more and more accurate.
 
 So, this is simply gradient descent on the original cost function J. This method looks at every example in the entire training set on every step, and is called **batch gradient descent**. Note that, while gradient descent can be susceptible to local minima in general, the optimization problem we have posed here for linear regression has only one global, and no other local, optima; thus gradient descent always converges (assuming the learning rate α is not too large) to the global minimum. Indeed, J is a convex quadratic function. Here is an example of gradient descent as it is run to minimize a quadratic function.
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xAQBlqaaEeawbAp5ByfpEg_24e9420f16fdd758ccb7097788f879e7_Screenshot-2016-11-09-08.36.49.png?expiry=1591228800000&hmac=HlDFQ08BS_8YOQRz8k5An1KqJ9GcThoLXWejTui-IFE)
 
 The ellipses shown above are the contours of a quadratic function. Also shown is the trajectory taken by gradient descent, which was initialized at (48,30). The x’s in the figure (joined by straight lines) mark the successive values of θ that gradient descent went through as it converged to its minimum.

 -- https://www.coursera.org/learn/machine-learning/supplement/U90DX/gradient-descent-for-linear-regression#main
