# Matrix-Matrix Multiplication
> 
> We multiply two matrices by breaking it into several vector multiplications and concatenating the result.
> 
> [abcdef]∗[wxyz]=[a∗w+b∗ya∗x+b∗zc∗w+d∗yc∗x+d∗ze∗w+f∗ye∗x+f∗z]
> 
> ⎡⎣acebdf⎤⎦
> 
> \begin{bmatrix} a & b \newline c & d \newline e & f \end{bmatrix} *
> 
> [wyxz]
> 
> \begin{bmatrix} w & x \newline y & z \newline \end{bmatrix} =
> 
> ⎡⎣⎢a∗w+b∗yc∗w+d∗ye∗w+f∗ya∗x+b∗zc∗x+d∗ze∗x+f∗z⎤⎦⎥
> 
> \begin{bmatrix} a*w + b*y & a*x + b*z \newline c*w + d*y & c*x + d*z \newline e*w + f*y & e*x + f*z\end{bmatrix}[a​bc​de​f​]∗[w​xy​z​]=[a∗w+b∗y​a∗x+b∗zc∗w+d∗y​c∗x+d∗ze∗w+f∗y​e∗x+f∗z​]
> 
> An **m x n matrix** multiplied by an **n x o matrix** results in an **m x o** matrix. In the above example, a 3 x 2 matrix times a 2 x 2 matrix resulted in a 3 x 2 matrix.
> 
> To multiply two matrices, the number of **columns** of the first matrix must equal the number of **rows** of the second matrix.
> 
> For example:
> 
> <pre contenteditable="false" data-language="matlab" data-evaluator-id="Ts_2-gEwQxOP9voBMPMTbw@2" style="opacity: 1;" tabindex="0">
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
> % Initialize a 3 by 2 matrix 
> 
> A = [1, 2; 3, 4;5, 6]
> 
> % Initialize a 2 by 1 matrix 
> 
> B = [1; 2] 
> 
> % We expect a resulting matrix of (3 by 2)*(2 by 1) = (3 by 1) 
> 
> mult_AB = A*B
> 
> % Make sure you understand why we got that result
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> RunReset
> 
> <pre class="rc-ConsoleOutput">
> 
> A =
> 
>    1   2
>    3   4
>    5   6
> 
> B =
> 
>    1
>    2
> 
> mult_AB =
> 
>     5
>    11
>    17
> 
> </pre>
> 
> </pre>
>
> -- https://www.coursera.org/learn/machine-learning/supplement/l0myT/matrix-matrix-multiplication#main
