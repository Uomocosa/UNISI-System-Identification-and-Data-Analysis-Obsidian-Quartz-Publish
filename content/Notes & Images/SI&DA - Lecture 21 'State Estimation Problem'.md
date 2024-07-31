###### Summary
Introduction to the **State Estimation** problem, we have seen the **linear** case and defined the generic problem as:
$$
\begin{array}{l}
x(t+1) = A \kern1px x(t) + B \kern1px u(t) + G \kern1px w(t)
\\
y(t) = C \kern1px x(t) + v(t)
\end{array}
$$
where:
$$
\begin{align}
&\left[ \begin{array}{c} w(t) \\ v(t) \end{array} \right]
\sim WP\left(
\left(\begin{array}{c} 0 \\ 0 \end{array} \right),
\left(\begin{array}{cc} Q & 0 \\ 0 & R \end{array} \right)
\right)
\\[7px]
&x(0) \sim (m_0 ,\ P_0)
\end{align}
$$
Where:
- $x(t)$ is the **state** of the system
- $u(t)$ is the **deterministic input**
- $y(t)$ is the **output** of the system
- $w(t)$ is the **disturbance process**, a stochastic term, which takes into account the discrepancies of the model, whit respect to the real system.
- $v(t)$ is the **measurement noise**, a stochastic term

We have considered and will consider only the case in which the tre "stochastic sources" $w(t)$, $v(t)$ and $x(0)$ are **independent** (the initial condition for the state can be chooses at random).
Also we have considered $w(t)$ and $v(t)$ **White Processes** as shown above.

Our objective is to find at every time $t$ an **estimate** of $x(t)$, based on the knowledge of the input $u(t)$ and the output data:
$$
Y^t = 
\left[
\begin{array}{c} y(0) \\ y(1) \\ \vdots \\ y(t) \end{array} \right]
$$
This is a **Bayesian Estimation Problem**, we want to estimate the random variable $x(t)$ based on the observation of another random variable $y(t)$.
So from *Estimation Theory* we know that there are 2 possible solution to minimize the **MSE** (Mean Square Error):
1. $\hat{x}_{MSE}(t) = E\left[x(t) \ | \ Y^t \right]$
2. $\hat{x}_{MSE}(t) = m_x(t) + R_{x(t)Y^t}\cdot \left(R_{Y^t}\right)^{-1}\cdot \left(Y^t - m_{Y^t}\right)$


---
![[Pasted image 20220718164525.png]]
![[Pasted image 20220718164610.png]]
$p$ : position
$v$ : velocity
$u$ : acceleration
<br>

![[Pasted image 20220718164653.png]]
![[Pasted image 20220718164808.png]]
![[Pasted image 20220718164835.png]]
![[Pasted image 20220718164849.png]]
![[Pasted image 20220718164901.png]]
![[Pasted image 20220718164948.png]]
![[Pasted image 20220718165003.png]]
![[Pasted image 20220718165016.png]]
#TODO Why $E[\cdot] = 0$ ???

![[Pasted image 20220718165040.png]]
![[Pasted image 20220718165102.png]]
![[Pasted image 20220718165122.png]]
![[Pasted image 20220718165139.png]]
![[Pasted image 20220718165206.png]]
![[Pasted image 20220718165224.png]]
![[Pasted image 20220718165239.png]]
![[Pasted image 20220718165356.png]]
![[Pasted image 20220718165420.png]]