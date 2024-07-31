###### Summary
The **prediction error** $\varepsilon$ at time $t$ depending on the **parametric vector** $\theta$ is equal to:
$$
\varepsilon(t, \ \theta) = y(t) - \hat{y}(t \ | \ t-1, \ \theta)
$$
Can be written in 2 ways:
$$
\varepsilon(t, \ \theta)  =
\left\{
\begin{array}{l}
y(t) - \varphi^{T}(t)\cdot \theta
\\
y(t) - \varphi^{T}(t,\ \theta)\cdot \theta
\end{array}
\right.
$$
Where the ***1°*** one is related to **ARX** models, where the **regressor** $\varphi$ does not depend on the **parametric vector** $\theta$ .
While the ***2°*** one is related to **ARMAX**, **OE**, **BJ** models, and $\varphi(t,\ \theta)$ (which depends on $\theta$) is called **pseudo-regressor**.

---
# Choosing the Best Model
![[Pasted image 20220415112104.png]]
![[Pasted image 20220415112137.png]]
![[Pasted image 20220415112152.png]]
-> We have to predict the stochastic term.

![[Pasted image 20220415112431.png]]
So to calculate the stochastic term we make use of the data set $Z$ up to time $t-1$, then to remove the stochastic term from $y(t)$ we consider its mean.

![[Pasted image 20220415112512.png]]
![[Pasted image 20220415112555.png]]
We may right the cost function $J$ which depends on $\varepsilon(t, \ \theta)$ as a function $V_N$ that depends on $\theta$ and $Z^N$ after all, $\varepsilon$ is calculate using those two arguments.
Of course, we define the **optimal parameter vector** $\hat{\theta}^{*}$ as the one that minimizes the **cost function** $J$ or $V_N$.

---
# How can I predict the output ?
First we assume that $y(t)$ is given by the following function:
%%Where $e(t)$ is **Gaussian**, and its transformation $v(t)$ is a generic stochastic process.%%
You can thing of $v(t)$ as the filtered noise, while $e(t)$ is a generic stochastic preocess.
![[Pasted image 20220415112735.png]]
-> **Inversely Stable**: means that all zeros and poles of $H(z)$ lie inside the unit circle.

So:
![[Pasted image 20220415112851.png]]
Where you have to remember that $e(t)$ is **unpredictable**

Then, since **e(t)** is unpredictable our best bet is to predict $\hat{v}$ as:
![[Pasted image 20220415113023.png]]

Now we can calculate the prediction $\hat y(t \ | \ t-1)$:
![[Pasted image 20220415113005.png]]
- $[1 - H(z)]$ will not have constant terms, also it's grade will be at least $z^{-1}$ (or less $z^{-2}$, $\ldots$
So $\hat y(t \ | \ t-1)$ will depend only on past term of $y(t)$
- The same also holds for $H(z)^{-1} \kern2px G(z)$

The error $\varepsilon (t)$ will be
![[Pasted image 20220415154521.png]]

That will depend both on $t$ and $\theta$
![[Pasted image 20220415154611.png]]

-> We will choose $\theta$ such that we can minimize the previous cost function.

---
# ARX Model (Error Function)
-> #TODO [ARX Model]
![[Pasted image 20220415154909.png]]
![[Pasted image 20220415154929.png]]

Remember that this is the structure of the ARX Model
![[Pasted image 20220415155017.png]]

So we have that:
![[Pasted image 20220415155058.png]]

And $\theta$ is of the form: (already seen)
![[Pasted image 20220415155114.png]]

We can define the **regressor** vector as:
![[Pasted image 20220415155200.png]]

Such that:
![[Pasted image 20220415155224.png]]
-> Nothing changed from the explicit formula, it's just much more compact

![[Pasted image 20220415155427.png]]
> **NOTE**:
> The error is linear in $\theta$

---
# ARMAX Model (Error Function)
![[Pasted image 20220415155532.png]]
![[Pasted image 20220415155631.png]]
![[Pasted image 20220415155648.png]]

We can write the regressor as:
![[Pasted image 20220415155722.png]]
-> **pseudo-regressor** because it depends on $\theta$

**RESULT**:
![[Pasted image 20220415155900.png]]
-> Differently from #TODO [ARX Model (Error Function)] it is **non-linear** in $\theta$

---
# OE Model (Error Function)
![[Pasted image 20220415160109.png]]
![[Pasted image 20220415160122.png]]

The **pseudo-regressor** is:
![[Pasted image 20220415160145.png]]
-> **pseudo-regressor** because $w(t)$ depends on $\theta$, and so does $\varphi(t)$
-> $\varphi(t, \ \theta)$

![[Pasted image 20220415160337.png]]
-> Like [ARMAX Model (Error Function)] the $\hat y(t \ | \ t-1)$ is non-linear in $\theta$

---
# Paradox of the Optimal Prediction
![[Pasted image 20220415160525.png]]
- To know the prediction of $y(t-1)$ we need $y(t-2)$,
- But to know the prediction of $y(t-2)$ we need $y(t-3)$,
- And so on ...

![[Pasted image 20220415161043.png]]
-> Both the input and output starting from time $t -n_a$ (or $t-n_b$) up to $t-1$ are known (i can measure them)

While for the #TODO [OE Model (Error Function)] the **pseudo-regressor** depends on the $n_F$ past **predictions** which depend on all the past outputs (starting from $t = - \infty$) so like for the #TODO [ARMAX Model (Error Function)] the problem stands.
