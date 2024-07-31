0. *Initialization*
![[Pasted image 20220723113622.png]]
![[Pasted image 20220723113656.png]]
1. ***PREDICTION STEP***:
$$
\begin{align}
\\
& F_x = \left. \frac{\partial f}{\partial x} \right|_{
	\begin{array}{l}
	\large x = x(t+1)
	\end{array}
}
\\
& F_w = \left. \frac{\partial f}{\partial w} \right|_{
	\begin{array}{l}
	\large x = x(t+1)
	\end{array}
}
\\[10px]
& \hat{x}(t+1 \ | \ t) = f(x(t) ,\ u(t) ,\ w(t))
\\
& P(t+1 \ | \ t) = F_x\kern1pxP(t \ | \ t)\kern1px F_x^T +  F_v \kern1px Q \kern1px F_v^T
\end{align}
$$
2. ***PREDICTION STEP***:
$$
\begin{align}
& H_x = \left. \frac{\partial h}{\partial x} \right|_{
	\begin{array}{l}
	\large x = \hat{x}(t+1)
	\end{array}
}
\\
& H_v = \left. \frac{\partial h}{\partial v} \right|_{
	\begin{array}{l}
	\large x = \hat{x}(t+1)
	\end{array}
}
\\[10px]
& S = H_x \kern1px P(t+1 \ | \ t) \kern1px H_x^T + H_w \kern1px R \kern2px H_w^T
\\
& K = P(t+1 \ | \ t)\kern1px H_x^T \kern1px S^{-1}
\\[10px]
& x(t+1 \ | \ t+1) = \hat{x}(t+1 \ | \ t) + K \left(z(t+1) - h\left(\hat{x}(t+1 \ | \ t)\right)\right)
\\
& P(t+1 \ | \ t+1) = \left[I - K \kern1px H_x \right] \kern1px P(t+1 \ | \ t)
\end{align}
$$
Where:
- $z(t+1)$ is the measurement at time $t+1$.
