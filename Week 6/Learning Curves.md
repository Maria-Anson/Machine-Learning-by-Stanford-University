# Learning Curves
> 
> Training an algorithm on a very few number of data points (such as 1, 2 or 3) will easily have 0 errors because we can always find a quadratic curve that touches exactly those number of points. Hence:
> 
> *   As the training set gets larger, the error for a quadratic function increases.
> *   The error value will plateau out after a certain m, or training set size.
> 
> **Experiencing high bias:**
> 
> **Low training set size**: causes Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) to be low and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) to be high.
> 
> **Large training set size**: causes both Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) to be high with Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ)≈JCV(Θ)J_{CV}(\Theta)JCV​(Θ).
> 
> If a learning algorithm is suffering from **high bias**, getting more training data will not **(by itself)** help much.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bpAOvt9uEeaQlg5FcsXQDA_ecad653e01ee824b231ff8b5df7208d9_2-am.png?expiry=1593907200000&hmac=stI_xEEcsk_C1dYQhj19MMhUfulbaWG0Y5eswHqK4lI)
> 
> **Experiencing high variance:**
> 
> **Low training set size**: Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) will be low and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) will be high.
> 
> **Large training set size**: Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) increases with training set size and JCV(Θ)J_{CV}(\Theta)JCV​(Θ) continues to decrease without leveling off. Also, Jtrain(Θ)J_{train}(\Theta)Jtrain​(Θ) < JCV(Θ)J_{CV}(\Theta)JCV​(Θ) but the difference between them remains significant.
> 
> If a learning algorithm is suffering from **high variance**, getting more training data is likely to help.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/vqlG7t9uEeaizBK307J26A_3e3e9f42b5e3ce9e3466a0416c4368ee_ITu3antfEeam4BLcQYZr8Q_37fe6be97e7b0740d1871ba99d4c2ed9_300px-Learning1.png?expiry=1593907200000&hmac=roIL6O9cUYQYJhg__hYAbjENm9l2nlNoWVXbR761oVs)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/79woL/learning-curves#main
