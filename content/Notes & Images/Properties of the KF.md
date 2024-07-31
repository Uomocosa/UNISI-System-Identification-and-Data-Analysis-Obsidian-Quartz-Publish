1. As we have seen the prediction of the covariance of the error $P(t \ | \ t)$ is equal to:
![[Pasted image 20220725100914.png]]
Which is **non-linear** in $P(t-1 \ | \ t)$
If we define the **Information Matrix** as:
![[Pasted image 20220725101007.png]]
Using the **matrix inversion Lemma**:
![[Pasted image 20220725101100.png]]
with:
![[Pasted image 20220725101137.png]]
We obtain:
![[Pasted image 20220725101158.png]]
We can simplify and rename $P(t \ | \ t)^{-1}$ as $I(t \ | \ t)$:
![[Pasted image 20220725101319.png]]
![[Pasted image 20220725101340.png]]
So:
![[Pasted image 20220725101357.png]]
We can see the argument $C^T R^{-1}C$ as:
![[Pasted image 20220725101507.png]]
![[Pasted image 20220725101549.png]]

---
2. Complexity of the **KF algorithm**:
![[Pasted image 20220725101624.png]]
We can reduce the complexity if we propagate $\sqrt{P}$, so we can reduce its size (from square matrix to a vector).
 ![[Pasted image 20220725101648.png]]

---
3. Let us consider the KF as a dynamical system:
![[Pasted image 20220725102133.png]]
To do this we substitute the 2nd expression of the **KF** algorithm:
![[Pasted image 20220725102303.png]]
Into the 4th:
![[Pasted image 20220725102324.png]]
as to obtain a single expression to update the state:
![[Pasted image 20220725102359.png]]
We group $\hat{x}$, $u(t)$ and $y(t)$:
![[Pasted image 20220725102440.png]]
This is now a dynamic system, where the matrices $A, B, C, D$ are defined as follows:
![[Pasted image 20220725102544.png]]

> **NOTE**:
> The **KF** is a **LTV (Linear Time Varying)** dynamic system

The output $\tilde{x}$ is:
![[Pasted image 20220725102654.png]]
We can now group to obtain:
![[Pasted image 20220725102720.png]]
So the complete system can be re-written a dynamic system with matrices:
![[Pasted image 20220725102758.png]]

> **NOTE**:
> It is independent form the input $u(t)$.
> The source of the error are the noises $w(t)$ and $v(t)$.

Then, the **MSE**:
![[Pasted image 20220725102912.png]]
Now we can say, since it is iterative, that:
![[Pasted image 20220725103303.png]]
Tho it's also true that:
![[Pasted image 20220725103335.png]]

We can see how $P$ evolves with time, and see if we can describe it as a dynamic system.
![[Pasted image 20220725103439.png]]
The independent entries are not $n^2$ because the state, the matrix $P$ is a symmetric, so they are $\frac{n (n+1)}{2}$ independent entries.

Also the system is **Non-Linear** in $P$, because of the second component of the equation.

But if the model $\mathcal{M}$ is time invariant, specifically $A, C, Q, R$ do not depend on time, are constant matrices then this dynamic system is **Time-Invariant** (still non-linear).

4. As we have seen in the previous point:
![[Pasted image 20220725104329.png]]
![[Pasted image 20220725104402.png]]
![[Pasted image 20220725104425.png]]

5. The **KF** is a **state observer**:
Let's consider only the deterministic part of the **KF** base system:
![[Pasted image 20220725104618.png]]
We know that for this system we can construct a state observer:
![[Pasted image 20220725104709.png]]
![[Pasted image 20220725104747.png]]
(The system becomes asymptotically stable).

So if the system is asymptotically stable the error will converge to zero, and the estimate of the state will be equal to the actual state, that's why it's called **asymptotic** observer.

Is it always possible to do this?
A sufficient condition is:
![[Pasted image 20220725105140.png]]
Where $n$ is the dimension of the state.

%% In the case of the **KF**, this is never the case tho, the noises $w$ and $v$ are not observable. %%

Another condition, less strict condition is:
![[Pasted image 20220725105305.png]]
![[Pasted image 20220725105506.png]]

---
6. Let us consider now the innovation process as as dynamic system:
![[Pasted image 20220725105543.png]]
This uncorrelation is what allowed us to do a recursive correction step in the **KF** algorithm. 