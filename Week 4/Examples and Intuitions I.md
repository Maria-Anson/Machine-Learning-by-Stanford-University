# Examples and Intuitions I
> 
> A simple example of applying neural networks is by predicting x1x_1x1​ AND x2x_2x2​, which is the logical 'and' operator and is only true if both x1x_1x1​ and x2x_2x2​ are 1.
> 
> The graph of our functions will look like:
> 
> ⎡⎣x0x1x2⎤⎦→[g(z(2))]→hΘ(x)\begin{align*}\begin{bmatrix}x_0 \newline x_1 \newline x_2\end{bmatrix} \rightarrow\begin{bmatrix}g(z^{(2)})\end{bmatrix} \rightarrow h_\Theta(x)\end{align*}
> 
> Remember that x0x_0x0​ is our bias variable and is always 1.
> 
> Let's set our first theta matrix as:
> 
> Θ(1)=[−302020]\Theta^{(1)} =
> 
> [−302020]
> 
> \begin{bmatrix}-30 & 20 & 20\end{bmatrix}Θ(1)=[−30​20​20​]
> 
> This will cause the output of our hypothesis to only be positive if both x1x_1x1​ and x2x_2x2​ are 1\. In other words:
> 
> hΘ(x)=g(−30+20x1+20x2)x1=0  and  x2=0  then  g(−30)≈0x1=0  and  x2=1  then  g(−10)≈0x1=1  and  x2=0  then  g(−10)≈0x1=1  and  x2=1  then  g(10)≈1\begin{align*}& h_\Theta(x) = g(-30 + 20x_1 + 20x_2) \newline \newline & x_1 = 0 \ \ and \ \ x_2 = 0 \ \ then \ \ g(-30) \approx 0 \newline & x_1 = 0 \ \ and \ \ x_2 = 1 \ \ then \ \ g(-10) \approx 0 \newline & x_1 = 1 \ \ and \ \ x_2 = 0 \ \ then \ \ g(-10) \approx 0 \newline & x_1 = 1 \ \ and \ \ x_2 = 1 \ \ then \ \ g(10) \approx 1\end{align*}
> 
> So we have constructed one of the fundamental operations in computers by using a small neural network rather than using an actual AND gate. Neural networks can also be used to simulate all the other logical gates. The following is an example of the logical operator 'OR', meaning either x1x_1x1​ is true or x2x_2x2​ is true, or both:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/f_ueJLGnEea3qApInhZCFg_a5ff8edc62c9a09900eae075e8502e34_Screenshot-2016-11-23-10.03.48.png?expiry=1592524800000&hmac=-M2_dPRLnA-9rU9rVl42e5LZYGbTct-9LEhtIWOG-cM)
> 
> Where g(z) is the following:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wMOiMrGnEeajLxLfjQiSjg_bbbdad80f5c95068bde7c9134babdd77_Screenshot-2016-11-23-10.07.24.png?expiry=1592524800000&hmac=wquMBRUGMTQ3tnhoRgfaF0s_Q1pG4kHpcyLo0F7tkd0)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/kivO9/examples-and-intuitions-i#main
