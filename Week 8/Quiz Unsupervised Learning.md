# Unsupervised Learning
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> For which of the following tasks might K-means clustering be a suitable algorithm? Select all that apply.
> 
> 1 / 1 point 
> 
>  Given historical weather records, predict if tomorrow's weather will be sunny or rainy. 
> 

      From the user usage patterns on a website, figure out what different groups of users exist. 
> 
> Check
> 
> Correct
> 
> We can cluster the users with K-means to find different, distinct groups.
> 
>  Given many emails, you want to determine if they are Spam or Non-Spam emails. 
> 

      Given a set of news articles from many different news websites, find out what are the main topics covered. 
> 
> Check
> 
> Correct
> 
> K-means can cluster the articles and then we can inspect them or use other methods to infer what topic each cluster represents
> 
>  2.Question 2
> 
> Suppose we have three cluster centroids μ1=[12]\mu_1 =
> 
> [12]
> 
> \begin{bmatrix}1 \\ 2 \end{bmatrix}μ1​=[12​], μ2=[−30]\mu_2 =
> 
> [−30]
> 
> \begin{bmatrix}-3 \\ 0 \end{bmatrix}μ2​=[−30​] and μ3=[42]\mu_3 =
> 
> [42]
> 
> \begin{bmatrix}4 \\ 2 \end{bmatrix}μ3​=[42​]. Furthermore, we have a training example x(i)=[−21]x^{(i)} =
> 
> [−21]
> 
> \begin{bmatrix}-2 \\ 1 \end{bmatrix}x(i)=[−21​]. After a cluster assignment step, what will c(i)c^{(i)}c(i) be?
> 
> 1 / 1 point 
> 
>  c(i)=3c^{(i)} = 3c(i)=3 
> 
>  c(i)=1c^{(i)} = 1c(i)=1 
> 
>  c(i)c^{(i)}c(i) is not assigned 
> 

      c(i)=2 
> 
> Check
> 
> Correct
> 
> x(i)x^{(i)}x(i) is closest to μ2\mu_2μ2​, so c(i)=2c^{(i)} = 2c(i)=2
> 
>  3.Question 3
> 
> K-means is an iterative algorithm, and two of the following steps are repeatedly carried out in its inner-loop. Which two?
> 
> 1 / 1 point 
> 
>  Feature scaling, to ensure each feature is on a comparable scale to the others. 
> 

      The cluster assignment step, where the parameters c(i)c^{(i)}c(i) are updated. 
> 
> Check
> 
> Correct
> 
> This is the correst first step of the K-means loop.
> 

      Move the cluster centroids, where the centroids μk\mu_kμk​ are updated. 
> 
> Check
> 
> Correct
> 
> The cluster update is the second step of the K-means loop.
> 
>  Using the elbow method to choose K. 
> 
>  4.Question 4
> 
> Suppose you have an unlabeled dataset {x(1),…,x(m)}\{x^{(1)}, \ldots, x^{(m)}\}{x(1),…,x(m)}. You run K-means with 50 different random
> 
> initializations, and obtain 50 different clusterings of the
> 
> data. What is the recommended way for choosing which one of
> 
> these 50 clusterings to use?
> 
> 1 / 1 point 
> 
>  The answer is ambiguous, and there is no good way of choosing. 
> 
>  Always pick the final (50th) clustering found, since by that time it is more likely to have converged to a good solution. 
> 
>  The only way to do so is if we also have labels y(i)y^{(i)}y(i) for our data. 
> 

      For each of the clusterings, compute 1m∑i=1m∣∣x(i)−μc(i)∣∣2\frac{1}{m} \sum_{i=1}^m{ ||x^{(i)} - \mu_{c^{(i)}}||^2}m1​∑i=1m​∣∣x(i)−μc(i)​∣∣2, and pick the one that minimizes this. 
> 
> Check
> 
> Correct
> 
> This function is the distortion function. Since a lower value for the distortion function implies a better clustering, you should choose the clustering with the smallest value for the distortion function.
> 
>  5.Question 5
> 
> Which of the following statements are true? Select all that apply.
> 
> 1 / 1 point 
> 

      On every iteration of K-means, the cost function J(c(1),…,c(m),μ1,…,μk)J(c^{(1)}, \ldots, c^{(m)}, \mu_1, \ldots,\mu_k)J(c(1),…,c(m),μ1​,…,μk​) (the distortion function) should either stay the same or decrease; in particular, it should not increase. 
> 
> Check
> 
> Correct
> 
> Both the cluster assignment and cluster update steps decrese the cost / distortion function, so it should never increase after an iteration of K-means.
> 

      A good way to initialize K-means is to select K (distinct) examples from the training set and set the cluster centroids equal to these selected examples. 
> 
> Check
> 
> Correct
> 
> This is the recommended method of initialization.
> 
>  K-Means will always give the same results regardless of the initialization of the centroids. 
> 
>  Once an example has been assigned to a particular centroid, it will never be reassigned to another different centroid
>
> -- https://www.coursera.org/learn/machine-learning/exam/4sGmv/unsupervised-learning/attempt?redirectToCover=true#Tunnel Vision Close
