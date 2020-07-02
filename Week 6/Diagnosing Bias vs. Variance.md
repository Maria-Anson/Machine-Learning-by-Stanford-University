# Diagnosing Bias vs. Variance
> 
> In this section we examine the relationship between the degree of the polynomial d and the underfitting or overfitting of our hypothesis.
> 
> *   We need to distinguish whether **bias** or **variance** is the problem contributing to bad predictions.
> *   High bias is underfitting and high variance is overfitting. Ideally, we need to find a golden mean between these two.
> 
> The training error will tend to **decrease** as we increase the degree d of the polynomial.
> 
> At the same time, the cross validation error will tend to **decrease** as we increase d up to a point, and then it will **increase** as d is increased, forming a convex curve.
> 
> **High bias (underfitting)**: both Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) will be high. Also, JCV(Θ)≈Jtrain(Θ)J_{CV}(\Theta) \approx J_{train}(\Theta)JCV​(Θ)≈Jtrain​(Θ).
> 
> **High variance (overfitting)**: Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) will be low and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) will be much greater than Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ).
> 
> The is summarized in the figure below:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/I4dRkz_pEeeHpAqQsW8qwg_bed7efdd48c13e8f75624c817fb39684_fixed.png?expiry=1593820800000&hmac=vWLBSE8B4C4yuuknrvpgztCbfWSA3FhCI0QDmXKSMno)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/81vp0/diagnosing-bias-vs-variance#main
