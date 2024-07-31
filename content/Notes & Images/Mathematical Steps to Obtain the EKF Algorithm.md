0. *Starting Knowledge*:
![[Pasted image 20220723113622.png]]
![[Pasted image 20220723113656.png]]
1. **Taylor expansion** on the $f$ function:
![[Pasted image 20220723120248.png]]
2. Neglect the last term and we obtain:
![[Pasted image 20220723120359.png]]
Where:
$F(t) = \large \frac{\partial f}{\partial x}$ and $G(t) = \large \frac{\partial f}{\partial w}$ are **Jacobean matrices**
So we can re-write $x(t+1)$ as:
![[Pasted image 20220723120618.png]]
3. Calculate the estimate $\hat{x}(t+1 \ | \ t)$ of $x(t+1)$:
![[Pasted image 20220723120722.png]]
![[Pasted image 20220723120745.png]]
![[Pasted image 20220723120804.png]]
4. We have defined $P(t+1 \ | \ t)$ as the covariance matrix of the error of the prediction $\hat{x}(t+1 \ | \ t)$ and true value $x(t+1)$, so:
![[Pasted image 20220723120934.png]]
![[Pasted image 20220723120949.png]]
![[Pasted image 20220723121005.png]]
![[Pasted image 20220723121016.png]]

Exactly like in the linear case, the only difference is that $F$ and $G$ are now time varying matrices, so because $\tilde{x}$ and $w$ are uncorrelated we can write:
$$
= \operatorname{E}\left[F(t) \kern1px \tilde{x}(t \ | \ t) \kern1px \tilde{x}^T(t \ | \ t) \kern1pxF^T(t)\right] 
+
\operatorname{E}\left[G(t) \kern1px w(t) \kern1px w^T(t) \kern1pxG^T(t)\right]
$$
From the definition we gave to $P(t \ | \ t)$ we have that:
$$
\begin{align}
& P(t \ | \ t) := \operatorname{E}\left[\left(x(t) - \hat{x}(t \ | \ t)\right)
\cdot \left(x(t) - \hat{x}(t \ | \ t)\right)^T
\right]
\\
& \tilde{x}(t \ | \ t) = \left(x(t) - \hat{x}(t \ | \ t)\right)
\\[7px]
& \Rightarrow \kern{25px} \operatorname{E}\left[
\tilde{x}(t \ | \ t)
\cdot 
\tilde{x}^T(t \ | \ t)
\right] = P(t \ | \ t)
\end{align}
$$
And from the definition of Covariance Matrix, and knowing that the mean of $w$ is $0$:
$$
\begin{align}
& Q(t) := \operatorname{E}\left[
\left(w(t) - \bar{w}(t)\right)
\cdot 
\left(w(t) - \bar{w}(t)\right)^T
\right]
\\
& \bar{w}(t) = 0
\\[7px]
& \Rightarrow \kern{25px} 
\operatorname{E}\left[
w(t)
\cdot 
w^T(t)
\right]
= Q(t)
\end{align}
$$

We can conclude that:

![[Pasted image 20220723122645.png]]
And obtain the 2nd formula of the **EKF** algorithm:
![[Pasted image 20220723122727.png]]
5. We can now start with the correction step:
![[Pasted image 20220723122812.png]]
The following step will be very similar to the previous ones.
6. **Taylor expansion** of the $h$ function:
![[Pasted image 20220723122907.png]]
![[Pasted image 20220723122953.png]]
So we have:
$$
\begin{align}
& d(t+1) := x(t+1) - \hat{x}(t + 1 \ | \ t)
\\
& m(t+1) := y(t+1) - h\left(\hat{x}(t + 1 \ | \ t)\right)
\\
& h(t+1) \simeq 
h\left(\hat{x}(t + 1 \ | \ t)\right) + 
H(t+1) \kern1px d(t+1)
\\
& \Rightarrow \kern25px m(t+1) = H(t+1) \kern1px d(t+1) + v(t+1)
\end{align}
$$
7. After declaring $d(t+1)$ we need to find its estimate:
$$
\begin{align}
& \hat{d}(t+1) := \operatorname{E}[d(t+1)]
\\
& d(t+1) = x(t+1) - \hat{x}(t + 1 \ | \ t)
\\[7px]
& \Rightarrow \kern25px \operatorname{E}[d(t+1)] = \hat{x}(t+1 \ | \ t) - \hat{x}(t + 1 \ | \ t)
\\[7px]
& \Rightarrow \kern25px \hat{d}(t+1) = 0
\end{align}
$$
8. Its covariance:
![[Pasted image 20220723124134.png]]
9. Then we can say that, using the same formulas from the **KF** algorithm:
![[Pasted image 20220723124216.png]]
![[Pasted image 20220723124325.png]]
Obtaining the 3rd formula of the **EKF** algorithm:
![[Pasted image 20220723125211.png]]
10. Where the **Kalman Gain**, $K(t+1)$, is given by:
![[Pasted image 20220723124256.png]]
(4th formula of the **EKF** algorithm, taken from the **KF** algorithm)
11. Also taken from the **KF** algorithm, the 5th formula of the **EKF** algorithm:
![[Pasted image 20220723125059.png]]
