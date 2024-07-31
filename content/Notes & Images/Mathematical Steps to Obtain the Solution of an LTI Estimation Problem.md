0. *Base Knowledge*:
![[Pasted image 20220723145023.png]]
1. Let's define the mean function of $x$ and $y$ and the variance function of $x$ as $m_x$ and $R_x(t, s)$:
![[Pasted image 20220723150031.png]]
Then we have that:
![[Pasted image 20220723150139.png]]
So:
![[Pasted image 20220723150302.png]]
2. For $m_y$ we have:
![[Pasted image 20220723150413.png]]
![[Pasted image 20220723150338.png]]
3. Let's now take into consideration the covariance function $R_x(t + \tau, \ t)$
Definition:
![[Pasted image 20220723150907.png]]
Substitute $x(t+\tau) = Ax(t+\tau-1) + \ldots$ and $m_x(t+\tau) = Am_x(t+\tau-1) + \ldots$ , then simplify :
![[Pasted image 20220723151023.png]]
Being $x(t)$ and $w(t)$ independent processes we have:
![[Pasted image 20220723151311.png]]
Since $w(t)$ is white, so we have that $w(t+\tau)$ and $w(t)$ are uncorrelated $\forall \ \tau \in \mathbb{R}$ we can say:
![[Pasted image 20220723151401.png]]
Where:
- $x(t) - m_x(t)$ only depends on the values of $w(i)$ for $i \leq t-1$ (more over it's a linear combination of $w(i)$ for $i \leq t-1$).
Then we can iterate an obtain:
![[Pasted image 20220723151950.png]]
So:
![[Pasted image 20220723152157.png]]
Now let's see what $R_x(t, t)$ is equal to, starting from the definition:
![[Pasted image 20220723152253.png]]
Like before we substitute $x(t+1)$ and $m_x(t+1)$:
![[Pasted image 20220723152307.png]]
Explicit form:
![[Pasted image 20220723152418.png]]
Since of $x(t)$ and $w(t)$ are uncorrelated, like we said before, $x(t) - m_x(t)$ only depends on the values of $w(i)$ for $i \leq t-1$, so:
$$
= \operatorname{E}\left[
\left(Ax(t)-m_x(t)\right)
\cdot
\left(Ax(t)-m_x(t)\right)^T
\right] +
\operatorname{E}\left[
G \kern1px w(t)
\kern1px
w^T(t) \kern1px G^T
\right]
$$
Where:
- $\operatorname{E}\left[\left(Ax(t)-m_x(t)\right)\cdot\left(Ax(t)-m_x(t)\right)^T\right] = A \kern1px R_x(t, t) \kern1px A^T$
- $\operatorname{E}\left[G \kern1px w(t) \kern1px w^T(t) \kern1px G^T\right] \triangleq G \kern1px Q \kern1px G^T$
For simplicity we call $R(t, t) = P(t+1)$ and declare the **Discrete Lyapunov equation** as:
![[Pasted image 20220723153200.png]]
It tells us how the variance $P(t)$ of $x(t)$ evolves in time, $x(t)$ is **not stationary**.
Finally we can conclude:
![[Pasted image 20220723153442.png]]
4. (no proof was provided)
![[Pasted image 20220723153517.png]]

---
# Remark
![[Pasted image 20220723153606.png]]
![[Pasted image 20220723153639.png]]
