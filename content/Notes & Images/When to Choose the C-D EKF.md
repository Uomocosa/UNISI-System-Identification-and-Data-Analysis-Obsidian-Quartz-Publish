1. The system is **Non-Linear**.
2. We know that the pdf of $f(x(t) \ | \ Y^t)$ is **approximately** a **Gaussian distribution**.
3. The **EKF (Extended Kalman Filter)** gave bad results, or failed, and we can suppose that the bad result were given to a not-so-good linearization of the function $f$.

> **NOTE**:
> $f(x(t) \ | \ Y^t)$ means: 
> pdf (probability distribution function) of $x(t)$ knowing the measurements ($Y^t$) up to time $t$.