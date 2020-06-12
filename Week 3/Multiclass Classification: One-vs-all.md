# Multiclass Classification: One-vs-all
> 
> Now we will approach the classification of data when we have more than two categories. Instead of y = {0,1} we will expand our definition so that y = {0,1...n}.
> 
> Since y = {0,1...n}, we divide our problem into n+1 (+1 because the index starts at 0) binary classification problems; in each one, we predict the probability that 'y' is a member of one of our classes.
> 
> y∈{0,1...n}h(0)θ(x)=P(y=0|x;θ)h(1)θ(x)=P(y=1|x;θ)⋯h(n)θ(x)=P(y=n|x;θ)prediction=maxi(h(i)θ(x))\begin{align*}& y \in \lbrace0, 1 ... n\rbrace \newline& h_\theta^{(0)}(x) = P(y = 0 | x ; \theta) \newline& h_\theta^{(1)}(x) = P(y = 1 | x ; \theta) \newline& \cdots \newline& h_\theta^{(n)}(x) = P(y = n | x ; \theta) \newline& \mathrm{prediction} = \max_i( h_\theta ^{(i)}(x) )\newline\end{align*}
> 
> We are basically choosing one class and then lumping all the others into a single second class. We do this repeatedly, applying binary logistic regression to each case, and then use the hypothesis that returned the highest value as our prediction.
> 
> The following image shows how one could classify 3 classes:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cqmPjanSEeawbAp5ByfpEg_299fcfbd527b6b5a7440825628339c54_Screenshot-2016-11-13-10.52.29.png?expiry=1592092800000&hmac=CS5KPmpvGS53pOSV-cl_CWqxsqQrTGFu6LleOMVcm3s)
> 
> **To summarize:**
> 
> Train a logistic regression classifier hθ(x)h_\theta(x)hθ​(x) for each class￼ to predict the probability that ￼ ￼y = i￼ ￼.
> 
> To make a prediction on a new x, pick the class ￼that maximizes hθ(x) h_\theta (x) hθ​(x)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/HuE6M/multiclass-classification-one-vs-all#main
