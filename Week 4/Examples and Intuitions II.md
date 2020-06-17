# Examples and Intuitions II
> 
> The Θ(1)Θ^{(1)}Θ(1) matrices for AND, NOR, and OR are:
> 
> AND:Θ(1)NOR:Θ(1)OR:Θ(1)=[−302020]=[10−20−20]=[−102020]\begin{align*}AND:\newline\Theta^{(1)} &=\begin{bmatrix}-30 & 20 & 20\end{bmatrix} \newline NOR:\newline\Theta^{(1)} &= \begin{bmatrix}10 & -20 & -20\end{bmatrix} \newline OR:\newline\Theta^{(1)} &= \begin{bmatrix}-10 & 20 & 20\end{bmatrix} \newline\end{align*}
> 
> We can combine these to get the XNOR logical operator (which gives 1 if x1x_1x1​ and x2x_2x2​ are both 0 or both 1).
> 
> ⎡⎣x0x1x2⎤⎦→⎡⎣a(2)1a(2)2⎤⎦→[a(3)]→hΘ(x)\begin{align*}\begin{bmatrix}x_0 \newline x_1 \newline x_2\end{bmatrix} \rightarrow\begin{bmatrix}a_1^{(2)} \newline a_2^{(2)} \end{bmatrix} \rightarrow\begin{bmatrix}a^{(3)}\end{bmatrix} \rightarrow h_\Theta(x)\end{align*}
> 
> For the transition between the first and second layer, we'll use a Θ(1)Θ^{(1)}Θ(1) matrix that combines the values for AND and NOR:
> 
> Θ(1)=[−30202010−20−20]\Theta^{(1)} =
> 
> [−301020−2020−20]
> 
> \begin{bmatrix}-30 & 20 & 20 \newline 10 & -20 & -20\end{bmatrix}Θ(1)=[−30​20​2010​−20​−20​]
> 
> For the transition between the second and third layer, we'll use a Θ(2)Θ^{(2)}Θ(2) matrix that uses the value for OR:
> 
> Θ(2)=[−102020]\Theta^{(2)} =
> 
> [−102020]
> 
> \begin{bmatrix}-10 & 20 & 20\end{bmatrix}Θ(2)=[−10​20​20​]
> 
> Let's write out the values for all our nodes:
> 
> a(2)=g(Θ(1)⋅x)a(3)=g(Θ(2)⋅a(2))hΘ(x)=a(3)\begin{align*}& a^{(2)} = g(\Theta^{(1)} \cdot x) \newline& a^{(3)} = g(\Theta^{(2)} \cdot a^{(2)}) \newline& h_\Theta(x) = a^{(3)}\end{align*}
> 
> And there we have the XNOR operator using a hidden layer with two nodes! The following summarizes the above algorithm:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/rag_zbGqEeaSmhJaoV5QvA_52c04a987dcb692da8979a2198f3d8d7_Screenshot-2016-11-23-10.28.41.png?expiry=1592524800000&hmac=fP7B0b2d6xGt0sJYd_Gi4JIl-6U99W5a8QIig1v45nI)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/5iqtV/examples-and-intuitions-ii#main
