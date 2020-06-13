> # The Problem of Overfitting
> 
> Consider the problem of predicting y from x ∈ R. The leftmost figure below shows the result of fitting a y = θ0+θ1xθ_0 + θ_1xθ0​+θ1​x to a dataset. We see that the data doesn’t really lie on straight line, and so the fit is not very good.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0cOOdKsMEeaCrQqTpeD5ng_2a806eb8d988461f716f4799915ab779_Screenshot-2016-11-15-00.23.30.png?expiry=1592179200000&hmac=jfk23u6YiWaqe5sha_SHsAVc3ntx_QIP4WM9LvGvkcw)
> 
> Instead, if we had added an extra feature x2x^2x2 , and fit y=θ0+θ1x+θ2x2y = \theta_0 + \theta_1x + \theta_2x^2y=θ0​+θ1​x+θ2​x2 , then we obtain a slightly better fit to the data (See middle figure). Naively, it might seem that the more features we add, the better. However, there is also a danger in adding too many features: The rightmost figure is the result of fitting a 5th5^{th}5th order polynomial y=∑j=05θjxjy = \sum_{j=0} ^5 \theta_j x^jy=∑j=05​θj​xj. We see that even though the fitted curve passes through the data perfectly, we would not expect this to be a very good predictor of, say, housing prices (y) for different living areas (x). Without formally defining what these terms mean, we’ll say the figure on the left shows an instance of **underfitting**—in which the data clearly shows structure not captured by the model—and the figure on the right is an example of **overfitting**.
> 
> Underfitting, or high bias, is when the form of our hypothesis function h maps poorly to the trend of the data. It is usually caused by a function that is too simple or uses too few features. At the other extreme, overfitting, or high variance, is caused by a hypothesis function that fits the available data but does not generalize well to predict new data. It is usually caused by a complicated function that creates a lot of unnecessary curves and angles unrelated to the data.
> 
> This terminology is applied to both linear and logistic regression. There are two main options to address the issue of overfitting:
> 
> 1) Reduce the number of features:
> 
> *   Manually select which features to keep.
> *   Use a model selection algorithm (studied later in the course).
> 
> 2) Regularization
> 
> *   Keep all the features, but reduce the magnitude of parameters θj\theta_jθj​.
> *   Regularization works well when we have a lot of slightly useful features.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/VTe37/the-problem-of-overfitting#main
