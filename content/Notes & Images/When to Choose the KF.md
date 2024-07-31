1. The system has to be **Linear**.
2. We know that the pdf of $f_x(x(t) \ | \ Y^t)$ is a **Gaussian distribution**.

> **NOTE**:
> $f_x(x(t) \ | \ Y^t)$ means: 
> pdf (probability distribution function) of $x(t)$ knowing the measurements ($Y^t$) up to time $t$.
---
- The **KF** will always provide the **LSME** (Lest Mean Square Error)* solution.
- If $w(t)$, $v(t)$ and $x(0)$ have **Gaussian distributions** the prediction will also be the **MSE** *(Mean Square Error)* solution.
- We can also write the pdf $f_x$ as:
$$
f_x(x(t) \ | \ Y^t) = \operatorname{N}\left(\hat{x}(t \ | \ t) ,\ P(t \ | \ t)\right)
$$
Where $\operatorname{N}$ means a Gaussian distribution with $\hat{x}(t \ | \ t)$ **mean**, and $P(t \ | \ t)$ **variance**.