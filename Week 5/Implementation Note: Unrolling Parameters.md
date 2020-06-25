# Implementation Note: Unrolling Parameters
> 
> With neural networks, we are working with sets of matrices:
> 
> Θ(1),Θ(2),Θ(3),…D(1),D(2),D(3),…\begin{align*} \Theta^{(1)}, \Theta^{(2)}, \Theta^{(3)}, \dots \newline D^{(1)}, D^{(2)}, D^{(3)}, \dots \end{align*}
> 
> In order to use optimizing functions such as "fminunc()", we will want to "unroll" all the elements and put them into one long vector:
> 
> <pre contenteditable="false" style="opacity: 1;" tabindex="0">
> 
> 
> thetaVector = [ Theta1(:); Theta2(:); Theta3(:); ]
> 
> deltaVector = [ D1(:); D2(:); D3(:) ]
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> If the dimensions of Theta1 is 10x11, Theta2 is 10x11 and Theta3 is 1x11, then we can get back our original matrices from the "unrolled" versions as follows:
> 
> <pre contenteditable="false" style="opacity: 1;" tabindex="0">
> 
> Theta1 = reshape(thetaVector(1:110),10,11)
> 
> Theta2 = reshape(thetaVector(111:220),10,11)
> 
> Theta3 = reshape(thetaVector(221:231),1,11)
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> To summarize:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/kdK7ubT2EeajLxLfjQiSjg_d35545b8d6b6940e8577b5a8d75c8657_Screenshot-2016-11-27-15.09.24.png?expiry=1593216000000&hmac=qGt_sMhzpUnBJB4aeLOoy5gFDn2Ym9DRYD3fJsJHU6M)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/v88ik/implementation-note-unrolling-parameters#main
