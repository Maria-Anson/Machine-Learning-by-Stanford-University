# Regularized Logistic Regression
> 
> We can regularize logistic regression in a similar way that we regularize linear regression. As a result, we can avoid overfitting. The following image shows how the regularized function, displayed by the pink line, is less likely to overfit than the non-regularized function represented by the blue line:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Od9mobDaEeaCrQqTpeD5ng_4f5e9c71d1aa285c1152ed4262f019c1_Screenshot-2016-11-22-09.31.21.png?expiry=1592179200000&hmac=40Qe6vJAi9ION66dxvPEtu87MpNj8ajj9DhaJAvHkb8)
> 
> ### Cost Function
> 
> Recall that our cost function for logistic regression was:
> 
> J(θ)=−1m∑i=1m[y(i)log⁡(hθ(x(i)))+(1−y(i))log⁡(1−hθ(x(i)))]J(\theta) = - \frac{1}{m} \sum_{i=1}^m \large[ y^{(i)}\ \log (h_\theta (x^{(i)})) + (1 - y^{(i)})\ \log (1 - h_\theta(x^{(i)})) \large]J(θ)=−m1​∑i=1m​[y(i) log(hθ​(x(i)))+(1−y(i)) log(1−hθ​(x(i)))]
> 
> We can regularize this equation by adding a term to the end:
> 
> J(θ)=−1m∑i=1m[y(i)log⁡(hθ(x(i)))+(1−y(i))log⁡(1−hθ(x(i)))]+λ2m∑j=1nθj2J(\theta) = - \frac{1}{m} \sum_{i=1}^m \large[ y^{(i)}\ \log (h_\theta (x^{(i)})) + (1 - y^{(i)})\ \log (1 - h_\theta(x^{(i)}))\large] + \frac{\lambda}{2m}\sum_{j=1}^n \theta_j^2J(θ)=−m1​∑i=1m​[y(i) log(hθ​(x(i)))+(1−y(i)) log(1−hθ​(x(i)))]+2mλ​∑j=1n​θj2​
> 
> The second sum, ∑j=1nθj2\sum_{j=1}^n \theta_j^2∑j=1n​θj2​ **means to explicitly exclude** the bias term, θ0\theta_0θ0​. I.e. the θ vector is indexed from 0 to n (holding n+1 values, θ0\theta_0θ0​ through θn\theta_nθn​), and this sum explicitly skips θ0\theta_0θ0​, by running from 1 to n, skipping 0\. Thus, when computing the equation, we should continuously update the two following equations:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dfHLC70SEea4MxKdJPaTxA_306de28804a7467f7d84da0fe3ee9c7b_Screen-Shot-2016-12-07-at-10.49.02-PM.png?expiry=1592179200000&hmac=jHV2b7-BkHw1CqxPI4HP65oEhl9IhDHQMMAfxjNUBgA)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/v51eg/regularized-logistic-regression#main
