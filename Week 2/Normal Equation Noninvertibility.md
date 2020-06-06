# Normal Equation Noninvertibility
> 
> When implementing the normal equation in octave we want to use the 'pinv' function rather than 'inv.' The 'pinv' function will give you a value of θ\thetaθ even if XTXX^TXXTX is not invertible.
> 
> If XTXX^TXXTX is **noninvertible,** the common causes might be having :
> 
> *   Redundant features, where two features are very closely related (i.e. they are linearly dependent)
> *   Too many features (e.g. m ≤ n). In this case, delete some features or use "regularization" (to be explained in a later lesson).
> 
> Solutions to the above problems include deleting a feature that is linearly dependent with another or deleting one or more features when there are too many features.
>
> -- https://www.coursera.org/learn/machine-learning/supplement/66bi5/normal-equation-noninvertibility#main
