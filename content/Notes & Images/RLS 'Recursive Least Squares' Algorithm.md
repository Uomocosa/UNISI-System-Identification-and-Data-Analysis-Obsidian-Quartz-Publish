![[Pasted image 20220725162321.png]]
![[Pasted image 20220725162605.png]]
![[Pasted image 20220725162639.png]]

---
# Relationship between the RLS and the KF
Simple problem:
![[Pasted image 20220725162721.png]]
**KF** algorithm:
![[Pasted image 20220725162739.png]]
Correction step of the **KF** transformed to be really similar to the **RLS** algorithm:
![[Pasted image 20220725162755.png]]
Let's make a little transformation:
![[Pasted image 20220725162910.png]]
With this little transformation we will obtain the **RLS** algorithm from the correction step of the **KF** algorithm.
![[Pasted image 20220725163000.png]]

==We can see the **RLS** as the **KF** algorithm applied to a specific problem==, where the state doesn't change, in fact the parametric vector to identify the system (the original problem from which we obtained the **RLS**) must me constant.

![[Pasted image 20220725163124.png]]

---
# Extension to other estimation problem:
1. Slowly time-varying parameters:
![[Pasted image 20220725163436.png]]
![[Pasted image 20220725163517.png]]

2. RLS with exponential data weighting
![[Pasted image 20220725163553.png]]
The idea is that **older information is less useful**, sometimes ever wrong old information might be outdated.

Typical values of $\lambda$:
![[Pasted image 20220725163711.png]]

![[Pasted image 20220725163729.png]]

> **NOTE**:
> $\lambda \gt 1$ would mean that older information is more useful than new information.
> A smaller $\lambda$ will increase the reactivity of the system to new information but it will also increase uncertainty, this is way we choose an exponential $\lambda$ with value a little less than $1$.