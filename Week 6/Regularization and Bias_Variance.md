# Regularization and Bias/Variance
> 
> **Note:** [The regularization term below and through out the video should be λ2m∑j=1nθj2\frac \lambda {2m} \sum _{j=1}^n \theta_j ^22mλ​∑j=1n​θj2​ and **NOT** λ2m∑j=1mθj2\frac \lambda {2m} \sum _{j=1}^m \theta_j ^22mλ​∑j=1m​θj2​]
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3XyCytntEeataRJ74fuL6g_3b6c06d065d24e0bf8d557e59027e87a_Screenshot-2017-01-13-16.09.36.png?expiry=1593820800000&hmac=Q-6Su-AxE704Yp0r5iPnProEJZxKEYIgqlTJtpQ88F8)
> 
> In the figure above, we see that as λ\lambdaλ increases, our fit becomes more rigid. On the other hand, as λ\lambdaλ approaches 0, we tend to over overfit the data. So how do we choose our parameter λ\lambdaλ to get it 'just right' ? In order to choose the model and the regularization term λ, we need to:
> 
> 1.  Create a list of lambdas (i.e. λ∈{0,0.01,0.02,0.04,0.08,0.16,0.32,0.64,1.28,2.56,5.12,10.24});
> 2.  Create a set of models with different degrees or any other variants.
> 3.  Iterate through the λ\lambdaλs and for each λ\lambdaλ go through all the models to learn some Θ\ThetaΘ.
> 4.  Compute the cross validation error using the learned Θ (computed with λ) on the JCV(Θ)J_{CV}(\Theta)JCV​(Θ) **without** regularization or λ = 0.
> 5.  Select the best combo that produces the lowest error on the cross validation set.
> 6.  Using the best combo Θ and λ, apply it on Jtest(Θ)J_{test}(\Theta)Jtest​(Θ) to see if it has a good generalization of the problem.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/JPJJj/regularization-and-bias-variance#main
