# Anomaly Detection
> 
> Latest Submission Grade
> 
> 100%
> 
>  1.Question 1
> 
> For which of the following problems would anomaly detection be a suitable algorithm?
> 
> 1 / 1 point 
> 
>  Given data from credit card transactions, classify each transaction according to type of purchase (for example: food, transportation, clothing). 
> 

      From a large set of primary care patient records, identify individuals who might have unusual health conditions. 
> 
> Check
> 
> Correct
> 
> Since you are just looking for unusual conditions instead of a particular disease, this is a good application of anomaly detection.
> 
>  From a large set of hospital patient records, predict which patients have a particular disease (say, the flu). 
> 

      In a computer chip fabrication plant, identify microchips that might be defective. 
> 
> Check
> 
> Correct
> 
> The defective chips are the anomalies you are looking for by modeling the properties of non-defective chips.
> 
>  2.Question 2
> 
> Suppose you have trained an anomaly detection system that flags anomalies when p(x)p(x)p(x) is less than ε\varepsilonε, and you find on the cross-validation set that it has too many false negatives (failing to flag a lot of anomalies). What should you do?
> 
> 1 / 1 point 
> 

      Increase ε\varepsilonε 
> 
>  Decrease ε\varepsilonε 
> 
> Check
> 
> Correct
> 
> By increasing ε\varepsilonε, you will flag more anomalies, as desired.
> 
>  3.Question 3
> 
> Suppose you are developing an anomaly detection system to catch manufacturing defects in airplane engines. You model uses
> 
> p(x)=∏j=1np(xj;μj,σj2).p(x) = \prod_{j=1}^n p(x_j ; \mu_j, \sigma^2_j).p(x)=∏j=1n​p(xj​;μj​,σj2​).
> 
> You have two features x1x_1x1​ = vibration intensity, and x2x_2x2​ = heat generated. Both x1x_1x1​ and x2x_2x2​ take on values between 0 and 1 (and are strictly greater than 0), and for most "normal" engines you expect that x1≈x2x_1 \approx x_2x1​≈x2​. One of the suspected anomalies is that a flawed engine may vibrate very intensely even without generating much heat (large x1x_1x1​, small x2x_2x2​), even though the particular values of x1x_1x1​ and x2x_2x2​ may not fall outside their typical ranges of values. What additional feature x3x_3x3​ should you create to capture these types of anomalies:
> 
> 1 / 1 point 
> 
>  x3=x1×x2x_3 = x_1 \times x_2x3​=x1​×x2​ 
> 
>  x3=x1+x2x_3 = x_1 + x_2x3​=x1​+x2​ 
> 

        x3=x1/x2
> 
>  x3=x12×x2x_3 = x_1^2 \times x_2x3​=x12​×x2​ 
> 
> Check
> 
> Correct
> 
> This is correct, as it will take on large values for anomalous examples and smaller values for normal examples.
> 
>  4.Question 4
> 
> Which of the following are true? Check all that apply.
> 
> 1 / 1 point 
> 

      If you do not have any labeled data (or if all your data has label y=0y=0y=0), then is is still possible to learn p(x)p(x)p(x), but it may be harder to evaluate the system or choose a good value of ϵ\epsilonϵ. 
> 
> Check
> 
> Correct
> 
> Only negative examples are used in training, but it is good to have some labeled data of both types for cross-validation.
> 
>  If you have a large labeled training set with many positive examples and many negative examples, the anomaly detection algorithm will likely perform just as well as a supervised learning algorithm such as an SVM. 
> 

      When choosing features for an anomaly detection system, it is a good idea to look for features that take on unusually large or small values for (mainly the) anomalous examples. 
> 
> Check
> 
> Correct
> 
> These are good features, as they will lie outside the learned model, so you will have small values for p(x)p(x)p(x) with these examples.
> 
>  If you are developing an anomaly detection system, there is no way to make use of labeled data to improve your system. 
> 
>  5.Question 5
> 
> You have a 1-D dataset {x(1),…,x(m)}\{x^{(1)}, \ldots, x^{(m)}\}{x(1),…,x(m)} and you want to detect outliers in the dataset. You first plot the dataset and it looks like this:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/ee5JoL54EeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-4.01.53-AM.png?Expires=1596153600&Signature=gIJkIpD-Mm-UUL5waM~nRefWKQ0g2cea-SZYZ6EuLlxbkLj6X2I1aPgYYTq8K2ag6YurTfxdyJe4v54tlAybf9pvmgli12eBSH3HgYd2jUlACFXqksYgN5tS7BYOIfaujB0RbD2EEdKEgF-vJq9-zsqsUmm1vVugGQSAvAjlO6Q_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> Suppose you fit the gaussian distribution parameters μ1\mu_1μ1​ and σ12\sigma_1^2σ12​ to this dataset. Which of the following values for μ1\mu_1μ1​ and σ12\sigma_1^2σ12​ might you get?
> 
> 1 / 1 point 
> 

      μ1=−3,σ12=4 
> 
>  μ1=−6,σ12=4\mu_1 = -6, \sigma_1^2 = 4μ1​=−6,σ12​=4 
> 
>  μ1=−3,σ12=2\mu_1 = -3, \sigma_1^2 = 2μ1​=−3,σ12​=2 
> 
>  μ1=−6,σ12=2\mu_1 = -6, \sigma_1^2 = 2μ1​=−6,σ12​=2 
> 
> Check
> 
> Correct
> 
> This is correct, as the data are centered around -3 and tail most of the points lie in [-5, -1].
>
> -- https://www.coursera.org/learn/machine-learning/exam/Dx28I/anomaly-detection/attempt?redirectToCover=true#Tunnel Vision Close
