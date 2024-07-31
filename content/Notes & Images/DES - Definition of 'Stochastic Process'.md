### Stochastic Process:
A **stochastic process** $\left\{ X(t) \right\}$ is a collection of random variables $X(t) \in \mathcal{X}$, indexed by time $t \in \mathcal{T}$.
- If the time set $\mathcal{T}$ is **discrete**, ex.: $\mathcal{T} = \{0, \space 1, \space 2, \space \ldots\}$ the stochastic process is in **discrete time**
- If the time set $\mathcal{T}$ is **continuous**, ex.: $\mathcal{T} = \mathbb{R}^{\ge 0}$ the stochastic process is in **continuous time**
- If the time set $\mathcal{X}$ is **discrete**, the stochastic process is called [[DES - Definition of 'Chain'|chain]]
- A realization of the stochastic process $\left\{ X(t) \right\}$ is denoted $x(t)$

- A stochastic process is specified by all possible **joint distributions** of its random variables:
$$
\begin{align}
&P(X(t_1) \le x_1, \ X(t_2) \le x_2, \ \ldots, \ X(t_h) \le x_h)
\\[5px]
&\forall \: 0 \le t_1 \le t_2 \le \dots \le t_h, 
\\[5px]
&\forall \: 0 \le x_1 \le x_2 \le \dots \le x_h, 
\\[5px]
&\forall \: h = 1,\space 2,  \space 3, \space \ldots 
\end{align}
$$

- A stochastic process is called **(strongly) stationary** if these distributions are invariant with respect to a shift in time:
$$
\begin{align}
&P(X(t_1 + \textcolor{#018786}{\tau}) \le x_1, \space X(t_2 + \textcolor{#018786}{\tau}) \le x_2, \space \ldots, \space X(t_h + \textcolor{#018786}{\tau}) \le x_h, \space ) = 
\\[5px]
& \kern 30 px = P(X(t_1) \le x_1, \space X(t_2) \le x_2, \space \ldots, \space X(t_h) \le x_h, \space )
\\[10px]
&\forall \: 0 \le t_1 \le t_2 \le \dots \le t_h, 
\\[5px]
&\forall \: 0 \le x_1 \le x_2 \le \dots \le x_h, 
\\[5px]
&\forall \: h = 1,\space 2,  \space 3, \space \ldots 
\\[5px]
&\forall \: \textcolor{#018786}{\tau} > 0
\end{align}
$$
---
### Observation:
Notice that **strong stationarity** implies all the random variables $X(t)$ are **identically distributed**

Suppose: $h = 1$, then:
$$
\begin{align}
&P(X(t_1 + \textcolor{#018786}{\tau})) = P(X(t_1) \le x_1)
\\[5px]
&\forall \: 0 \le t_1 \le t_2 \le \dots \le t_n, 
\\[5px]
&\forall \: 0 \le x_1 \le x_2 \le \dots \le x_n, 
\\[5px]
&\forall \: h = 1,\space 2,  \space 3, \space \ldots 
\end{align}
$$
---
###### ~Example: continuous state
$\mathcal{T}$ continuous
$\mathcal{X}$ continuous
![[Pasted image 20220124142000.png]]

###### ~Example: discrete state
$\mathcal{T}$ continuous
$\mathcal{X}$ discrete
![[Pasted image 20220124142113.png]]