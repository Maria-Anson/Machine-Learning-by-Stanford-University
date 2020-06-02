# Inverse and Transpose
> 
> The **inverse** of a matrix A is denoted A−1A^{-1}A−1. Multiplying by the inverse results in the identity matrix.
> 
> A non square matrix does not have an inverse matrix. We can compute inverses of matrices in octave with the pinv(A)pinv(A)pinv(A) function and in Matlab with the inv(A)inv(A)inv(A) function. Matrices that don't have an inverse are _singular_ or _degenerate_.
> 
> The **transposition** of a matrix is like rotating the matrix 90**°** in clockwise direction and then reversing it. We can compute transposition of matrices in matlab with the transpose(A) function or A':
> 
> A=[abcdef]A =
> 
> ⎡⎣acebdf⎤⎦
> 
> \begin{bmatrix} a & b \newline c & d \newline e & f \end{bmatrix}A=[a​bc​de​f​]AT=[acebdf]A^T =
> 
> [abcdef]
> 
> \begin{bmatrix} a & c & e \newline b & d & f \newline \end{bmatrix}AT=[a​c​eb​d​f​]
> 
> In other words:
> 
> Aij=AjiTA_{ij} = A^T_{ji}Aij​=AjiT​
> 
> <pre contenteditable="false" data-language="matlab" data-evaluator-id="zx33eOHKTvid93jhyo74zQ@2" style="opacity: 1;" tabindex="0">
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
> 11
> 
> 12
> 
> 13
> 
> % Initialize matrix A 
> 
> A = [1,2,0;0,5,6;7,0,9]
> 
> % Transpose A 
> 
> A_trans = A' 
> 
> % Take the inverse of A 
> 
> A_inv = inv(A)
> 
> % What is A^(-1)*A? 
> 
> A_invA = inv(A)*A
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> RunReset
> 
> <pre class="rc-ConsoleOutput">
> 
> A =
> 
>    1   2   0
>    0   5   6
>    7   0   9
> 
> A_trans =
> 
>    1   0   7
>    2   5   0
>    0   6   9
> 
> A_inv =
> 
>    0.348837  -0.139535   0.093023
>    0.325581   0.069767  -0.046512
>   -0.271318   0.108527   0.038760
> 
> A_invA =
> 
>    1.00000  -0.00000   0.00000
>    0.00000   1.00000  -0.00000
>   -0.00000   0.00000   1.00000
> 
> </pre>
> 
> </pre>
>
> -- https://www.coursera.org/learn/machine-learning/supplement/EcNto/inverse-and-transpose#main
