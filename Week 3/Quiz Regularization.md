# Regularization
> 
> Total points 5
> 
>  1.Question 1
> 
> You are training a classification model with logistic
> 
> regression. Which of the following statements are true? Check
> 
> all that apply.
> 
> 1 point 
> 
>  Adding many new features to the model helps prevent overfitting on the training set. 
> 

      Introducing regularization to the model always results in equal or better performance on examples not in the training set. 
> 
>  Adding a new feature to the model always results in equal or better performance on the training set. 
> 
>  Introducing regularization to the model always results in equal or better performance on the training set. 
> 
>  2.Question 2
> 
> Suppose you ran logistic regression twice, once with λ=0\lambda = 0λ=0, and once with λ=1\lambda = 1λ=1. One of the times, you got
> 
> parameters θ=[26.2965.41]\theta =
> 
> [26.2965.41]
> 
> \begin{bmatrix} 26.29 \\ 65.41 \end{bmatrix}θ=[26.2965.41​], and the other time you got
> 
> θ=[2.751.32]\theta =
> 
> [2.751.32]
> 
> \begin{bmatrix} 2.75 \\ 1.32 \end{bmatrix}θ=[2.751.32​]. However, you forgot which value of
> 
> λ\lambdaλ corresponds to which value of θ\thetaθ. Which one do you
> 
> think corresponds to λ=1\lambda = 1λ=1?
> 
> 1 point 
> 
>  θ=[26.2965.41]\theta =
> 
> [26.2965.41]
> 
> \begin{bmatrix} 26.29 \\ 65.41 \end{bmatrix}θ=[26.2965.41​] 
> 

      θ=[2.751.32]\theta =
> 
> [2.751.32]
> 
> \begin{bmatrix} 2.75 \\ 1.32 \end{bmatrix}θ=[2.751.32​] 
> 
>  3.Question 3
> 
> Which of the following statements about regularization are
> 
> true? Check all that apply.
> 
> 1 point 
> 
>  Because regularization causes J(θ)J(\theta)J(θ) to no longer be convex, gradient descent may not always converge to the global minimum (when λ>0\lambda > 0λ>0, and when using an appropriate learning rate α\alphaα). 
> 
>  Using a very large value of λ\lambdaλ cannot hurt the performance of your hypothesis; the only reason we do not set λ\lambdaλ to be too large is to avoid numerical problems. 
> 

      Using too large a value of λ\lambdaλ can cause your hypothesis to underfit the data. 
> 
>  Because logistic regression outputs values 0≤hθ(x)≤10 \leq h_\theta(x) \leq 10≤hθ​(x)≤1, its range of output values can only be "shrunk" slightly by regularization anyway, so regularization is generally not helpful for it. 
> 
>  4.Question 4
> 
> In which one of the following figures do you think the hypothesis has overfit the training set?
> 
> 1 point 
> 
>  Figure:
> 

   ![](https://d3c33hcgiwev3.cloudfront.net/6w-qg77oEeSZtCIACx4DqA_Screen-Shot-2015-02-27-at-5.24.59-PM.png?Expires=1592179200&Signature=kLJlbV~Vl0bWIY3mXsCDnrEaGPwfAyP5iT-yRSiM2cWKvzYF2E175WHVeUH3H3PTKEz7MvbGoOc6k1DAwQNH4SMrXLR13jX0TKZbnhLFBjpe2EZNGtODN4zIiowihiUSmnSV4CZCZ9nYVcdwX0G1y0jx-C9SPGvZtkS~HTq3xqI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  Figure:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/B--iib7pEeSjMiIAC7MDiQ_Screen-Shot-2015-02-27-at-5.25.16-PM.png?Expires=1592179200&Signature=HASeVH2d7fdQfZ5N0e9p37-Ak3u7qLF5Jbm9b7A1JWEl~YX01W7hA6O~VNhDXlvclE5k3TVd3R~zJaayPx7-qEPbIv-pi1eTCiSGhjP9RDE3hU4xnaD7-yJzsokm3jITNbcEA0vpprMQyOPGoINF8YgXbk98Ct3T2iD3CqpjLag_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  Figure:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/MMTSK77pEeSjMiIAC7MDiQ_Screen-Shot-2015-02-27-at-5.25.39-PM.png?Expires=1592179200&Signature=W03ehNs88HFW~1A32oiK6QdPwdeVaJt6aAqRUvhfl-viafUysmZnvuV6-EaJw3OkvYm1IeITlQcpM9XD9CqG9d9w430GPrXZoLrBoAgj2yRPRv6eJ9gFMXKVs-DMg4qwRvZZp1nPf2dujKFBY5qekg8TwNR0I59tCIIgcOegu5o_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  Figure:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/SlZinr7pEeSKOiIAC1ARFQ_Screen-Shot-2015-02-27-at-5.25.45-PM.png?Expires=1592179200&Signature=c~sck~Wt0ZM3Zr4KaL6vybamPQd61dIjl8OZPsMVA7K2b-uzpQ~BNanNxvuLtf4EzbAZQlNsOLDuGXVpMVCVANo4VOrIGic1A6HE3-zBrq8YpofGempQjDp3jv-fXhxUFEHQBRZxGm73vbWvT54KjDaSOCet-Keg8s7CeVdDXN8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  5.Question 5
> 
> In which one of the following figures do you think the hypothesis has underfit the training set?
> 
> 1 point 
> 
>  Figure:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/4qRnjr7pEeSjMiIAC7MDiQ_Screen-Shot-2015-02-27-at-5.30.48-PM.png?Expires=1592179200&Signature=P~ISrIU0X9cFmBAsIRahaIY1a6ony-2syjiznASUn7Lyx2cLLZvk8WxcVHiejt6uYZT5py6c1GTXeYAL5M~6GQ59odkqXwSSD5G7uMVr3W0D3dGNbJYVxteLezcTIODWTeqvOCPLAShdrF3mIzMa-s8Ecs8ETpyszRLs-V-lwnI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  Figure:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/8kfaFb7pEeSZtCIACx4DqA_Screen-Shot-2015-02-27-at-5.30.56-PM.png?Expires=1592179200&Signature=T0QVL8tJk3hjIKy3EsWmLVB8g7kOFS4M0L7siLmxASskl1gO52ILIZHnDs7UX8bqyIHCy5ZibzZM8ONPcjvDHovubwVPz-yuMjKNZdfNBpBIiyQWyK5rLykimvTXfD-vegUp9pYsnbshHFjYyXLQ5iF5yB0jlZxAqwNPZw-f0GI_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  Figure:
> 

   ![](https://d3c33hcgiwev3.cloudfront.net/BRZOFr7qEeSZtCIACx4DqA_Screen-Shot-2015-02-27-at-5.31.02-PM.png?Expires=1592179200&Signature=OMOjKdumov6DWozveafDMDyL3CzD1Mw4Y4Tokbz1Dxb7RSMMkWsLgqtcxhf733x9J7I39pOIlCznEbBJitiQnoGV5RB-FgKzqKauYFkjXLZQBoWKuV5uta~z9Km0cjXd66QmN2Yg6J-mTAzLTNme7IEikaAeLWgyqoq2898yTG0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
>
> -- https://www.coursera.org/learn/machine-learning/exam/lehkt/regularization/attempt#Tunnel Vision Close
