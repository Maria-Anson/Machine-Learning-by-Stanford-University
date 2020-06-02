 # Matrix-Vector Multiplication
> 
> We map the column of the vector onto each row of the matrix, multiplying each element and summing the result.
> 
> [abcdef]∗[xy]=[a∗x+b∗yc∗x+d∗ye∗x+f∗y]
> 
> ⎡⎣acebdf⎤⎦
> 
> \begin{bmatrix} a & b \newline c & d \newline e & f \end{bmatrix} *
> 
> [xy]
> 
> \begin{bmatrix} x \newline y \newline \end{bmatrix} =
> 
> ⎡⎣⎢a∗x+b∗yc∗x+d∗ye∗x+f∗y⎤⎦⎥
> 
> \begin{bmatrix} a*x + b*y \newline c*x + d*y \newline e*x + f*y\end{bmatrix}[a​bc​de​f​]∗[xy​]=[a∗x+b∗yc∗x+d∗ye∗x+f∗y​]
> 
> The result is a **vector**. The number of **columns** of the matrix must equal the number of **rows** of the vector.
> 
> An **m x n matrix** multiplied by an **n x 1 vector** results in an **m x 1 vector**.
> 
> Below is an example of a matrix-vector multiplication. Make sure you understand how the multiplication works. Feel free to try different matrix-vector multiplications.
> 
> <pre contenteditable="false" data-language="matlab" data-evaluator-id="n48TWVmsQlePE1lZrHJXwA@2" style="opacity: 1;" tabindex="0">
> 
> 1
> 
> 2
> 
> 3
> 
> 4
> 
> 5
> 
> 6
> 
> 7
> 
> 8
> 
> 9
> 
> 10
> 
> % Initialize matrix A 
> 
> A = [1, 2, 3; 4, 5, 6;7, 8, 9] 
> 
> % Initialize vector v 
> 
> v = [1; 1; 1] 
> 
> % Multiply A * v
> 
> Av = A * v
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> RunReset
> 
> <pre class="rc-ConsoleOutput">
> 
> A =
> 
>    1   2   3
>    4   5   6
>    7   8   9
> 
> v =
> 
>    1
>    1
>    1
> 
> Av =
> 
>     6
>    15
>    24
> 
> </pre>
> 
> </pre>
>
> -- https://www.coursera.org/learn/machine-learning/supplement/cgVgM/matrix-vector-multiplication#main
