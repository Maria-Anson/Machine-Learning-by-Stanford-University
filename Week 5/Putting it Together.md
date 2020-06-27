# Putting it Together
> 
> First, pick a network architecture; choose the layout of your neural network, including how many hidden units in each layer and how many layers in total you want to have.
> 
> *   Number of input units = dimension of features x(i)x^{(i)}x(i)
> *   Number of output units = number of classes
> *   Number of hidden units per layer = usually more the better (must balance with cost of computation as it increases with more hidden units)
> *   Defaults: 1 hidden layer. If you have more than 1 hidden layer, then it is recommended that you have the same number of units in every hidden layer.
> 
> **Training a Neural Network**
> 
> 1.  Randomly initialize the weights
> 2.  Implement forward propagation to get hΘ(x(i))h_\Theta(x^{(i)})hΘ​(x(i)) for any x(i)x^{(i)}x(i)
> 3.  Implement the cost function
> 4.  Implement backpropagation to compute partial derivatives
> 5.  Use gradient checking to confirm that your backpropagation works. Then disable gradient checking.
> 6.  Use gradient descent or a built-in optimization function to minimize the cost function with the weights in theta.
> 
> When we perform forward and back propagation, we loop on every training example:
> 
> <pre contenteditable="false" style="opacity: 1;" tabindex="0">
> 
> 1
> 
> 2
> 
> 3
> 
> for i = 1:m,
> 
>    Perform forward propagation and backpropagation using example (x(i),y(i))
> 
>    (Get activations a(l) and delta terms d(l) for l = 2,...,L
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> The following image gives us an intuition of what is happening as we are implementing our neural network:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hGk18LsaEea7TQ6MHcgMPA_8de173808f362583eb39cdd0c89ef43e_Screen-Shot-2016-12-05-at-10.40.35-AM.png?expiry=1593388800000&hmac=3Q0omPdnJtG_fgZNwlObRbFJSmg2ULvmTlOgh2JN_G0)
> 
> Ideally, you want hΘ(x(i))h_\Theta(x^{(i)})hΘ​(x(i)) ≈\approx≈ y(i)y^{(i)}y(i). This will minimize our cost function. However, keep in mind that J(Θ)J(\Theta)J(Θ) is not convex and thus we can end up in a local minimum instead.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/Uskwd/putting-it-together#main
