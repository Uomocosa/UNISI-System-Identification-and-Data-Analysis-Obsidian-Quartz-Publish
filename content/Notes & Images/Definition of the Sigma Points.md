- The sigma points: $X^{(i)} \in \mathbb{R}^n, \kern15px i = 1,\ \ldots ,\ p$
- The associated weights: $W^{(i)} \in \mathbb{R}^n, \kern15px i = 1,\ \ldots ,\ p$, such that:
$$\sum_{i=1}^p W^{(i)} = 1$$
- $p \in N$ is choose arbitrarily, more sigma points means more accuracy, but more computational cost.
- The minimum number of sigma points that can be taken is $p = 2n$.
- $n$ is the dimension of $x(t)$, we can write $x(t) \in \mathbb{R}^n$
- Sigma points are selected such that their mean $\mu$ and covariance $P$ are the same as the pdf.
![[Pasted image 20220722172324.png]]
- Also the sigma points are distributed symmetrically with respect to the mean of the pdf.

---
###### ~Example
Let's see a generic example on how to calculate the sigma points:
![[Pasted image 20220722175726.png]]
Where:
- $p$ and $n$ were defined before.
- $m$ is the mean of $x(t \ | \ t)$.
- $P$ is the covariance matrix of $x(t \ | \ t)$.
- $M$ is the just a place holder matrix to understand the notation, below the explanations of the notations used.
- When we say:
$$
\left(\sqrt{n\cdot P}\right)_i
$$
we mean the $i$-th column of $\sqrt{n\cdot P}$
- To calculate $\sqrt{n\cdot P}$ you can use the `sqrtm` function on MATLAB.
