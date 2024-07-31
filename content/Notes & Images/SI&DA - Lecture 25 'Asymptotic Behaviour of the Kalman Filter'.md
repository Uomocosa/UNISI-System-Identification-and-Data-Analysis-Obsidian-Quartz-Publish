###### Summary
**Discrete Riccati Equation**: an equation that governs the **covariance** $p(t+1 \ | \ t)$ given $p(t \ | \ t-1)$.

If we "compress" the whole **KF algorithm** of the following model:
$$
\begin{align}
&x(t+1) = a \kern1px x(t)
\\
&y(t) = x(t) + v(t)
\end{align}
$$
where: $v(t) \sim WP\left(0 ,\ \sigma_v^2 \right)$
into 2 equation, we obtain:
$$
\begin{align}
\hat{x}(t+1 \ | \ t) &= a \kern1px \hat{x}(t \ | \ t-1) + a \kern1px K(t) \kern1px (y(t) - \hat{x}(t \ | \ t-1))
\\
p(t+1 \ | \ t) &= a^2 \left(p(t \ | \ t-1) - \frac{p^2(t \ | \ t-1)}{p(t \ | \ t-1) + \sigma_v^2}\right)
\\
& = \frac{a^2 \cdot p(t \ | \ t-1) \cdot \sigma_v^2}{p(t \ | \ t-1) + \sigma_v^2}
\end{align}
$$
We defined this equation:
$$
p(t+1 \ | \ t) = \frac{a^2 \cdot p(t \ | \ t-1) \cdot \sigma_v^2}{p(t \ | \ t-1) + \sigma_v^2}
$$
as the **Discrete Riccati Equation** (for this particular model) and we analyzed what would happen for $t\to \infty$, we defined the following as the 
"**Algebric Riccati Equation**":
$$
\lim_{t \to \infty} p(\infty) = \frac{a^2 \cdot p(\infty) \cdot \sigma_v^2}{p(\infty) + \sigma_v^2}
$$
and we found 2 solution.
1. $p(\infty) = 0$ $\kern25px$ (which it will assume if $|a| \lt 1$, the system is asymptotically stable, given by a theorem)
2. $p(\infty) = \sigma_v^2 \kern1px (a^2 -1)$ $\kern25px$ (which it will assume if $|a| \gt 1$, the system is unstable)

---
![[Pasted image 20220719103839.png]]
![[Pasted image 20220719103902.png]]
![[Pasted image 20220719103920.png]]
![[Pasted image 20220719103941.png]]

#TODO ###### What does **detectable** mean ?
#TODO ###### What does **stabilizable** mean ?


![[Pasted image 20220719104008.png]]
![[Pasted image 20220719104127.png]]

---
![[Pasted image 20220719104234.png]]
![[Pasted image 20220719104340.png]]
![[Pasted image 20220719104403.png]]
![[Pasted image 20220719104420.png]]
![[Pasted image 20220719104441.png]]
![[Pasted image 20220719104502.png]]


Prediction using an **LTI Filter** (not good):
![[Pasted image 20220719104603.png]]
![[Pasted image 20220719104542.png]]

LTI Filters using 2 different constant $K$ (which is bad, while in the KF, $K$ varies with each iteration, this graph does **not** show a KF)
![[Pasted image 20220719104649.png]]
![[Pasted image 20220719104712.png]]
![[Pasted image 20220719104723.png]]
#TODO If there is time describe the graphs.


![[Pasted image 20220719104738.png]]
![[Pasted image 20220719104754.png]]
![[Pasted image 20220719104822.png]]
![[Pasted image 20220719104846.png]]
