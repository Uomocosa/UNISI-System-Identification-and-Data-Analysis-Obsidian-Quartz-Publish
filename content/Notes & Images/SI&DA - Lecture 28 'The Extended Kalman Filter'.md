###### Summary
We want to apply the theory behind the **Kalman Filter** to **non-linear** system.
$$
\begin{array}{l}
x(t+1) = f\left(x(t) ,\ u(t) ,\ w(t)\right)
\\
y(t) = h\left(x(t) ,\ v(t)\right)
\end{array}
$$
We can use the algorithm for the **Extended Kalman Filter**, that we can found here: [EKF Algorithm (Wikipedia)](https://en.wikipedia.org/wiki/Extended_Kalman_filter#:~:text=Predict%5Bedit,u%7D%7D_%7Bk%7D%7D%7D)

The Idea behind the ***EKF*** is to linearize the two functions $f$ and $h$ using their **Jacobean Matrices** (derived for $x$, $v$ and $w$).

---
![[Pasted image 20220719164404.png]]
![[Pasted image 20220719164428.png]]
![[Pasted image 20220719164445.png]]
![[Pasted image 20220719164502.png]]
![[Pasted image 20220719164524.png]]
![[Pasted image 20220719164550.png]]
![[Pasted image 20220719164628.png]]
![[Pasted image 20220719164645.png]]
![[Pasted image 20220719164700.png]]
![[Pasted image 20220719165139.png]]
![[Pasted image 20220719165210.png]]
![[Pasted image 20220719165257.png]]
![[Pasted image 20220719165322.png]]
![[Pasted image 20220719165404.png]]
![[Pasted image 20220719165441.png]]
![[Pasted image 20220719165458.png]]
