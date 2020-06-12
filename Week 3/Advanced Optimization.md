# Advanced Optimization
> 
> **Note:** [7:35 - '100' should be 100 instead. The value provided should be an integer and not a character string.]
> 
> "Conjugate gradient", "BFGS", and "L-BFGS" are more sophisticated, faster ways to optimize θ that can be used instead of gradient descent. We suggest that you should not write these more sophisticated algorithms yourself (unless you are an expert in numerical computing) but use the libraries instead, as they're already tested and highly optimized. Octave provides them.
> 
> We first need to provide a function that evaluates the following two functions for a given input value θ:
> 
> J(θ)∂∂θjJ(θ)\begin{align*} & J(\theta) \newline & \dfrac{\partial}{\partial \theta_j}J(\theta)\end{align*}
> 
> We can write a single function that returns both of these:
> 
> Then we can use octave's "fminunc()" optimization algorithm along with the "optimset()" function that creates an object containing the options we want to send to "fminunc()". (Note: the value for MaxIter should be an integer, not a character string - errata in the video at 7:30)
> 
> We give to the function "fminunc()" our cost function, our initial vector of theta values, and the "options" object that we created beforehand.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/cmjIc/advanced-optimization#main
