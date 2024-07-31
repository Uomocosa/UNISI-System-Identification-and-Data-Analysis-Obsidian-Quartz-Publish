### Markov Process:
For Markov process, we assume an [[DES - Definition of 'Independent Stochastic Process'|independent stochastic process]] where the assumption of independence is partially **relaxed**:

Given the **current** value of the process, the future values **do not depend** on the past.

###### Markov Property:
$$
\begin{align}
&P(X(t + \tau) \le \bar{x} \mid X(s) = x(s) \ \ \forall \ s \le t)
\\[5px]
& \kern 30px = P(X(t + \tau) \le \bar{x} \mid \textcolor{orange}{X(t) = x(t)})
\end{align}
$$
> Notice the difference with the [[DES - Definition of 'Independent Stochastic Process'#^57e9e3|Independent Stochastic Process Assumption]] where the process is also independent from the current value.

> **NOTE**:
> When writing $X(s) = x(s) \ \ \forall \ s \in [0, \ t]$ it means to consider all the sample path up to time $t$, how and when the states evolved.
> The equivalent in discrete time, (which is more clear to understand) is given by: $X(n) = x(n), \ X(n-1) = x(n-1), \ \ldots, \ x(0) = x(0)$

---
###### ~Example: 
![[Pasted image 20220124185921.png]]

If the processes are both **Markov processes** then the probabilities:
$$
P(X_1(t + \tau) \le \bar{x} \mid X_1(t) = x(t)) 
\kern 10px = \kern 10px
P(X_2(t + \tau) \le \bar{x} \mid X_2(t) = x(t)) 
$$
---
