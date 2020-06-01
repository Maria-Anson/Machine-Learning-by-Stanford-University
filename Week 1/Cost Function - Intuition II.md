 # Cost Function - Intuition II
 
 A contour plot is a graph that contains many contour lines. A contour line of a two variable function has a constant value at all points of the same line. An example of such a graph is the one to the right below.
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/N2oKYp2wEeaVChLw2Vaaug_d4d1c5b1c90578b32a6672e3b7e4b3a4_Screenshot-2016-10-29-01.14.37.png?expiry=1591142400000&hmac=ub8WiG2lKqTFE5bnWTjs14oElddAI9p8VgsVUTv76b0)
 
 Taking any color and going along the 'circle', one would expect to get the same value of the cost function. For example, the three green points found on the green line above have the same value for J(θ0,θ1)J(\theta_0,\theta_1)J(θ0​,θ1​) and as a result, they are found along the same line. The circled x displays the value of the cost function for the graph on the left when θ0\theta_0θ0​ = 800 and θ1\theta_1θ1​= -0.15\. Taking another h(x) and plotting its contour plot, one gets the following graphs:
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/26RZhJ34EeaiZBL80Yza_A_0f38a99c8ceb8aa5b90a5f12136fdf43_Screenshot-2016-10-29-01.14.57.png?expiry=1591142400000&hmac=YEbwhSfXx6ssjaLbAQRfoeBp5YYYzOh6n0pLzYZATqI)
 
 When θ0\theta_0θ0​ = 360 and θ1\theta_1θ1​ = 0, the value of J(θ0,θ1)J(\theta_0,\theta_1)J(θ0​,θ1​) in the contour plot gets closer to the center thus reducing the cost function error. Now giving our hypothesis function a slightly positive slope results in a better fit of the data.
 
 ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hsGgT536Eeai9RKvXdDYag_2a61803b5f4f86d4290b6e878befc44f_Screenshot-2016-10-29-09.59.41.png?expiry=1591142400000&hmac=lX-VOrIAoBHtwKgKmoQIkCSWpTRzXrKMUZvRtz78_-k)
 
 The graph above minimizes the cost function as much as possible and consequently, the result of θ1\theta_1θ1​ and θ0\theta_0θ0​ tend to be around 0.12 and 250 respectively. Plotting those values on our graph to the right seems to put our point in the center of the inner most 'circle'.

 -- https://www.coursera.org/learn/machine-learning/supplement/9SEeJ/cost-function-intuition-ii#main
