# Model Representation I
> 
> Let's examine how we will represent a hypothesis function using neural networks. At a very simple level, neurons are basically computational units that take inputs (**dendrites**) as electrical inputs (called "spikes") that are channeled to outputs (**axons**). In our model, our dendrites are like the input features x1⋯xnx_1\cdots x_nx1​⋯xn​, and the output is the result of our hypothesis function. In this model our x0x_0x0​ input node is sometimes called the "bias unit." It is always equal to 1\. In neural networks, we use the same logistic function as in classification, 11+e−θTx\frac{1}{1 + e^{-\theta^Tx}}1+e−θTx1​, yet we sometimes call it a sigmoid (logistic) **activation** function. In this situation, our "theta" parameters are sometimes called "weights".
> 
> Visually, a simplistic representation looks like:
> 
> [x0x1x2]→[]→hθ(x)
> 
> ⎡⎣x0x1x2⎤⎦
> 
> \begin{bmatrix}x_0 \newline x_1 \newline x_2 \newline \end{bmatrix}\rightarrow
> 
> [   ]
> 
> \begin{bmatrix}\ \ \ \newline \end{bmatrix}\rightarrow h_\theta(x)[x0​x1​x2​​]→[   ​]→hθ​(x)
> 
> Our input nodes (layer 1), also known as the "input layer", go into another node (layer 2), which finally outputs the hypothesis function, known as the "output layer".
> 
> We can have intermediate layers of nodes between the input and output layers called the "hidden layers."
> 
> In this example, we label these intermediate or "hidden" layer nodes a02⋯an2a^2_0 \cdots a^2_na02​⋯an2​ and call them "activation units."
> 
> a(j)i="activation" of unit i in layer jΘ(j)=matrix of weights controlling function mapping from layer j to layer j+1\begin{align*}& a_i^{(j)} = \text{"activation" of unit $i$ in layer $j$} \newline& \Theta^{(j)} = \text{matrix of weights controlling function mapping from layer $j$ to layer $j+1$}\end{align*}
> 
> If we had one hidden layer, it would look like:
> 
> [x0x1x2x3]→[a1(2)a2(2)a3(2)]→hθ(x)
> 
> ⎡⎣⎢⎢x0x1x2x3⎤⎦⎥⎥
> 
> \begin{bmatrix}x_0 \newline x_1 \newline x_2 \newline x_3\end{bmatrix}\rightarrow
> 
> ⎡⎣⎢⎢⎢a(2)1a(2)2a(2)3⎤⎦⎥⎥⎥
> 
> \begin{bmatrix}a_1^{(2)} \newline a_2^{(2)} \newline a_3^{(2)} \newline \end{bmatrix}\rightarrow h_\theta(x)[x0​x1​x2​x3​​]→[a1(2)​a2(2)​a3(2)​​]→hθ​(x)
> 
> The values for each of the "activation" nodes is obtained as follows:
> 
> a(2)1=g(Θ(1)10x0+Θ(1)11x1+Θ(1)12x2+Θ(1)13x3)a(2)2=g(Θ(1)20x0+Θ(1)21x1+Θ(1)22x2+Θ(1)23x3)a(2)3=g(Θ(1)30x0+Θ(1)31x1+Θ(1)32x2+Θ(1)33x3)hΘ(x)=a(3)1=g(Θ(2)10a(2)0+Θ(2)11a(2)1+Θ(2)12a(2)2+Θ(2)13a(2)3)\begin{align*} a_1^{(2)} = g(\Theta_{10}^{(1)}x_0 + \Theta_{11}^{(1)}x_1 + \Theta_{12}^{(1)}x_2 + \Theta_{13}^{(1)}x_3) \newline a_2^{(2)} = g(\Theta_{20}^{(1)}x_0 + \Theta_{21}^{(1)}x_1 + \Theta_{22}^{(1)}x_2 + \Theta_{23}^{(1)}x_3) \newline a_3^{(2)} = g(\Theta_{30}^{(1)}x_0 + \Theta_{31}^{(1)}x_1 + \Theta_{32}^{(1)}x_2 + \Theta_{33}^{(1)}x_3) \newline h_\Theta(x) = a_1^{(3)} = g(\Theta_{10}^{(2)}a_0^{(2)} + \Theta_{11}^{(2)}a_1^{(2)} + \Theta_{12}^{(2)}a_2^{(2)} + \Theta_{13}^{(2)}a_3^{(2)}) \newline \end{align*}
> 
> This is saying that we compute our activation nodes by using a 3×4 matrix of parameters. We apply each row of the parameters to our inputs to obtain the value for one activation node. Our hypothesis output is the logistic function applied to the sum of the values of our activation nodes, which have been multiplied by yet another parameter matrix Θ(2)\Theta^{(2)}Θ(2) containing the weights for our second layer of nodes.
> 
> Each layer gets its own matrix of weights, Θ(j)\Theta^{(j)}Θ(j).
> 
> The dimensions of these matrices of weights is determined as follows:
> 
> If network has sj units in layer j and sj+1 units in layer j+1, then Θ(j) will be of dimension sj+1×(sj+1).\text{If network has $s_j$ units in layer $j$ and $s_{j+1}$ units in layer $j+1$, then $\Theta^{(j)}$ will be of dimension $s_{j+1} \times (s_j + 1)$.}If network has sj​ units in layer j and sj+1​ units in layer j+1, then Θ(j) will be of dimension sj+1​×(sj​+1).
> 
> The +1 comes from the addition in Θ(j)\Theta^{(j)}Θ(j) of the "bias nodes," x0x_0x0​ and Θ0(j)\Theta_0^{(j)}Θ0(j)​. In other words the output nodes will not include the bias nodes while the inputs will. The following image summarizes our model representation:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0rgjYLDeEeajLxLfjQiSjg_0c07c56839f8d6e8d7b0d09acedc88fd_Screenshot-2016-11-22-10.08.51.png?expiry=1592438400000&hmac=EYuziImYIZ3XDSYewG6-ykNFeCMDhLPRqB3AB9g2NdY)
> 
> Example: If layer 1 has 2 input nodes and layer 2 has 4 activation nodes. Dimension of Θ(1)\Theta^{(1)}Θ(1) is going to be 4×3 where sj=2s_j = 2sj​=2 and sj+1=4s_{j+1} = 4sj+1​=4, so sj+1×(sj+1)=4×3s_{j+1} \times (s_j + 1) = 4 \times 3sj+1​×(sj​+1)=4×3.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/Bln5m/model-representation-i#main
