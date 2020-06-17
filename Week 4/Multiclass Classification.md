# Multiclass Classification
> 
> To classify data into multiple classes, we let our hypothesis function return a vector of values. Say we wanted to classify our data into one of four categories. We will use the following example to see how this classification is done. This algorithm takes as input an image and classifies it accordingly:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9Aeo6bGtEea4MxKdJPaTxA_4febc7ec9ac9dd0e4309bd1778171d36_Screenshot-2016-11-23-10.49.05.png?expiry=1592524800000&hmac=x4AuPaLtwVpbAndh1EPTZk5wsfaWLxS69alpqrvihuY)
> 
> We can define our set of resulting classes as y:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/KBpHLXqiEealOA67wFuqoQ_95654ff11df1261d935ab00553d724e5_Screenshot-2016-09-14-10.38.27.png?expiry=1592524800000&hmac=1sX7uSozdfgXWabir2H7RC4tB8lHoGz1Lurz_VuINZg)
> 
> Each y(i)y^{(i)}y(i) represents a different image corresponding to either a car, pedestrian, truck, or motorcycle. The inner layers, each provide us with some new information which leads to our final hypothesis function. The setup looks like:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/VBxpV7GvEeamBAoLccicqA_3e7f67888330b131426ecffd27936f61_Screenshot-2016-11-23-10.59.19.png?expiry=1592524800000&hmac=I_Whrf17E6xJMwPrOpNWTRq1a484lwUHU2qBnKWiX_Y)
> 
> Our resulting hypothesis for one set of inputs may look like:
> 
> hΘ(x)=[0010]h_\Theta(x) =
> 
> ⎡⎣⎢⎢0010⎤⎦⎥⎥
> 
> \begin{bmatrix}0 \newline 0 \newline 1 \newline 0 \newline\end{bmatrix}hΘ​(x)=[0010​]
> 
> In which case our resulting class is the third one down, or hΘ(x)3h_\Theta(x)_3hΘ​(x)3​, which represents the motorcycle.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/xSUml/multiclass-classification#main
