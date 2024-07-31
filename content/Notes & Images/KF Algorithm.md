![[Pasted image 20220723143345.png]]

>**NOTE**:
> Sometimes is possible to find $z(t)$ instead of $y(t)$ to indicate the measurement at time $t$.

---
0. *Initialization*: arbitrarily choose $\hat{x}(0 \ | \ -1)$, and $P(0 \ | \ -1)$
2. ***CORRECTION STEP***:
$$
\begin{align}
& S = C \kern1px P(t \ | \ t-1) \kern1px C^T + R
\\
& K = P(t \ | \ t-1) \kern1px C^T \kern0px S^{-1}
\\
& \hat{x}(t \ | \ t) = \hat{x}(t \ | \ t-1) + K \kern1px \left(y(t) - h(\hat{x}(t \ | \ t-1)) \right)
\\
& P(t \ | \ t) = \left[I - K \kern1px C \right] \kern1px P(t \ | \ t-1)
\end{align}
$$
1. ***PREDICTION STEP***:
$$
\begin{align}
& \hat{x}(t+1 \ | \ t) = 
A \kern1px \hat{x}(t \ | \ t) +
B \kern1px u(t)
\\
& P(t+1 \ | \ t) = 
A \kern1px P(t \ | \ t) \kern1px A^T +
G \kern1px Q \kern1px G^T
\end{align}
$$
3. *Iterate*.

> **NOTE**:
> Depending on the initial data the prediction step and the correction step can be inverted.