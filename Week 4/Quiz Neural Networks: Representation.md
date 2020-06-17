# Neural Networks: Representation
> 
> Total points 5
> 
>  1.Question 1
> 
> Which of the following statements are true? Check all that apply.
> 
> 1 point 
> 
>  Suppose you have a multi-class classification problem with three classes, trained with a 3 layer network. Let a1(3)=(hΘ(x))1a^{(3)}_1 = (h_\Theta(x))_1a1(3)​=(hΘ​(x))1​ be the activation of the first output unit, and similarly a2(3)=(hΘ(x))2a^{(3)}_2 = (h_\Theta(x))_2a2(3)​=(hΘ​(x))2​ and a3(3)=(hΘ(x))3a^{(3)}_3 = (h_\Theta(x))_3a3(3)​=(hΘ​(x))3​. Then for any input xxx, it must be the case that a1(3)+a2(3)+a3(3)=1a^{(3)}_1 + a^{(3)}_2 + a^{(3)}_3 = 1a1(3)​+a2(3)​+a3(3)​=1. 
> 
>  A two layer (one input layer, one output layer; no hidden layer) neural network can represent the XOR function. 
> 

      The activation values of the hidden units in a neural network, with the sigmoid activation function applied at every layer, are always in the range (0, 1). 
> 

      Any logical function over binary-valued (0 or 1) inputs x1x_1x1​ and x2x_2x2​ can be (approximately) represented using some neural network. 
> 
>  2.Question 2
> 
> Consider the following neural network which takes two binary-valued inputs x1,x2∈{0,1}x_1, x_2 \in \{0, 1\}x1​,x2​∈{0,1} and outputs hΘ(x)h_\Theta(x)hΘ​(x). Which of the following logical functions does it (approximately) compute?
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/Kf1MZL5zEeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.24.00-AM.png?Expires=1592524800&Signature=Qg92OxZvWWwj1RKhKFXQwsLZ47qnuNgHPHq6lpmN-9ejtLV5V5If7PWwJbldwtKsNLg7nxuYHqoYE5NOb7qFcjrKsA-LuzdlRZD2dDOOO1JQ-A~3hvPLz0FDR3J2xDhVY0eGwyJ2-UN7QRgY20m41vQhrVi6Vi1s88BywGjVP4w_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> 1 point 
> 

      AND 
> 
>  NAND (meaning "NOT AND") 
> 
>  OR 
> 
>  XOR (exclusive OR) 
> 
>  3.Question 3
> 
> Consider the neural network given below. Which of the following equations correctly computes the activation a1(3)a_1^{(3)}a1(3)​? Note: g(z)g(z)g(z) is the sigmoid activation function.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/FflwP750EeSGOCIAC3iXdw_Screen-Shot-2015-02-27-at-3.28.08-AM.png?Expires=1592524800&Signature=jZ3SmnCkIyrAijmtMCSpEfmRbW4B8mWVFHuDplkn3TSpMFSAVBeipXmWxKuDUvSLjqXibcvKM2ejJVyRtG09jclVq2HmhbIAwrvZ51-NixQuctcjTK5I3thEwqY00uKP~86Ft~KEnKajtmPD5iiwtEnNlVVg8inwWvPUoXc~mYY_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> 1 point 
> 

      a1(3)=g(Θ1,0(2)a0(2)+Θ1,1(2)a1(2)+Θ1,2(2)a2(2))a_1^{(3)} = g(\Theta_{1,0}^{(2)}a_0^{(2)} + \Theta_{1,1}^{(2)}a_1^{(2)} + \Theta_{1,2}^{(2)}a_2^{(2)}) a1(3)​=g(Θ1,0(2)​a0(2)​+Θ1,1(2)​a1(2)​+Θ1,2(2)​a2(2)​) 
