# Principal Component Analysis
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> Consider the following 2D dataset:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/lkk6_L7kEeSZtCIACx4DqA_15.1-question.jpg?Expires=1595203200&Signature=kvJv39oMwUetGcooS7f8A80oUTA~AtzgreNcmWU3XEY0vzcSLjxVUqwAFKQAOpK-agjc6gQe2qnWIbkSehDbHB8~FSu9x~vxfnk0f-BdY3LCjyVekY8zvcWYFfXm1hBlZdGyil5yAUUIibDs1WJlUxUDPES3Z5XqfHWYennmbKM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> Which of the following figures correspond to possible values that PCA may return for u(1)u^{(1)}u(1) (the first eigenvector / first principal component)? Check all that apply (you may have to check more than one figure).
> 
> 1 / 1 point 
> 
>  ![](https://d3c33hcgiwev3.cloudfront.net/wBdxSL7kEeSKOiIAC1ARFQ_15.1-a.jpg?Expires=1595203200&Signature=XR8x4rikMmUZmTmF~gbjFgnLwnqpM9v0yHMFvtNZhD0jq~UpKrEEfxPokry0NT9LJgJ9eoMBbhmXK09rHD-WTQr4AnK77-TJz~whw~ksy2-e8ha40xhOYZEVsJ8QLLJvAtjXWHZWjPIicBIBZiJWzexzugy3mPeBeIyOoFvBH4o_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
> Check
> 

     Correct
> 
> The maximal variance is along the y = x line, so this option is correct.
> 
>  ![](https://d3c33hcgiwev3.cloudfront.net/6lGHcL7kEeSZtCIACx4DqA_15.1-b.jpg?Expires=1595203200&Signature=XjGhtN05qqiTzXfrrx6mQ3Exvy8NKbbq6rNbSKCwlQOd8G6NwcMVX19CoOyJ45PjRPYR0jOcqavLHWpsnYQNC18uAdBx3MvcS3SlirkR2pH9rVIOsvJCH3pwaEVaOOipJPvm2hw1zQUDuNCjbfJKcQNGi9NjeEpymkgp3otkBaQ_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
> Check
> 

     Correct
> 
> The maximal variance is along the y = x line, so the negative vector along that line is correct for the first principal component.
> 
>  ![](https://d3c33hcgiwev3.cloudfront.net/_Say2r7kEeSKOiIAC1ARFQ_15.1-c.jpg?Expires=1595203200&Signature=Km8pogxGS5DGwfnLoH80GqEcHAlQ0cX5OcvCdFclmTia4aasQKk63svyQLAKPJ1a-Un56mOKropPARz~xgWEovT7CwfRXAeuLID3ZOOhsH9dW-BcpBYeF4HvXBvUEr8ZFyFbMWqJdWzI8JxjwH7KmI9yMpe0xUmiX5BV7Va3HKk_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  ![](https://d3c33hcgiwev3.cloudfront.net/DoOVFr7lEeSjMiIAC7MDiQ_15.1-d.jpg?Expires=1595203200&Signature=bXxU2a3CKghieCYAf4IGTjFU9AzJ1dcqxphi7kWIyt04Y2uNx2LDNILbzdtF~nxOpUoemtrfgQXRID8aXF-ugAsMkNFGqMudzbauLWxEp~0Qb73OPwdOEqerdD2sdQHYUssJx2hTMffF3JneoBcaBHatvqnDOXfuOxa5OBTNhyc_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A) 
> 
>  2.Question 2
> 
> Which of the following is a reasonable way to select the number of principal components kkk?
> 
> (Recall that nnn is the dimensionality of the input data and mmm is the number of input examples.)
> 
> 1 / 1 point 
> 
>  Choose kkk to be the smallest value so that at least 1% of the variance is retained. 
> 
>  Choose the value of kkk that minimizes the approximation error 1m∑i=1m∣∣x(i)−xapprox(i)∣∣2\frac{1}{m} \sum_{i=1}^m ||x^{(i)} - x^{(i)}_{\rm approx}||^2m1​∑i=1m​∣∣x(i)−xapprox(i)​∣∣2. 
> 

      Choose kkk to be the smallest value so that at least 99% of the variance is retained. 
> 
>  Choose kkk to be 99% of nnn (i.e., k=0.99∗nk = 0.99*nk=0.99∗n, rounded to the nearest integer). 
> 
> Check
> 
> Correct
> 
> This is correct, as it maintains the structure of the data while maximally reducing its dimension.
> 
>  3.Question 3
> 
> Suppose someone tells you that they ran PCA in such a way that "95% of the variance was retained." What is an equivalent statement to this?
> 
> 1 / 1 point 
> 

      1m∑i=1m∣∣x(i)−xapprox(i)∣∣21m∑i=1m∣∣x(i)∣∣2≤0.05\frac{ \frac{1}{m} \sum_{i=1}^m ||x^{(i)}- x^{(i)}_{\rm approx}||^2}{\frac{1}{m} \sum_{i=1}^m ||x^{(i)}||^2} \leq 0.05m1​∑i=1m​∣∣x(i)∣∣2m1​∑i=1m​∣∣x(i)−xapprox(i)​∣∣2​≤0.05 
> 
>  1m∑i=1m∣∣x(i)∣∣21m∑i=1m∣∣x(i)−xapprox(i)∣∣2≥0.95\frac{\frac{1}{m} \sum_{i=1}^m ||x^{(i)}||^2}{\frac{1}{m} \sum_{i=1}^m ||x^{(i)}- x^{(i)}_{\rm approx}||^2} \geq 0.95m1​∑i=1m​∣∣x(i)−xapprox(i)​∣∣2m1​∑i=1m​∣∣x(i)∣∣2​≥0.95 
> 
>  1m∑i=1m∣∣x(i)−xapprox(i)∣∣21m∑i=1m∣∣x(i)∣∣2≥0.05\frac{ \frac{1}{m} \sum_{i=1}^m ||x^{(i)}- x^{(i)}_{\rm approx}||^2}{\frac{1}{m} \sum_{i=1}^m ||x^{(i)}||^2} \geq 0.05m1​∑i=1m​∣∣x(i)∣∣2m1​∑i=1m​∣∣x(i)−xapprox(i)​∣∣2​≥0.05 
> 
>  1m∑i=1m∣∣x(i)−xapprox(i)∣∣21m∑i=1m∣∣x(i)∣∣2≥0.95\frac{ \frac{1}{m} \sum_{i=1}^m ||x^{(i)}- x^{(i)}_{\rm approx}||^2}{\frac{1}{m} \sum_{i=1}^m ||x^{(i)}||^2} \geq 0.95m1​∑i=1m​∣∣x(i)∣∣2m1​∑i=1m​∣∣x(i)−xapprox(i)​∣∣2​≥0.95 
> 
> Check
> 
> Correct
> 
> This is the correct formula.
> 
>  4.Question 4
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 / 1 point 
> 
>  Given only z(i)z^{(i)}z(i) and UreduceU_{\rm reduce}Ureduce​, there is no way to reconstruct any reasonable approximation to x(i)x^{(i)}x(i). 
> 

      Even if all the input features are on very similar scales, we should still perform mean normalization (so that each feature has zero mean) before running PCA. 
> 
> Check
> 
> Correct
> 
> If you do not perform mean normalization, PCA will rotate the data in a possibly undesired way.
> 
>  PCA is susceptible to local optima; trying multiple random initializations may help. 
> 

      Given input data x∈Rnx \in \mathbb{R}^nx∈Rn, it makes sense to run PCA only with values of kkk that satisfy k≤nk \le nk≤n. (In particular, running it with k=nk = nk=n is possible but not helpful, and k>nk > nk>n does not make sense.) 
> 
> Check
> 
> Correct
> 
> The reasoning given is correct: with k=nk = nk=n, there is no compression, so PCA has no use.
> 
>  5.Question 5
> 
> Which of the following are recommended applications of PCA? Select all that apply.
> 
> 1 / 1 point 
> 
>  Data visualization: To take 2D data, and find a different way of plotting it in 2D (using k=2). 
> 

      Data compression: Reduce the dimension of your data, so that it takes up less memory / disk space. 
> 
> Check
> 
> Correct
> 
> If memory or disk space is limited, PCA allows you to save space in exchange for losing a little of the data's information. This can be a reasonable tradeoff.
> 
>  As a replacement for (or alternative to) linear regression: For most learning applications, PCA and linear regression give substantially similar results. 
> 

      Data compression: Reduce the dimension of your input data x(i)x^{(i)}x(i), which will be used in a supervised learning algorithm (i.e., use PCA so that your supervised learning algorithm runs faster). 
> 
> Check
> 
> Correct
> 
> If your learning algorithm is too slow because the input dimension is too high, then using PCA to speed it up is a reasonable choice.
>
> -- https://www.coursera.org/learn/machine-learning/exam/B20Bx/principal-component-analysis/attempt?redirectToCover=true#Tunnel Vision Close
