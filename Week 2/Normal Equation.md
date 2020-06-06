# Normal Equation
> 
> **Note:** [8:00 to 8:44 - The design matrix X (in the bottom right side of the slide) given in the example should have elements x with subscript 1 and superscripts varying from 1 to m because for all m training sets there are only 2 features x0x_0x0​ and x1x_1x1​. 12:56 - The X matrix is m by (n+1) and NOT n by n. ]
> 
> Gradient descent gives one way of minimizing J. Let’s discuss a second way of doing so, this time performing the minimization explicitly and without resorting to an iterative algorithm. In the "Normal Equation" method, we will minimize J by explicitly taking its derivatives with respect to the θj ’s, and setting them to zero. This allows us to find the optimum theta without iteration. The normal equation formula is given below:
> 
> θ=(XTX)−1XTy\theta = (X^T X)^{-1}X^T yθ=(XTX)−1XTy
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/dykma6dwEea3qApInhZCFg_333df5f11086fee19c4fb81bc34d5125_Screenshot-2016-11-10-10.06.16.png?expiry=1591574400000&hmac=gYKck-11eMb5coUT44jvVyJMTT7LOxcYp6xQ1_iyaD4)
> 
> There is **no need** to do feature scaling with the normal equation.
> 
> The following is a comparison of gradient descent and the normal equation:
> 
> Gradient DescentNormal EquationNeed to choose alphaNo need to choose alphaNeeds many iterationsNo need to iterateO (kn2kn^2kn2)O (n3n^3n3), need to calculate inverse of XTXX^TXXTXWorks well when n is largeSlow if n is very large
> 
> With the normal equation, computing the inversion has complexity O(n3)\mathcal{O}(n^3)O(n3). So if we have a very large number of features, the normal equation will be slow. In practice, when n exceeds 10,000 it might be a good time to go from a normal solution to an iterative process.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/bjjZW/normal-equation#main
