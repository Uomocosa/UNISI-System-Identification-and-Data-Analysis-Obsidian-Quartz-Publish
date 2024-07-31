# Analytic Solution
The C-D KF has an analytic solution:
![[Pasted image 20220723100306.png]]

---
# Algorithm
> **NOTE**:
> Like the **KF** the **C-D KF** provides the **LMSE (Least Mean Square Error)** estimate $\hat{x}(t \ | \ t)$ of $x(t)$.

0. *Initialization*:
![[Pasted image 20220723100410.png]]
![[Pasted image 20220723100445.png]]
1. ***PREDICTION STEP***:
![[Pasted image 20220723100639.png]]
2. **CORRECTION STEP**:
![[Pasted image 20220723100710.png]]
3. *Iterate*, restart from point (1.)

---
###### ~Example 'Output of the **C-D KF** algorithm:':
![[Pasted image 20220723100810.png]]
