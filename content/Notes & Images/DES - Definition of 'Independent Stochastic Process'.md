### Independent Stochastic Process:
A [[DES - Definition of 'Stochastic Process'|stochastic process]] is called **independent** if the random variables:
$$
X(t_1), \ X(t_2), \ \ldots, \ X(t_h)
$$
are **independent**, for any choice of :
$$
t_1 < t_2 < \ldots < t_h \in \mathcal{T}, \kern 10px h = 2, \ 3, \ldots
$$
---
###### ~Example: 
Assume that you observed the stochastic process up to time $t$, and you want to infer (probabilistically) the value of the process at time $t + \tau$, using additional information provided by the observation.

![[Pasted image 20220124184648.png]]

For an independent process where:
$$
\begin{align}
&P(X(t + \tau) \le \bar{x} \mid X(s) = x(s) \ \ \forall \: s \le t) = 
\\[5px]
& \kern 30px = P(X(t + \tau) \le \bar{x})
\end{align}
$$

^57e9e3

The knowledge of the **past and current** values of the process does not change our inference with respect to the prior

---