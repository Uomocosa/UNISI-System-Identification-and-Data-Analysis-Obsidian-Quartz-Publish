###### Summary
The KF (*Kalman Filter*) Algorithm
*Initialization*: select $\hat{x}(0 \ | \ -1)$ and $P(0 \ | \ -1)$.
*For-Loop*: $t = 0 ,\ 1 ,\ 2 ,\ \ldots$
$\kern25px$$K(t) = P(t \ | \ t-1) \cdot C^T \cdot \left[C \kern1px P(t \ | \ t-1) \kern1px C^T + R \right]^{-1}$
$\kern25px$$\hat{x}(t \ | \ t-1) = \hat{x}(t \ | \ t-1) + K(t)\cdot \left(y(t) - C\kern1px \hat{x}(t \ | \ t-1)\right)$
$\kern25px$$P(t \ | \ t) = \left[I - K(t) \kern1px C\right]\cdot P(t \ | \ t-1)$
$\kern25px$$\hat{x}(t+1 \ | \ t) = A \kern1px \hat{x}(t \ | \ t) + B \kern1px u(t)$
$\kern25px$$P(t+1 \ | \ t) = A \kern2px P(t \ | \ t) \kern1px A^T + G \kern1px Q \kern1px G^T$

The Wikipedia version of the algorithm: [KF Algorithm (Wikipedia)](https://en.wikipedia.org/wiki/Kalman_filter#:~:text=Predict%5Bedit,post%2Dfit%20residual)

> **NOTE**:
> We propagate also $P(t \ | \ t)$ from the past iteration of the loop not only $\hat{x}(t \ | \ t)$.
> Think of $P$ as the amount of uncertainty we have for the prediction $\hat x$.
%% > $\hat x$ is the center of our prediction space and $P$ gives the size of the space.%%


---
![[Pasted image 20220718183550.png]]
![[Pasted image 20220718183605.png]]
![[Pasted image 20220718183640.png]]
![[Pasted image 20220718183724.png]]
![[Pasted image 20220718183824.png]]
![[Pasted image 20220718183849.png]]
![[Pasted image 20220718183912.png]]
![[Pasted image 20220718184044.png]]
![[Pasted image 20220718184109.png]]
![[Pasted image 20220718184128.png]]
![[Pasted image 20220718184153.png]]
![[Pasted image 20220718184209.png]]
![[Pasted image 20220718184230.png]]
![[Pasted image 20220718184250.png]]

> **NOTE**:
> During the Lab session the professor doesn't use the eigenvalues of $P$ instead, it just takes the elements of the diagonal of $P$: $p_{1,1}$, $p_{2,2}$, $p_{3,3}$, $\ldots$


![[Pasted image 20220718184305.png]]
![[Pasted image 20220718184321.png]]
