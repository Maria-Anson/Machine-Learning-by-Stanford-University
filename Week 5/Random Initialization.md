# Random Initialization
> 
> Initializing all theta weights to zero does not work with neural networks. When we backpropagate, all nodes will update to the same value repeatedly. Instead we can randomly initialize our weights for our Θ\ThetaΘ matrices using the following method:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y7gaS7pXEeaCrQqTpeD5ng_8868ccda2c387f5d481d0c54ab78a86e_Screen-Shot-2016-12-04-at-11.27.28-AM.png?expiry=1593216000000&hmac=V6Y6kSWI5xcITlA6fZdkB_X7p2PMQTAQMD-SfrVik9c)
> 
> Hence, we initialize each Θij(l)\Theta^{(l)}_{ij}Θij(l)​ to a random value between[−ϵ,ϵ] [-\epsilon,\epsilon][−ϵ,ϵ]. Using the above formula guarantees that we get the desired bound. The same procedure applies to all the Θ\ThetaΘ's. Below is some working code you could use to experiment.
> 
> <pre contenteditable="false" style="opacity: 1;" tabindex="0">
> 
> 
> If the dimensions of Theta1 is 10x11, Theta2 is 10x11 and Theta3 is 1x11.
> 
> Theta1 = rand(10,11) * (2 * INIT_EPSILON) - INIT_EPSILON;
> 
> Theta2 = rand(10,11) * (2 * INIT_EPSILON) - INIT_EPSILON;
> 
> Theta3 = rand(1,11) * (2 * INIT_EPSILON) - INIT_EPSILON;
> 
> XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
> 
> </pre>
> 
> rand(x,y) is just a function in octave that will initialize a matrix of random real numbers between 0 and 1\.
> 
> (Note: the epsilon used above is unrelated to the epsilon from Gradient Checking)
>
> -- https://www.coursera.org/learn/machine-learning/supplement/KMzY7/random-initialization#main
