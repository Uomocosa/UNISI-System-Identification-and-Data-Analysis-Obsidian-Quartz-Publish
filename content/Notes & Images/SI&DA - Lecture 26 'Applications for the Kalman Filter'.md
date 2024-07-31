###### Summary
Recursive system identification, we considered the following **Linear Regression Model**:
$$
y(t) = \varphi(t)^T \kern2px \theta + e(t)
$$
where:
- $\varphi(t)$ : **regressor vector** which usually contains past values of input and output signals like in **ARX** or **FIR** models
- $\theta$ : **vector of parameters** to be estimated
- $e(t)$ : a **corruption process** or noise

We have found the solution to this problem, if we minimize *the sum of squares of the one step ahead output prediction error* :
$$
\min_{\theta} \sum_{t=1}^N \left(y(t) - \hat{y}(t\ | \ t-1)\right)^2
$$
We get the **Least Square Solution**:
$$
\hat{\theta}_{LS} = \left[\sum_{t=1}^N \varphi(t)\kern2px\varphi^T(t)\right]^{-1} \cdot \sum_{t=1}^N \varphi(t)\kern2pxy(t) 
$$
But in case we want to calculate the estimate at time $t$ to deliver it, instead at $t=N$ (when the measurement ends) we just need to change the formula a bit, in principle the same formula:
$$
\hat{\theta}_{t} = \left[\sum_{t=1}^t \varphi(k)\kern2px\varphi^T(k)\right]^{-1} \cdot \sum_{k=1}^t \varphi(k)\kern2pxy(k)  
$$
But a more clever solution to recursively update the estimate could be to implement the following *Recursive Algorithm* :
$$
\left\{
\begin{array}{l}
\hat{\theta}_t = \hat{\theta}_{t-1} + R(t)^{-1}\kern1px\varphi(t)\kern0px\left(y(t)-\varphi^T(t)\kern1px\hat{\theta}_{t-1}\right)
\\
R(t) = R(t-1) + \varphi(t)\kern1px\varphi^T(t)
\end{array}
\right.
$$
where: $\varphi^T(t)\kern1px\hat{\theta}_{t-1} = \hat{y}(t \ | \ t-1)$

This algorithm can also be upgraded, removing the need to compute the inverse of $R(t)$ at each iteration:
We call $P(t) = R(t)^{-1}$, and using the property:
$$
(A+BCD)^{-1} = A^{-1}-A^{-1}B\left(C^{-1}+DA^{-1}B\right)^{-1}DA^{-1}
$$
we obtain:
$$
P(t)= P(t-1) - \frac{P(t-1)\kern1px\varphi(t)\kern1px\varphi^T(t)\kern1px P(t-1)}{1 + \varphi^T(t)\kern1px P(t-1)\kern1px\varphi(t)}
$$
So the ***complete*** algorithm is:
$$
\left\{
\begin{array}{l}
\hat{\theta}_t = \hat{\theta}_{t-1} + P(t)\kern1px\varphi(t)\kern0px\left(y(t)-\varphi^T(t)\kern1px\hat{\theta}_{t-1}\right)
\\
P(t)= P(t-1) - \large \frac{P(t-1)\kern1px\varphi(t)\kern1px\varphi^T(t)\kern1px P(t-1)}{1 + \varphi^T(t)\kern1px P(t-1)\kern1px\varphi(t)}
\end{array}
\right.
$$
---
![[Pasted image 20220719111757.png]]
![[Pasted image 20220719111841.png]]
#TODO What does the purple line mean??
![[Pasted image 20220719111913.png]]
![[Pasted image 20220719111946.png]]
![[Pasted image 20220719112004.png]]
![[Pasted image 20220719112017.png]]
#TODO Understand the graph
![[Pasted image 20220719112034.png]]
![[Pasted image 20220719112056.png]]
![[Pasted image 20220719112122.png]]
![[Pasted image 20220719112136.png]]
![[Pasted image 20220719112215.png]]
![[Pasted image 20220719112239.png]]
![[Pasted image 20220719112253.png]]
![[Pasted image 20220719112305.png]]
![[Pasted image 20220719112319.png]]
![[Pasted image 20220719112343.png]]
![[Pasted image 20220719112400.png]]
![[Pasted image 20220719112426.png]]
![[Pasted image 20220719112552.png]]
![[Pasted image 20220719112618.png]]
