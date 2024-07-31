1. The system is **Non-Linear** but **Locally Linear**, the function of state-update $f$ and measurement $h$ will be **locally linearized**.
2. We know that the pdf of $f(x(t) \ | \ Y^t)$ is **approximately** a **Gaussian distribution**.

> **NOTE**:
> $f(x(t) \ | \ Y^t)$ means: 
> pdf (probability distribution function) of $x(t)$ knowing the measurements ($Y^t$) up to time $t$.

---
- In case the approximation is not satisfactory, for example:
![[Pasted image 20220722170740.png]]
real distribution (in black), resulting distribution (in red).
We can use more accurate alternatives:
The **UKF (Unscented Kalman Filter)**.
Or the **PF (Particle Filter)**.

---