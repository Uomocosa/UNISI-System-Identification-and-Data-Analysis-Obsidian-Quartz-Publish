# Linear Time Invariant (LTI) Models
![[Pasted image 20220415095305.png]]

Knowing that:
![[Pasted image 20220415095847.png]]

Then:
![[Pasted image 20220415100109.png]]
- And by the **probability density function** $f_e(e)$ of $e(t)$

---
# Parametric System Identification
![[Pasted image 20220415100646.png]]

If we assume that the noise is Gaussian also the [[SI&DA - Definition of 'PDF (Probability Density Function)'|pdf]] is known.

![[Pasted image 20220415100932.png]]

---
# ARX Model
**A**uto **R**egressive with e**X**oguenous inputs
![[Pasted image 20220415101247.png]]
-> Similar to an AR Model

Expect for this part:
![[Pasted image 20220415101330.png]]

> **NOTE**:
> The **AR** model is defined as:
> $y(t) + a_1 \kern2px y(t-1) + \ldots  + a_{n_a} \kern2px y(t-n_a) = e(t)$
 
We define:
![[Pasted image 20220415101405.png]]

So the **ARX Model** can be re-written as:
$$
A(z)\cdot y(t) = B(z)\cdot u(t) + e(t)
$$

And i can find that:
![[Pasted image 20220415101625.png]]

And I can represent the model as:
![[Pasted image 20220415101717.png]]

The **parametric vector model** $\theta$ is given by:
$$
\theta = [a_1, \ \ldots, \ a_{n_a}, \ b_1, \ \ldots, \ b_{n_b} ]^T
$$
Of dimensions: $\operatorname{dim}(\theta) = [(n_a+n_b) \times 1] \triangleq [d \times 1]$ 

![[Pasted image 20220415102051.png]]
(This strong assumptions is difficult to motivate)

---
# FIR Models
*Finite Impulse Response*
- *Subset of #TODO  [ARX Model]*

$$
\begin{array}{l}
n_a = 0
\\
\kern 15px \Rightarrow A(z) = 1
\end{array}
$$
Then the input/output response will be equal to:
![[Pasted image 20220415102340.png]]

---
# Monic Polynomial
$C(z)$ is defined as *monic* if it's "leading coefficient" (the ...) is $1$ and all the other coefficient are multiplied by $z^{-1}$, $z^{-2}$, $\ldots$, or $z^{-n}$ (resulting in a polynomial of grade 0)

###### ~Ex.:
![[Pasted image 20220415103327.png]]

---
# ARMAX Model
*#TODO [Auto Regressive Moving Average] with eXtrogenous Inputs*

![[Pasted image 20220415102940.png]]

We define:
![[Pasted image 20220415103008.png]]

So:
![[Pasted image 20220415103022.png]]

Model representation
![[Pasted image 20220415103127.png]]

![[Pasted image 20220415103201.png]]

> **NOTE**:
> $B(z)$ is not #TODO [monic]
> Because the system does not depend on the input at time $t$ : $u(t)$
> The input at time $t$ is just the noise $e(t)$

---
# OE Model
*Output Error*

We assume that
![[Pasted image 20220415104124.png]]

Where $w(t)$ is defined as:
![[Pasted image 20220415104145.png]]
-> Which is very similar to an #TODO [ARMAX Model], except for the noise that is moved to the formula above

We define:
![[Pasted image 20220415105004.png]]

So:
![[Pasted image 20220415105042.png]]
-> Which is different from an #TODO [ARX Model] because the error $e(t)$ is not filtered.

The structure of an OE model is defined as follows:
![[Pasted image 20220415105238.png]]

---

# BJ Model
*Box-Jenkins Model*, the name of this model is given after the 2 surnames of the guys that firstly used this model.

We define:
![[Pasted image 20220415105459.png]]

Where $D(z)$ is a #TODO [Monic Polynomial]:
![[Pasted image 20220415105535.png]]

The model structure is:
![[Pasted image 20220415105559.png]]

The **parametric vector model** $\theta$ is given by:
![[Pasted image 20220415105712.png]]
-> Differently from the #TODO [OE Model] is that we have new parameters: $c_1, \ \ldots, \ c_n$ and $d_1, \ \ldots, \ d_n$
This means having a more complex model, that results in:
-> More freedom
-> The identification process is more complex, so more prone to numerical errors

So for the #TODO [Principle of parsimony] if I can represent well my system with a more simple model (in this case the #TODO [OE Model]), I should do so.

---
# General Model Class
Let's group all the following model classes into one:
- #TODO [ARX Model]
- #TODO [FIR Model]
- #TODO [ARMAX Model]
- #TODO [OE Model] 
- #TODO [BJ Model]

![[Pasted image 20220415110242.png]]

So for:
- $A = F = C = D = 1$ -> We obtain an #TODO [FIR Model] (just $B(z) \neq 1$)
- $F = C = D = 1$ -> #TODO [ARX Model] ($A(z)$ and $B(z)$ $\neq 1$)
- $F = D = 1$ -> #TODO [ARMAX Model] ($A(z)$, $B(z)$ and $C(z)$ $\neq 1$)
- $A = C = D = 1$ -> #TODO [OE Model] ($B(z)$ and $F(z)$ $\neq 1$)
- $A = 1$ -> #TODO [BJ Model] ($B(z)$, $C(z)$, $D(z)$ and $F(z)$  $\neq 1$)

> **NOTE**:
> For the #TODO [Principle of parsimony] if I can represent the general system with a more simple model (one from the list above), I should do so.

---
# Delay in Input
![[Pasted image 20220415111232.png]]
![[Pasted image 20220415111247.png]]

If we know the delay $r$ we the problem is the same as #TODO [General Model Class].
Otherwise we have a new parameter to estimate, the delay $r$.