# Decision Boundary
> 
> In order to get our discrete 0 or 1 classification, we can translate the output of the hypothesis function as follows:
> 
> hθ(x)≥0.5→y=1hθ(x)<0.5→y=0\begin{align*}& h_\theta(x) \geq 0.5 \rightarrow y = 1 \newline& h_\theta(x) < 0.5 \rightarrow y = 0 \newline\end{align*}
> 
> The way our logistic function g behaves is that when its input is greater than or equal to zero, its output is greater than or equal to 0.5:
> 
> g(z)≥0.5whenz≥0\begin{align*}& g(z) \geq 0.5 \newline& when \; z \geq 0\end{align*}
> 
> Remember.
> 
> z=0,e0=1⇒g(z)=1/2z→∞,e−∞→0⇒g(z)=1z→−∞,e∞→∞⇒g(z)=0\begin{align*}z=0, e^{0}=1 \Rightarrow g(z)=1/2\newline z \to \infty, e^{-\infty} \to 0 \Rightarrow g(z)=1 \newline z \to -\infty, e^{\infty}\to \infty \Rightarrow g(z)=0 \end{align*}
> 
> So if our input to g is θTX\theta^T XθTX, then that means:
> 
> hθ(x)=g(θTx)≥0.5whenθTx≥0\begin{align*}& h_\theta(x) = g(\theta^T x) \geq 0.5 \newline& when \; \theta^T x \geq 0\end{align*}
> 
> From these statements we can now say:
> 
> θTx≥0⇒y=1θTx<0⇒y=0\begin{align*}& \theta^T x \geq 0 \Rightarrow y = 1 \newline& \theta^T x < 0 \Rightarrow y = 0 \newline\end{align*}
> 
> The **decision boundary** is the line that separates the area where y = 0 and where y = 1\. It is created by our hypothesis function.
> 
> **Example**:
> 
> θ=⎡⎣5−10⎤⎦y=1if5+(−1)x1+0x2≥05−x1≥0−x1≥−5x1≤5\begin{align*}& \theta = \begin{bmatrix}5 \newline -1 \newline 0\end{bmatrix} \newline & y = 1 \; if \; 5 + (-1) x_1 + 0 x_2 \geq 0 \newline & 5 - x_1 \geq 0 \newline & - x_1 \geq -5 \newline& x_1 \leq 5 \newline \end{align*}
> 
> In this case, our decision boundary is a straight vertical line placed on the graph where x1=5x_1 = 5x1​=5, and everything to the left of that denotes y = 1, while everything to the right denotes y = 0.
> 
> Again, the input to the sigmoid function g(z) (e.g. θTX\theta^T XθTX) doesn't need to be linear, and could be a function that describes a circle (e.g. z=θ0+θ1x12+θ2x22z = \theta_0 + \theta_1 x_1^2 +\theta_2 x_2^2z=θ0​+θ1​x12​+θ2​x22​) or any shape to fit our data.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/N8qsm/decision-boundary#main
