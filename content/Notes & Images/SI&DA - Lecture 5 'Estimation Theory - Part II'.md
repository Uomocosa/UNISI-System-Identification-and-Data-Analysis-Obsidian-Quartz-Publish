![[SI&DA - Definition of 'MSE (Mean Square Error)']]

---
![[SI&DA - Definition of 'MSE Estimator Comparison']]

---
### Definition of 'Uniformly Minimum Variance Unbiased Estimator (UMVUE)'
![[Pasted image 20220411114348.png]]
![[Pasted image 20220411114359.png]]
![[Pasted image 20220411114410.png]]

> **NOTE**:
> $v$ is a **vector**, $v \in \mathbb{R}^m$
> This theorem just says that the matrix $v \kern3px v^T$ is a **diagonal matrix**, and if we were to sum all the elements in the diagonal the result will be equal to $v^T \kern0px v$.
> Nothing too surprising.

![[Pasted image 20220411114419.png]]
![[Pasted image 20220411114428.png]]
![[Pasted image 20220411114436.png]]

---
### Definition of 'BLUE (Best Linear Unbiased Estimator)'
![[Pasted image 20220411114539.png]]

---
###### ~Ex.:
![[Pasted image 20220411114610.png]]
![[Pasted image 20220411114624.png]]
![[Pasted image 20220411114636.png]]
![[Pasted image 20220411114648.png]]

-> Then utilizing the [[HCR - Lagrangian Theorem|Lagrangian Function]]:
![[Pasted image 20220411114809.png]]
![[Pasted image 20220411114824.png]]
![[Pasted image 20220411114840.png]]
![[Pasted image 20220411114850.png]]

---
### Theorem 'The Cramer-Rao Bound'
![[Pasted image 20220411114919.png]]
![[Pasted image 20220411114928.png]]
![[Pasted image 20220411114937.png]]
![[Pasted image 20220411114949.png]]

---
### Definition of 'Efficient Estimator'
![[Pasted image 20220411115059.png]]
![[Pasted image 20220411115051.png]]
-> Where:
![[Pasted image 20220411115038.png]]
![[Pasted image 20220411115123.png]]

---
# Property the Fisher Information Matrix for i.i.d. RVs
i.i.d. RVs : *Independent Identically Distributed Random Variables*

$I_n(\theta)$ : Fisher information matrix


![[Pasted image 20220411115137.png]]

---
# Properties of the Sample Mean
The #TODO Sample Mean is an:
- #TODO **Efficient Estimator**
- #TODO **UMVU (Uniformly Minimum Variance Unbiased) Estimator**

Because its #TODO Fisher Information Matrix matches the #TODO Cramer-Rao Bound.

---
###### ~Dim.:
![[Pasted image 20220411115347.png]]
![[Pasted image 20220411115401.png]]
![[Pasted image 20220411115413.png]]

---
###### ~Ex.:
#SIandDA #Homework 
![[Pasted image 20220411115447.png]]