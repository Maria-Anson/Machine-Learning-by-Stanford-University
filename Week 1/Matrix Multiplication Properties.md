# Matrix Multiplication Properties
> 
> *   Matrices are not commutative: A∗B≠B∗AA∗B \neq B∗AA∗B​=B∗A
> *   Matrices are associative: (A∗B)∗C=A∗(B∗C)(A∗B)∗C = A∗(B∗C)(A∗B)∗C=A∗(B∗C)
> 
> The **identity matrix**, when multiplied by any matrix of the same dimensions, results in the original matrix. It's just like multiplying numbers by 1\. The identity matrix simply has 1's on the diagonal (upper left to lower right diagonal) and 0's elsewhere.
> 
> [100010001]
> 
> ⎡⎣100010001⎤⎦
> 
> \begin{bmatrix} 1 & 0 & 0 \newline 0 & 1 & 0 \newline 0 & 0 & 1 \newline \end{bmatrix}[1​0​00​1​00​0​1​]
> 
> When multiplying the identity matrix after some matrix (A∗I), the square identity matrix's dimension should match the other matrix's **columns**. When multiplying the identity matrix before some other matrix (I∗A), the square identity matrix's dimension should match the other matrix's **rows**.
> 
> <pre contenteditable="false" data-language="matlab" data-evaluator-id="En9Gc7jWTMa_RnO41szGWw@2" style="opacity: 1;" tabindex="0">
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
> 14
> 
> 15
> 
> 16
> 
> 17
> 
> 18
> 
> 19
> 
> 20
> 
> 21
> 
> 22
> 
> % Initialize random matrices A and B 
> 
> A = [1,2;4,5]
> 
> B = [1,1;0,2]
> 
> % Initialize a 2 by 2 identity matrix
> 
> I = eye(2)
> 
> % The above notation is the same as I = [1,0;0,1]
> 
> % What happens when we multiply I*A ? 
> 
> IA = I*A 
> 
> % How about A*I ? 
> 
> AI = A*I 
> 
> % Compute A*B 
> 
> AB = A*B 
> 
> % Is it equal to B*A? 
> 
> BA = B*A 
> 
> % Note that IA = AI but AB != BA
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
>    4   5
> 
> B =
> 
>    1   1
>    0   2
> 
> I =
> 
> Diagonal Matrix
> 
>    1   0
>    0   1
> 
> IA =
> 
>    1   2
>    4   5
> 
> AI =
> 
>    1   2
>    4   5
> 
> AB =
> 
>     1    5
>     4   14
> 
> BA =
> 
>     5    7
>     8   10
> 
> </pre>
> 
> </pre>
>
> -- https://www.coursera.org/learn/machine-learning/supplement/Xl0xT/matrix-multiplication-properties#main
