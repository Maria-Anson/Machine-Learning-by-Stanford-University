# Addition and Scalar Multiplication
> 
> Addition and subtraction are **element-wise**, so you simply add or subtract each corresponding element:
> 
> [abcd]+[wxyz]=[a+wb+xc+yd+z]
> 
> [acbd]
> 
> \begin{bmatrix} a & b \newline c & d \newline \end{bmatrix} +
> 
> [wyxz]
> 
> \begin{bmatrix} w & x \newline y & z \newline \end{bmatrix} =
> 
> [a+wc+yb+xd+z]
> 
> \begin{bmatrix} a+w & b+x \newline c+y & d+z \newline \end{bmatrix}[a​bc​d​]+[w​xy​z​]=[a+w​b+xc+y​d+z​]
> 
> Subtracting Matrices:
> 
> [abcd]−[wxyz]=[a−wb−xc−yd−z]
> 
> [acbd]
> 
> \begin{bmatrix} a & b \newline c & d \newline \end{bmatrix} -
> 
> [wyxz]
> 
> \begin{bmatrix} w & x \newline y & z \newline \end{bmatrix} =
> 
> [a−wc−yb−xd−z]
> 
> \begin{bmatrix} a-w & b-x \newline c-y & d-z \newline \end{bmatrix}[a​bc​d​]−[w​xy​z​]=[a−w​b−xc−y​d−z​]
> 
> To add or subtract two matrices, their dimensions must be **the same**.
> 
> In scalar multiplication, we simply multiply every element by the scalar value:
> 
> [abcd]∗x=[a∗xb∗xc∗xd∗x]
> 
> [acbd]
> 
> \begin{bmatrix} a & b \newline c & d \newline \end{bmatrix} * x =
> 
> [a∗xc∗xb∗xd∗x]
> 
> \begin{bmatrix} a*x & b*x \newline c*x & d*x \newline \end{bmatrix}[a​bc​d​]∗x=[a∗x​b∗xc∗x​d∗x​]
> 
> In scalar division, we simply divide every element by the scalar value:
> 
> [abcd]/x=[a/xb/xc/xd/x]
> 
> [acbd]
> 
> \begin{bmatrix} a & b \newline c & d \newline \end{bmatrix} / x =
> 
> [a/xc/xb/xd/x]
> 
> \begin{bmatrix} a /x & b/x \newline c /x & d /x \newline \end{bmatrix}[a​bc​d​]/x=[a/x​b/xc/x​d/x​]
> 
> Experiment below with the Octave/Matlab commands for matrix addition and scalar multiplication. Feel free to try out different commands. Try to write out your answers for each command before running the cell below.
> 
> <pre contenteditable="false" data-language="matlab" data-evaluator-id="vRmabkqtTdiZmm5KrX3Ydw@4" style="opacity: 1;" tabindex="0">
> 

> 
> % Initialize matrix A and B 
> 
> A = [1, 2, 4; 5, 3, 2]
> 
> B = [1, 3, 4; 1, 1, 1]
> 
> % Initialize constant s 
> 
> s = 2
> 
> % See how element-wise addition works
> 
> add_AB = A + B 
> 
> % See how element-wise subtraction works
> 
> sub_AB = A - B
> 
> % See how scalar multiplication works
> 
> mult_As = A * s
> 
> % Divide A by s
> 
> div_As = A / s
> 
> % What happens if we have a Matrix + scalar?
> 
> add_As = A + s
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> RunReset
> 
> <pre class="rc-ConsoleOutput">
> 
> A =
> 
>    1   2   4
>    5   3   2
> 
> B =
> 
>    1   3   4
>    1   1   1
> 
> s =  2
> add_AB =
> 
>    2   5   8
>    6   4   3
> 
> sub_AB =
> 
>    0  -1   0
>    4   2   1
> 
> mult_As =
> 
>     2    4    8
>    10    6    4
> 
> div_As =
> 
>    0.50000   1.00000   2.00000
>    2.50000   1.50000   1.00000
> 
> add_As =
> 
>    3   4   6
>    7   5   4
> 
> </pre>
> 
> </pre>
>
> -- https://www.coursera.org/learn/machine-learning/supplement/FenyC/addition-and-scalar-multiplication#main
