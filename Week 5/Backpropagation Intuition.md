# Backpropagation Intuition
> 
> **Note:** [4:39, the last term for the calculation for z13z^3_1z13​ (three-color handwritten formula) should be a22a^2_2a22​ instead of a12a^2_1a12​. 6:08 - the equation for cost(i) is incorrect. The first term is missing parentheses for the log() function, and the second term should be (1−y(i))log⁡(1−hθ(x(i)))(1-y^{(i)})\log(1-h{_\theta}{(x^{(i)}}))(1−y(i))log(1−hθ​(x(i))). 8:50 - δ(4)=y−a(4)\delta^{(4)} = y - a^{(4)}δ(4)=y−a(4) is incorrect and should be δ(4)=a(4)−y\delta^{(4)} = a^{(4)} - yδ(4)=a(4)−y.]
> 
> Recall that the cost function for a neural network is:
> 
> J(Θ)=−1m∑t=1m∑k=1K[y(t)k log(hΘ(x(t)))k+(1−y(t)k) log(1−hΘ(x(t))k)]+λ2m∑l=1L−1∑i=1sl∑j=1sl+1(Θ(l)j,i)2\begin{gather*}J(\Theta) = - \frac{1}{m} \sum_{t=1}^m\sum_{k=1}^K \left[ y^{(t)}_k \ \log (h_\Theta (x^{(t)}))_k + (1 - y^{(t)}_k)\ \log (1 - h_\Theta(x^{(t)})_k)\right] + \frac{\lambda}{2m}\sum_{l=1}^{L-1} \sum_{i=1}^{s_l} \sum_{j=1}^{s_l+1} ( \Theta_{j,i}^{(l)})^2\end{gather*}
> 
> If we consider simple non-multiclass classification (k = 1) and disregard regularization, the cost is computed with:
> 
> cost(t)=y(t)log⁡(hΘ(x(t)))+(1−y(t))log⁡(1−hΘ(x(t)))cost(t) =y^{(t)} \ \log (h_\Theta (x^{(t)})) + (1 - y^{(t)})\ \log (1 - h_\Theta(x^{(t)}))cost(t)=y(t) log(hΘ​(x(t)))+(1−y(t)) log(1−hΘ​(x(t)))
> 
> Intuitively, δj(l)\delta_j^{(l)}δj(l)​ is the "error" for aj(l)a^{(l)}_jaj(l)​ (unit j in layer l). More formally, the delta values are actually the derivative of the cost function:
> 
> δj(l)=∂∂zj(l)cost(t)\delta_j^{(l)} = \dfrac{\partial}{\partial z_j^{(l)}} cost(t)δj(l)​=∂zj(l)​∂​cost(t)
> 
> Recall that our derivative is the slope of a line tangent to the cost function, so the steeper the slope the more incorrect we are. Let us consider the following neural network below and see how we could calculate some δj(l)\delta_j^{(l)}δj(l)​:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qc309rdcEea4MxKdJPaTxA_324034f1a3c3a3be8e7c6cfca90d3445_fixx.png?expiry=1593216000000&hmac=d4LtmG-slXry-EG-4QCzOyF0CHwvFvKzNptz2GHW4hA)
> 
> In the image above, to calculate δ2(2)\delta_2^{(2)}δ2(2)​, we multiply the weights Θ12(2)\Theta_{12}^{(2)}Θ12(2)​ and Θ22(2)\Theta_{22}^{(2)}Θ22(2)​ by their respective δ\deltaδ values found to the right of each edge. So we get δ2(2)\delta_2^{(2)}δ2(2)​= Θ12(2)\Theta_{12}^{(2)}Θ12(2)​*δ1(3)\delta_1^{(3)}δ1(3)​+Θ22(2)\Theta_{22}^{(2)}Θ22(2)​*δ2(3)\delta_2^{(3)}δ2(3)​. To calculate every single possible δj(l)\delta_j^{(l)}δj(l)​, we could start from the right of our diagram. We can think of our edges as our Θij\Theta_{ij}Θij​. Going from right to left, to calculate the value of δj(l)\delta_j^{(l)}δj(l)​, you can just take the over all sum of each weight times the δ\deltaδ it is coming from. Hence, another example would be δ2(3)\delta_2^{(3)}δ2(3)​=Θ12(3)\Theta_{12}^{(3)}Θ12(3)​*δ1(4)\delta_1^{(4)}δ1(4)​.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/v5Bu8/backpropagation-intuition#main
