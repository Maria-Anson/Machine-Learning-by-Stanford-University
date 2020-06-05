 # Multiple Features
> 
> **Note:** [7:25 - θT\theta^TθT is a 1 by (n+1) matrix and not an (n+1) by 1 matrix]
> 
> Linear regression with multiple variables is also known as "multivariate linear regression".
> 
> We now introduce notation for equations where we can have any number of input variables.
> 
> x(i)jx(i)mn=value of feature j in the ith training example=the input (features) of the ith training example=the number of training examples=the number of features\begin{align*}x_j^{(i)} &= \text{value of feature } j \text{ in the }i^{th}\text{ training example} \newline x^{(i)}& = \text{the input (features) of the }i^{th}\text{ training example} \newline m &= \text{the number of training examples} \newline n &= \text{the number of features} \end{align*}
> 
> The multivariable form of the hypothesis function accommodating these multiple features is as follows:
> 
> hθ(x)=θ0+θ1x1+θ2x2+θ3x3+⋯+θnxnh_\theta (x) = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \theta_3 x_3 + \cdots + \theta_n x_nhθ​(x)=θ0​+θ1​x1​+θ2​x2​+θ3​x3​+⋯+θn​xn​
> 
> In order to develop intuition about this function, we can think about θ0\theta_0θ0​ as the basic price of a house, θ1\theta_1θ1​ as the price per square meter, θ2\theta_2θ2​ as the price per floor, etc. x1x_1x1​ will be the number of square meters in the house, x2x_2x2​ the number of floors, etc.
> 
> Using the definition of matrix multiplication, our multivariable hypothesis function can be concisely represented as:
> 
> hθ(x)=[θ0θ1...θn]⎡⎣⎢⎢⎢x0x1⋮xn⎤⎦⎥⎥⎥=θTx\begin{align*}h_\theta(x) =\begin{bmatrix}\theta_0 \hspace{2em} \theta_1 \hspace{2em} ... \hspace{2em} \theta_n\end{bmatrix}\begin{bmatrix}x_0 \newline x_1 \newline \vdots \newline x_n\end{bmatrix}= \theta^T x\end{align*}
> 
> This is a vectorization of our hypothesis function for one training example; see the lessons on vectorization to learn more.
> 
> Remark: Note that for convenience reasons in this course we assume x0(i)=1 for (i∈1,…,m)x_{0}^{(i)} =1 \text{ for } (i\in { 1,\dots, m } )x0(i)​=1 for (i∈1,…,m). This allows us to do matrix operations with theta and x. Hence making the two vectors 'θ\thetaθ' and x(i)x^{(i)}x(i) match each other element-wise (that is, have the same number of elements: n+1).]
>
> -- https://www.coursera.org/learn/machine-learning/supplement/WKgbA/multiple-features#main