> 
>  a1(3)=g(Θ1,0(1)a0(1)+Θ1,1(1)a1(1)+Θ1,2(1)a2(1))a_1^{(3)} = g(\Theta_{1,0}^{(1)}a_0^{(1)} + \Theta_{1,1}^{(1)}a_1^{(1)} + \Theta_{1,2}^{(1)}a_2^{(1)}) a1(3)​=g(Θ1,0(1)​a0(1)​+Θ1,1(1)​a1(1)​+Θ1,2(1)​a2(1)​) 
> 
>  a1(3)=g(Θ1,0(1)a0(2)+Θ1,1(1)a1(2)+Θ1,2(1)a2(2))a_1^{(3)} = g(\Theta_{1,0}^{(1)}a_0^{(2)} + \Theta_{1,1}^{(1)}a_1^{(2)} + \Theta_{1,2}^{(1)}a_2^{(2)}) a1(3)​=g(Θ1,0(1)​a0(2)​+Θ1,1(1)​a1(2)​+Θ1,2(1)​a2(2)​) 
> 
>  The activation a1(3)a_1^{(3)}a1(3)​ is not present in this network. 
> 
>  4.Question 4
> 
> You have the following neural network:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/lvSx8L50EeSGOCIAC3iXdw_Screen-Shot-2015-02-27-at-3.32.25-AM.png?Expires=1592524800&Signature=NED6gT8Qr3Fq4T4QtP6drhhItg1z2ntFMPyS764fYAlP4UWvCd1mdaE6DcRqg4msZMKM-xD~n9QzHWIchHNKKv2hoOkex9wpb3sm0xwpTB53s2M00d9hmdSAlS4N24dVsM2HzWQWUFRvbOPBoKKs~IJwxthXk9Hlw-RKLLPOyk8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> You'd like to compute the activations of the hidden layer a(2)∈R3a^{(2)} \in \mathbb{R}^3a(2)∈R3. One way to do so is the following Octave code:
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/uLXmWL50EeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.32.38-AM.png?Expires=1592524800&Signature=hUvrn2hH3LdAloXoe0r3XSd9RswQfnG7swGqK74R7vGXK3Mxc72~vC4VkNDHQsWDOLsChFBSRAUSP07h7Q6GPP~KlpgmmyPhBMKAuAvLQLe9q8Kwyz0q7sm2W2mGpSt103cJLPaTt2qs5qrCRImArD2DSE9ByR~hQMDLA1KSnEA_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> You want to have a vectorized implementation of this (i.e., one that does not use for loops). Which of the following implementations correctly compute a(2)a^{(2)}a(2)? Check all that apply.
> 
> 1 point 
> 

      a2 = sigmoid (Theta1 * x); 
> 
>  a2 = sigmoid (x * Theta1); 
> 
>  a2 = sigmoid (Theta2 * x); 
> 
>  z = sigmoid(x); a2 = Theta1 * z; 
> 
>  5.Question 5
> 
> You are using the neural network pictured below and have learned the parameters Θ(1)=[112.411.73.2]\Theta^{(1)} =
> 
> [1111.72.43.2]
> 
> \begin{bmatrix} 1 & 1 & 2.4 \\ 1 & 1.7 & 3.2\end{bmatrix}Θ(1)=[11​11.7​2.43.2​] (used to compute a(2)a^{(2)}a(2)) and Θ(2)=[10.3−1.2]\Theta^{(2)} =
> 
> [10.3−1.2]
> 
> \begin{bmatrix} 1 & 0.3 & -1.2 \end{bmatrix}Θ(2)=[1​0.3​−1.2​] (used to compute a(3)a^{(3)}a(3)} as a function of a(2)a^{(2)}a(2)). Suppose you swap the parameters for the first hidden layer between its two units so Θ(1)=[11.73.2112.4]\Theta^{(1)} =
> 
> [111.713.22.4]
> 
> \begin{bmatrix}1 & 1.7 & 3.2 \\1 & 1 & 2.4 \end{bmatrix}Θ(1)=[11​1.71​3.22.4​] and also swap the output layer so Θ(2)=[1−1.20.3]\Theta^{(2)} =
> 
> [1−1.20.3]
> 
> \begin{bmatrix} 1 & -1.2 & 0.3 \end{bmatrix}Θ(2)=[1​−1.2​0.3​]. How will this change the value of the output hΘ(x)h_\Theta(x)hΘ​(x)?![](https://d3c33hcgiwev3.cloudfront.net/uHeIXL51EeSVRiIAC2sM-Q_Screen-Shot-2015-02-27-at-3.42.00-AM.png?Expires=1592524800&Signature=TDF3DmpFYPdLR32G2dYHEJY3dedW922I3utjO4X87IzbA5L~C8ge7GHiwMrz2jGwS8MSd0~xs3p-67vu7Dy1a16IUbeD3ST5~bk~1fwmYrrX70vyHWWHhf28UkL5l1FE7cSjEnhlfPVOGZ8oA9km51ZdYseDGi2YE-6H4~4Jzxo_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
> 
> 1 point 
> 

      It will stay the same. 
> 
>  It will increase. 
> 
>  It will decrease 
> 
>  Insufficient information to tell: it may increase or decrease.
>
> -- https://www.coursera.org/learn/machine-learning/exam/HrMM9/neural-networks-representation/attempt#Tunnel Vision Close
