### Explanation of the Algorithm
1. Find the **sigma points**
2. Calculate the approximate **Gaussian distribution** of the state estimate using the **non-linear function** of the system and the **sigma points**, this approximation will replace the $P(t \ | \ t)$ **covariance matrix**. 
![[Pasted image 20220722173359.png]]
![[Pasted image 20220722172404.png]]
3. The newly calculated Gaussian pdf is then used to calculate the new estimate at $t+1$.
4. The estimate at $t+1$ is corrected using the measurements at $t+1$.

---
### Algorithm
0. *Initialization*:

1. Calculate the **mean** $m$ and **covariance matrix** $P$
$$
\begin{align}
& m = \sum_{i=1}^p W^{(i)} X^{(i)}
\\
& P = \sum_{i=1}^p W^{(i)} \cdot \left(X^{(i)} - m\right)\left(X^{(i)} - m\right)^T
\end{align}
$$
2. Calculate the **sigma points** $X^{(i)}$:
$$
\begin{align}
& p = 2n
\\
& X^{(i)} =
\left\{
\begin{array}{ll}
m + \left(\sqrt{n\cdot P}\right)_i & i = 1 ,\ \ldots ,\ n
\\
m - \left(\sqrt{n\cdot P}\right)_{i-n} & i = n+1 ,\ \ldots ,\ 2n
\end{array}
\right.
\\
& W^{(i)} =\frac{1}{2n} \kern25px i = 1 ,\ \ldots ,\ 2n
\end{align}
$$
3. Transform the sigma points using the **non-linear** state-update function $f$:
$$
\hat{X}^{(i)} = f(X^{(i)},\ u(t),\ \Omega^{(i)})
$$
Where:
- $\Omega^{(i)}$ are the sigma point of $w(t)$.
4. Approximate the pdf of the $\hat{X}^{(i)}$ points:
$$
\begin{align}
& m_x = \sum_{i=1}^p W^{(i)} \hat{X}^{(i)}
\\
& P_x = \sum_{i=1}^p W^{(i)} \cdot \left(\hat{X}^{(i)} - m_x\right)\left(\hat{X}^{(i)} - m_x\right)^T
\end{align}
$$
5. Transform the sigma points using the **non-linear** measurement function $h$:
$$
\hat{Z}^{(i)} = h(X^{(i)}) + V^{(i)}
$$
Where: 
- $V^{(i)}$ are the sigma point of $v(t)$.
6. Approximate the pdf of the $\hat{Z}^{(i)}$ points:
$$
\begin{align}
& m_z = \sum_{i=1}^p W^{(i)} \hat{Z}^{(i)}
\\
& P_z = \sum_{i=1}^p W^{(i)} \cdot \left(\hat{Z}^{(i)} - \hat{m}_z\right)\left(\hat{Z}^{(i)} - \hat{m}_z\right)^T
\\
& P_{xy} = \sum_{i=1}^p W^{(i)} \cdot \left(\hat{X}^{(i)} - \hat{m}_x\right)\left(\hat{Z}^{(i)} - \hat{m}_z\right)^T
\\[4px]
& m_x = m_x + P_{xy}\kern2px P_y^{-1}\left(z(t+1) - \hat{m}_z\right)
\\[9px]
& P_x = P_x - P_{xy} \kern2px P_y^{-1} \kern0px P_{xy}^T
\\[10px]
& \rightarrow \kern25px \operatorname{pdf}_x = \operatorname{N}(m_x,\ P_x)
\end{align}
$$
Where:
- $z(t+1)$ measured data.
7. *Iterate* repeating form point (2.)

---
