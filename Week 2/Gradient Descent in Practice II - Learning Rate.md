# Gradient Descent in Practice II - Learning Rate
> 
> **Note:** [5:20 - the x -axis label in the right graph should be θ\thetaθ rather than No. of iterations ]
> 
> **Debugging gradient descent.** Make a plot with _number of iterations_ on the x-axis. Now plot the cost function, J(θ) over the number of iterations of gradient descent. If J(θ) ever increases, then you probably need to decrease α.
> 
> **Automatic convergence test.** Declare convergence if J(θ) decreases by less than E in one iteration, where E is some small value such as 10−310^{−3}10−3. However in practice it's difficult to choose this threshold value.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FEfS3aajEea3qApInhZCFg_6be025f7ad145eb0974b244a7f5b3f59_Screenshot-2016-11-09-09.35.59.png?expiry=1591488000000&hmac=7Gfkw8g2bH3zmGcRNvNOSx7nY83xYMZ9R50nxad3GTo)
> 
> It has been proven that if learning rate α is sufficiently small, then J(θ) will decrease on every iteration.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rC2jGKgvEeamBAoLccicqA_ec9e40a58588382f5b6df60637b69470_Screenshot-2016-11-11-08.55.21.png?expiry=1591488000000&hmac=mqnm7R_pi4itAqynHw-ndVpsQNhsUR5mjmz1dDTFAkI)
> 
> To summarize:
> 
> If α\alphaα is too small: slow convergence.
> 
> If α\alphaα is too large: ￼may not decrease on every iteration and thus may not converge.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/TnHvV/gradient-descent-in-practice-ii-learning-rate#main
