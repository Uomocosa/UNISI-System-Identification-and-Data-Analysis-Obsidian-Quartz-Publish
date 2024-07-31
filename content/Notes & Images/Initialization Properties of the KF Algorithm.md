![[Pasted image 20220724103446.png]]
Where:
![[Pasted image 20220724103508.png]]

But a really nice property of the **KF** algorithm allows us to do so:
![[Pasted image 20220724103553.png]]
![[Pasted image 20220724103607.png]]

So we can just choose $P_0$ large enough such that $x_0$ belongs to the $3\sigma$ confidence interval, then the algorithm will adjust both $\hat{x}(t)$ and $P(t)$ every times it iterate.

But even if we choose $P_0$ too small, such that $x_0$ is not inside the $3\sigma$ confidence interval, the **KF** will still converge to the "optimal" solution **MSE** if the state of the problem is not Gaussian, **LSME** if it is Gaussian, tho is better to choose $P_0$ bigger, the **KF** will converge sooner.

> **NOTE**:
> This is **not** the case in **non-linear** systems, where if $P_0$ is too small or too large the algorithm might not converge, the linearization might fail.
