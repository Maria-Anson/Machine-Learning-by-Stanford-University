# Gradient Descent Intuition
 
 In this video we explored the scenario where we used one parameter θ1\theta_1θ1​ and plotted its cost function to implement a gradient descent. Our formula for a single parameter was :
 
 Repeat until convergence:
 
 θ1:=θ1−αd/dθ1J(θ1)
 
 Regardless of the slope's sign for d/dθ1J(θ1), θ1 eventually converges to its minimum value. The following graph shows that when the slope is negative, the value of θ1\theta_1θ1​ increases and when it is positive, the value of θ1\theta_1θ1​ decreases.
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/SMSIxKGUEeav5QpTGIv-Pg_ad3404010579ac16068105cfdc8e950a_Screenshot-2016-11-03-00.05.06.png?expiry=1591228800000&hmac=QddmMWO9_08HbI_Y8DzS9x0LPzrpF-UW-4ewHjXOBWA)
 
 On a side note, we should adjust our parameter α\alphaα to ensure that the gradient descent algorithm converges in a reasonable time. Failure to converge or too much time to obtain the minimum value imply that our step size is wrong.
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UJpiD6GWEeai9RKvXdDYag_3c3ad6625a2a4ec8456f421a2f4daf2e_Screenshot-2016-11-03-00.05.27.png?expiry=1591228800000&hmac=TKIkFPhe88c541_Lx3Umd939GB5sRteNEjUI1aidWfQ)
 
 ### How does gradient descent converge with a fixed step size α\alphaα?
 
 The intuition behind the convergence is that ddθ1J(θ1)\frac{d}{d\theta_1} J(\theta_1)dθ1​d​J(θ1​) approaches 0 as we approach the bottom of our convex function. At the minimum, the derivative will always be 0 and thus we get:
 
 θ1:=θ1−α∗0![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RDcJ-KGXEeaVChLw2Vaaug_cb782d34d272321e88f202940c36afe9_Screenshot-2016-11-03-00.06.00.png?expiry=1591228800000&hmac=LtnJv2LQZA2etawpO56a5l4LYe9u_5Ehl56XK5Gr7Hc)

 -- https://www.coursera.org/learn/machine-learning/supplement/QKEdR/gradient-descent-intuition#main
