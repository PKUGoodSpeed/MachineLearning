#### Second Order Optimizations

##### 5 steps of gradient descent:
1. Define a model
2. Define an error function or Loss
3. Compute gradients
4. Update weights using gradients: $w_i += -\text{learning_rate} * grad_w_i$
5. Repeat step 1 ~ 4


##### Second Order optimization methods:
###### Idea: using the second order derivatives
###### Advantageous:
    1. Do not ignore curvature of the error surface
    2. Better Performance in a single optimization step
    3. Will not trapped by the slow convergence near saddle points
    
###### Newton's methods:
    1. Version #1: Root finding method
    
        $x = x - \frac{f(x)}{f'(x)}$
        
        where $f'(x)$ should be non-zero otherwise it is trapped in a singularity point.
        
    2. Version #2: Optimization
        
        Trying to find where the derivative of the objective function is zero:
        
        $x = x - \frac{f'(x)}{f"(x)}$
        
        1. One-D case, equivalent as using a quadratic approximation
        
        2. Function of a Multiple-D space:
        
            $x = x - H^{-1}\cdot G$
            
            where $H$ is the Hessian matrix (second order derivative tensor), $G$ is the gradient vector.
            

##### Four Derivative Operations
- Gradient (vector)
- Derivative (scalar)
- Jacobi (Matrix: multi-D/multi-D)
- Hessian (Second order derivative tensor: 1-D/multi-D)