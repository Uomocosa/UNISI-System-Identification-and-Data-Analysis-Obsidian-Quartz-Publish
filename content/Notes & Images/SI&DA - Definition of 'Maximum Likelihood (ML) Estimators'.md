### Definition of 'Maximum Likelihood (ML) Estimators'
![[Pasted image 20220411151010.png]]
![[Pasted image 20220411151100.png]]

The maximum likelihood estimator searches for the max value of the **pdf** function $f_Y^{\theta}(y)$ where $\theta$ is our **parameter** to be estimated, we have said that $\theta$ is also equal to the mean of this **pdf** which is also equal to its max value, here's way the **ML Estimator**.

---
### Theorem
If our observations $y_i$ are **independent** and **identically distribuited** then we can say:
$$
\mathcal{L}(\theta \ | \ y) = \prod_{i}^{n} f(\theta \ | \ y_i)
$$
---
###### ~Ex.:
For simplicity let's say that our parameter $\Theta$ can take only 3 values: 
![[Pasted image 20220411151214.png]]
![[Pasted image 20220411151231.png]]
![[Pasted image 20220411151246.png]]

---
> **NOTE**:
> The $T_{ML}$ is a **consistent** estimator

![[Pasted image 20220411151533.png]]

---
![[Pasted image 20220411151431.png]]
