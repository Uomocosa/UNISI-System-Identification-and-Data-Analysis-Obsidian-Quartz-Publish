###### Summary
> **NOTE**:
> $P(t \ | \ t) := \operatorname{Var}\left[(x(t)-\hat{x}(t \ | \ t)\right]$
> Defined as "**covariance matrix of the prediction error**".

- ***PREDICTION STEP***: we compute the **one step ahead prediction** of $\hat{x}(t+1 \ | \ t)$, and for the **covariance of the prediction error** $P(t+1 \ | \ t)$, using the model $\mathcal{M}(A,\ B ,\ C ,\ G ,\ Q ,\ R)$.
- We then receive the measurement from the sensor at time $t+1$: $y(t+1)$.
- ***CORRECTION STEP***: with $y(t+1)$, the calculated predictions $\hat{x}(t+1 \ | \ t)$ and $P(t+1 \ | \ t)$, still using the same model $\mathcal{M}$ we compute  $\hat{x}(t+1 \ | \ t+1)$ and $P(t+1 \ | \ t+1)$.

---
![[Pasted image 20220718182039.png]]
![[Pasted image 20220718182116.png]]
![[Pasted image 20220718182135.png]]
![[Pasted image 20220718182155.png]]
![[Pasted image 20220718182211.png]]
![[Pasted image 20220718182225.png]]
![[Pasted image 20220718182242.png]]
![[Pasted image 20220718182258.png]]
![[Pasted image 20220718182317.png]]
![[Pasted image 20220718182334.png]]
![[Pasted image 20220718182428.png]]
![[Pasted image 20220718182453.png]]
![[Pasted image 20220718182509.png]]
![[Pasted image 20220718182531.png]]
![[Pasted image 20220718182627.png]]
![[Pasted image 20220718182650.png]]
#TODO Is e(t+1) an error???


![[Pasted image 20220718182726.png]]
##### What's $\mathcal{L}$ ? 
It means that $\hat{x}(t+1 \ | \ t)$ is a **linear combination** of $Y^t$

