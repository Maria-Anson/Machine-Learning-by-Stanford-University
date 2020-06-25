# Backpropagation Algorithm
> 
> "Backpropagation" is neural-network terminology for minimizing our cost function, just like what we were doing with gradient descent in logistic and linear regression. Our goal is to compute:
> 
> min⁡ΘJ(Θ)\min_\Theta J(\Theta)minΘ​J(Θ)
> 
> That is, we want to minimize our cost function J using an optimal set of parameters in theta. In this section we'll look at the equations we use to compute the partial derivative of J(Θ):
> 
> ∂∂Θi,j(l)J(Θ)\dfrac{\partial}{\partial \Theta_{i,j}^{(l)}}J(\Theta)∂Θi,j(l)​∂​J(Θ)
> 
> To do so, we use the following algorithm:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Ul6i5teoEea1UArqXEX_3g_a36fb24a11c744d7552f0fecf2fdd752_Screenshot-2017-01-10-17.13.27.png?expiry=1593216000000&hmac=iPFx67OscJmk4yjcjjjFie9NH7comjk2N3LwNwWary8)
> 
> **Back propagation Algorithm**
> 
> Given training set {(x(1),y(1))⋯(x(m),y(m))}\lbrace (x^{(1)}, y^{(1)}) \cdots (x^{(m)}, y^{(m)})\rbrace{(x(1),y(1))⋯(x(m),y(m))}
> 
> *   Set Δi,j(l)\Delta^{(l)}_{i,j}Δi,j(l)​ := 0 for all (l,i,j), (hence you end up having a matrix full of zeros)
> 
> For training example t =1 to m:
> 
> 1.  Set a(1):=x(t)a^{(1)} := x^{(t)}a(1):=x(t)
> 2.  Perform forward propagation to compute a(l)a^{(l)}a(l) for l=2,3,…,L
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bYLgwteoEeaX9Qr89uJd1A_73f280ff78695f84ae512f19acfa29a3_Screenshot-2017-01-10-18.16.50.png?expiry=1593216000000&hmac=xOutpnOeWu0SVFeOA2MMv_7Qwr6qhJSnfYkjPY5VyMQ)
> 
> 3\. Using y(t)y^{(t)}y(t), compute δ(L)=a(L)−y(t)\delta^{(L)} = a^{(L)} - y^{(t)}δ(L)=a(L)−y(t)
> 
> Where L is our total number of layers and a(L)a^{(L)}a(L) is the vector of outputs of the activation units for the last layer. So our "error values" for the last layer are simply the differences of our actual results in the last layer and the correct outputs in y. To get the delta values of the layers before the last layer, we can use an equation that steps us back from right to left:
> 
> 4\. Compute δ(L−1),δ(L−2),…,δ(2)\delta^{(L-1)}, \delta^{(L-2)},\dots,\delta^{(2)}δ(L−1),δ(L−2),…,δ(2) using δ(l)=((Θ(l))Tδ(l+1)).∗a(l).∗(1−a(l))\delta^{(l)} = ((\Theta^{(l)})^T \delta^{(l+1)})\ .*\ a^{(l)}\ .*\ (1 - a^{(l)})δ(l)=((Θ(l))Tδ(l+1)) .∗ a(l) .∗ (1−a(l))
> 
> The delta values of layer l are calculated by multiplying the delta values in the next layer with the theta matrix of layer l. We then element-wise multiply that with a function called g', or g-prime, which is the derivative of the activation function g evaluated with the input values given by z(l)z^{(l)}z(l).
> 
> The g-prime derivative terms can also be written out as:
> 
> g′(z(l))=a(l).∗(1−a(l))g'(z^{(l)}) = a^{(l)}\ .*\ (1 - a^{(l)})g′(z(l))=a(l) .∗ (1−a(l))
> 
> 5\. Δi,j(l):=Δi,j(l)+aj(l)δi(l+1)\Delta^{(l)}_{i,j} := \Delta^{(l)}_{i,j} + a_j^{(l)} \delta_i^{(l+1)}Δi,j(l)​:=Δi,j(l)​+aj(l)​δi(l+1)​ or with vectorization, Δ(l):=Δ(l)+δ(l+1)(a(l))T\Delta^{(l)} := \Delta^{(l)} + \delta^{(l+1)}(a^{(l)})^TΔ(l):=Δ(l)+δ(l+1)(a(l))T
> 
> Hence we update our new Δ\DeltaΔ matrix.
> 
> *   Di,j(l):=1m(Δi,j(l)+λΘi,j(l))D^{(l)}_{i,j} := \dfrac{1}{m}\left(\Delta^{(l)}_{i,j} + \lambda\Theta^{(l)}_{i,j}\right)Di,j(l)​:=m1​(Δi,j(l)​+λΘi,j(l)​), if j≠0.
> *   Di,j(l):=1mΔi,j(l)D^{(l)}_{i,j} := \dfrac{1}{m}\Delta^{(l)}_{i,j}Di,j(l)​:=m1​Δi,j(l)​ If j=0
> 
> The capital-delta matrix D is used as an "accumulator" to add up our values as we go along and eventually compute our partial derivative. Thus we get ∂∂Θij(l)J(Θ)\frac \partial {\partial \Theta_{ij}^{(l)}} J(\Theta)∂Θij(l)​∂​J(Θ)= Dij(l)D_{ij}^{(l)}Dij(l)​
>
> -- https://www.coursera.org/learn/machine-learning/supplement/pjdBA/backpropagation-algorithm#main
