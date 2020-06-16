# Model Representation II
> 
> To re-iterate, the following is an example of a neural network:
> 
> a(2)1=g(Θ(1)10x0+Θ(1)11x1+Θ(1)12x2+Θ(1)13x3)a(2)2=g(Θ(1)20x0+Θ(1)21x1+Θ(1)22x2+Θ(1)23x3)a(2)3=g(Θ(1)30x0+Θ(1)31x1+Θ(1)32x2+Θ(1)33x3)hΘ(x)=a(3)1=g(Θ(2)10a(2)0+Θ(2)11a(2)1+Θ(2)12a(2)2+Θ(2)13a(2)3)\begin{align*} a_1^{(2)} = g(\Theta_{10}^{(1)}x_0 + \Theta_{11}^{(1)}x_1 + \Theta_{12}^{(1)}x_2 + \Theta_{13}^{(1)}x_3) \newline a_2^{(2)} = g(\Theta_{20}^{(1)}x_0 + \Theta_{21}^{(1)}x_1 + \Theta_{22}^{(1)}x_2 + \Theta_{23}^{(1)}x_3) \newline a_3^{(2)} = g(\Theta_{30}^{(1)}x_0 + \Theta_{31}^{(1)}x_1 + \Theta_{32}^{(1)}x_2 + \Theta_{33}^{(1)}x_3) \newline h_\Theta(x) = a_1^{(3)} = g(\Theta_{10}^{(2)}a_0^{(2)} + \Theta_{11}^{(2)}a_1^{(2)} + \Theta_{12}^{(2)}a_2^{(2)} + \Theta_{13}^{(2)}a_3^{(2)}) \newline \end{align*}
> 
> In this section we'll do a vectorized implementation of the above functions. We're going to define a new variable zk(j)z_k^{(j)}zk(j)​ that encompasses the parameters inside our g function. In our previous example if we replaced by the variable z for all the parameters we would get:
> 
> a(2)1=g(z(2)1)a(2)2=g(z(2)2)a(2)3=g(z(2)3)\begin{align*}a_1^{(2)} = g(z_1^{(2)}) \newline a_2^{(2)} = g(z_2^{(2)}) \newline a_3^{(2)} = g(z_3^{(2)}) \newline \end{align*}
> 
> In other words, for layer j=2 and node k, the variable z will be:
> 
> zk(2)=Θk,0(1)x0+Θk,1(1)x1+⋯+Θk,n(1)xnz_k^{(2)} = \Theta_{k,0}^{(1)}x_0 + \Theta_{k,1}^{(1)}x_1 + \cdots + \Theta_{k,n}^{(1)}x_nzk(2)​=Θk,0(1)​x0​+Θk,1(1)​x1​+⋯+Θk,n(1)​xn​
> 
> The vector representation of x and zjz^{j}zj is:
> 
> x=⎡⎣⎢⎢x0x1⋯xn⎤⎦⎥⎥z(j)=⎡⎣⎢⎢⎢⎢z(j)1z(j)2⋯z(j)n⎤⎦⎥⎥⎥⎥\begin{align*}x = \begin{bmatrix}x_0 \newline x_1 \newline\cdots \newline x_n\end{bmatrix} &z^{(j)} = \begin{bmatrix}z_1^{(j)} \newline z_2^{(j)} \newline\cdots \newline z_n^{(j)}\end{bmatrix}\end{align*}
> 
> Setting x=a(1)x = a^{(1)}x=a(1), we can rewrite the equation as:
> 
> z(j)=Θ(j−1)a(j−1)z^{(j)} = \Theta^{(j-1)}a^{(j-1)}z(j)=Θ(j−1)a(j−1)
> 
> We are multiplying our matrix Θ(j−1)\Theta^{(j-1)}Θ(j−1) with dimensions sj×(n+1)s_j\times (n+1)sj​×(n+1) (where sjs_jsj​ is the number of our activation nodes) by our vector a(j−1)a^{(j-1)}a(j−1) with height (n+1). This gives us our vector z(j)z^{(j)}z(j) with height sjs_jsj​. Now we can get a vector of our activation nodes for layer j as follows:
> 
> a(j)=g(z(j))a^{(j)} = g(z^{(j)})a(j)=g(z(j))
> 
> Where our function g can be applied element-wise to our vector z(j)z^{(j)}z(j).
> 
> We can then add a bias unit (equal to 1) to layer j after we have computed a(j)a^{(j)}a(j). This will be element a0(j)a_0^{(j)}a0(j)​ and will be equal to 1\. To compute our final hypothesis, let's first compute another z vector:
> 
> z(j+1)=Θ(j)a(j)z^{(j+1)} = \Theta^{(j)}a^{(j)}z(j+1)=Θ(j)a(j)
> 
> We get this final z vector by multiplying the next theta matrix after Θ(j−1)\Theta^{(j-1)}Θ(j−1) with the values of all the activation nodes we just got. This last theta matrix Θ(j)\Theta^{(j)}Θ(j) will have only **one row** which is multiplied by one column a(j)a^{(j)}a(j) so that our result is a single number. We then get our final result with:
> 
> hΘ(x)=a(j+1)=g(z(j+1))h_\Theta(x) = a^{(j+1)} = g(z^{(j+1)})hΘ​(x)=a(j+1)=g(z(j+1))
> 
> Notice that in this **last step**, between layer j and layer j+1, we are doing **exactly the same thing** as we did in logistic regression. Adding all these intermediate layers in neural networks allows us to more elegantly produce interesting and more complex non-linear hypotheses.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/YlEVx/model-representation-ii#main
