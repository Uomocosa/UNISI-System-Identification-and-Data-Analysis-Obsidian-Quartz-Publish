![[Pasted image 20220725112746.png]]
So we can say that:
![[Pasted image 20220725113144.png]]

> **NOTE**:
> The $ii)$ condition can be relaxed and just technical, it grantees that there is a unique solution to the **ARE (Algebraic Riccati Equation)**, *you want to avoid non-reachable eigenvalues values on the unit circumference*.
> While the $i)$ condition is unavoidable, and it says that the non-observable eigenvalues have to be stable $|\lambda_i| \lt 1$, *if you cannot measure something it has to go to zero*.

1. $lim$ of the error $\tilde{x}$ :
![[Pasted image 20220725112825.png]]
Both limits go to $0$, no matter the initial value $\tilde{x}(0 \ | \ -1)$:
![[Pasted image 20220725113618.png]]


2. 
![[Pasted image 20220725112849.png]]
![[Pasted image 20220725113704.png]]

Solution of the **ARE (Algebraic Riccati Equation)**, in a specific linear case:
- $A \to a$
- $C \to 1$
- $Q \to 0$
- $R \to \sigma_v^2$

![[Pasted image 20220725115204.png]]
![[Pasted image 20220725115533.png]]

Why this is true, will be shown later.

3. $lim_{t \to \infty} \kern10px \bar{A}(t)$ 
Where, $\bar{A}(t)$ was defined in the "**KF** as a dynamic system":
![[Pasted image 20220725112905.png]]
Taking the results from the previous point (2.) of $P_{\infty}$
![[Pasted image 20220725114111.png]]

7. Let's take a simple version of the **DRE (Discrete Riccati Equation)**:
![[Pasted image 20220725151850.png]]
We study the curve:
![[Pasted image 20220725151911.png]]
So we obtain something like this:
![[Pasted image 20220725151951.png]]
Let's take a random $p(0)$:
![[Pasted image 20220725152024.png]]
To compute $p(1)$ we simply do:
![[Pasted image 20220725152047.png]]
So we take project $p(1)$ on the $x$ axis, using the $45°$ line $p(t+1) = p(t)$ and calculate $p(2)$:
![[Pasted image 20220725152208.png]]
As we iterate, as we can see we will have that $p(t \to \infty) = 0$
![[Pasted image 20220725152247.png]]
So we have shown graphically that that is true $\forall \ p(0) \gt 0$

Let's see what happens for $|a| \gt 1$, the starting graph looks something like:
![[Pasted image 20220725152440.png]]
The point where the two curves intersect is:
![[Pasted image 20220725152518.png]]
So now doing like we did before we will obtain the limit:
![[Pasted image 20220725152558.png]]
This is how we can find the two different solution of the **DRE** for $|a| \lt 1$ and $|a| \gt 1$.

> **NOTE**:
> $p(0) = 0$ is the only exception, for $p(0) = 0$, $p(\infty) = 0$ and not $\sigma_v^2 \left(a^2 -1 \right)$

Let's now see the case with the disturbance processes $w(t)$ and $v(t)$ : 
![[Pasted image 20220725152812.png]]
The theorem holds, so the **ARE** has an unique solution, as we can see solving the equation:
![[Pasted image 20220725153050.png]]
![[Pasted image 20220725153154.png]]
![[Pasted image 20220725153207.png]]
Where:
- The positive solution will be our man, $p_{\infty}$
- The negative solution, I don't care, the variance is always positive.
![[Pasted image 20220725153241.png]]
Even if $p(0) = 0$ the solution will always be $p(\infty)$.
