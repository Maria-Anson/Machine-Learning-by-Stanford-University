# Octave/Matlab Tutorial
> 
> Total points 5
> 
>  1.Question 1
> 
> Suppose I first execute the following in Octave/Matlab:
> 
> <pre contenteditable="false" data-language="matlab" style="opacity: 1;" tabindex="0">
> 
> 1
> 
> 2
> 
> A = [1 2; 3 4; 5 6];
> 
> B = [1 2 3; 4 5 6];
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> Which of the following are then valid commands? Check all that apply. (Hint: A' denotes the transpose of A.)
> 
> 1 point 
> 

      C = A' + B; 
> 

      C = B * A; 
> 
>  C = A + B; 
> 
>  C = B' * A; 
> 
>  2.Question 2
> 
> Let A=[16231351110897612414151]A =
> 
> ⎡⎣⎢⎢16594211714310615138121⎤⎦⎥⎥
> 
> \begin{bmatrix} 16 & 2 & 3 & 13 \\ 5 & 11 & 10 & 8 \\ 9 & 7 & 6 & 12 \\ 4 & 14 & 15 & 1 \end{bmatrix} A=⎣⎢⎢⎢⎡​16594​211714​310615​138121​⎦⎥⎥⎥⎤​.
> 
> Which of the following indexing expressions gives B=[16251197414]B =
> 
> ⎡⎣⎢⎢16594211714⎤⎦⎥⎥
> 
> \begin{bmatrix} 16 & 2 \\ 5 & 11 \\ 9 & 7 \\ 4 & 14 \end{bmatrix} B=⎣⎢⎢⎢⎡​16594​211714​⎦⎥⎥⎥⎤​? Check all that apply.
> 
> 1 point 
> 

      B = A(:, 1:2); 
> 

      B = A(1:4, 1:2); 
> 
>  B = A(0:2, 0:4) 
> 
>  B = A(1:2, 1:4); 
> 
>  3.Question 3
> 
> Let AAA be a 10x10 matrix andxxx be a 10-element vector. Your friend wants to compute the product AxAxAx and writes the following code:
> 
> <pre contenteditable="false" data-language="matlab" style="opacity: 1;" tabindex="0">
> 

> 
> v = zeros(10, 1);
> 
> for i = 1:10
> 
>   for j = 1:10
> 
>     v(i) = v(i) + A(i, j) * x(j);
> 
>   end
> 
> end
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> How would you vectorize this code to run without any for loops? Check all that apply.
> 
> 1 point 
> 

      v = A * x; 
> 

      v = Ax; 
> 
>  v = x' * A; 
> 
>  v = sum (A * x); 
> 
>  4.Question 4
> 
> Say you have two column vectors vvv and www, each with 7 elements (i.e., they have dimensions 7x1). Consider the following code:
> 
> <pre contenteditable="false" data-language="matlab" style="opacity: 1;" tabindex="0">
>
> 
> z = 0;
> 
> for i = 1:7
> 
>   z = z + v(i) * w(i)
> 
> end
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> Which of the following vectorizations correctly compute z? Check all that apply.
> 
> 1 point 
> 

      z = sum (v .* w); 
> 

      z = v' * w; 
> 
>  z = v * w'; 
> 
>  z = v .* w; 
> 
>  5.Question 5
> 
> In Octave/Matlab, many functions work on single numbers, vectors, and matrices. For example, the sin function when applied to a matrix will return a new matrix with the sin of each element. But you have to be careful, as certain functions have different behavior. Suppose you have an 7x7 matrix XXX. You want to compute the log of every element, the square of every element, add 1 to every element, and divide every element by 4\. You will store the results in four matrices, A,B,C,DA, B, C, DA,B,C,D. One way to do so is the following code:
> 
> <pre contenteditable="false" data-language="matlab" style="opacity: 1;" tabindex="0">
> 
> for i = 1:7
> 
>   for j = 1:7
> 
>     A(i, j) = log(X(i, j));
> 
>     B(i, j) = X(i, j) ^ 2;
> 
>     C(i, j) = X(i, j) + 1;
> 
>     D(i, j) = X(i, j) / 4;
> 
>   end
> 
> end
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> Which of the following correctly compute A,B,C,A, B, C,A,B,C, or DDD? Check all that apply.
> 
> 1 point 
> 

      C = X + 1; 
> 

      D = X / 4; 
> 

      B = X .^ 2; 
> 
>  B = X ^ 2;
>
> -- https://www.coursera.org/learn/machine-learning/exam/dbM1J/octave-matlab-tutorial/attempt#Tunnel Vision Close
