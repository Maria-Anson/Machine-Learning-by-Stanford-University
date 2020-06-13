# Cost Function
> 
> **Note:** [5:18 - There is a typo. It should be ∑j=1nθj2\sum_{j=1}^{n} \theta _j ^2∑j=1n​θj2​ instead of ∑i=1nθj2\sum_{i=1}^{n} \theta _j ^2∑i=1n​θj2​]
> 
> If we have overfitting from our hypothesis function, we can reduce the weight that some of the terms in our function carry by increasing their cost.
> 
> Say we wanted to make the following function more quadratic:
> 
> θ0+θ1x+θ2x2+θ3x3+θ4x4\theta_0 + \theta_1x + \theta_2x^2 + \theta_3x^3 + \theta_4x^4θ0​+θ1​x+θ2​x2+θ3​x3+θ4​x4
> 
> We'll want to eliminate the influence of θ3x3\theta_3x^3θ3​x3 and θ4x4\theta_4x^4θ4​x4 . Without actually getting rid of these features or changing the form of our hypothesis, we can instead modify our **cost function**:
> 
> minθ12m∑i=1m(hθ(x(i))−y(i))2+1000⋅θ32+1000⋅θ42min_\theta\ \dfrac{1}{2m}\sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2 + 1000\cdot\theta_3^2 + 1000\cdot\theta_4^2minθ​ 2m1​∑i=1m​(hθ​(x(i))−y(i))2+1000⋅θ32​+1000⋅θ42​
> 
> We've added two extra terms at the end to inflate the cost of θ3\theta_3θ3​ and θ4\theta_4θ4​. Now, in order for the cost function to get close to zero, we will have to reduce the values of θ3\theta_3θ3​ and θ4\theta_4θ4​ to near zero. This will in turn greatly reduce the values of θ3x3\theta_3x^3θ3​x3 and θ4x4\theta_4x^4θ4​x4 in our hypothesis function. As a result, we see that the new hypothesis (depicted by the pink curve) looks like a quadratic function but fits the data better due to the extra small terms θ3x3\theta_3x^3θ3​x3 and θ4x4 \theta_4x^4θ4​x4.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/j0X9h6tUEeawbAp5ByfpEg_ea3e85af4056c56fa704547770da65a6_Screenshot-2016-11-15-08.53.32.png?expiry=1592179200000&hmac=mw4Bq7X4lSL-8vUAzZ89K_A_GvInALrgcy4h40NAqCc)
> 
> We could also regularize all of our theta parameters in a single summation as:
> 
> minθ12m∑i=1m(hθ(x(i))−y(i))2+λ∑j=1nθj2min_\theta\ \dfrac{1}{2m}\ \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)})^2 + \lambda\ \sum_{j=1}^n \theta_j^2minθ​ 2m1​ ∑i=1m​(hθ​(x(i))−y(i))2+λ ∑j=1n​θj2​
> 
> The λ, or lambda, is the **regularization parameter**. It determines how much the costs of our theta parameters are inflated.
> 
> Using the above cost function with the extra summation, we can smooth the output of our hypothesis function to reduce overfitting. If lambda is chosen to be too large, it may smooth out the function too much and cause underfitting. Hence, what would happen if λ=0\lambda = 0λ=0 or is too small ?
>
> -- https://www.coursera.org/learn/machine-learning/supplement/1tJlY/cost-function#main
