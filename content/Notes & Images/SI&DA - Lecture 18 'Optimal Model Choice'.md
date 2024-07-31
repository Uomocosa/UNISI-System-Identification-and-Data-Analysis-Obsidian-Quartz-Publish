 ![[Pasted image 20220717181633.png]]
$\varphi$ : regressor
-> In case of **ARX** models the regressor does **not** depend on the unknown "parameter vector" $\theta$
-> In case of the other models, it does depend on it.

---

![[Pasted image 20220717182431.png]]
Where:
- $N$ : max value of $t$, $t \in \left[t_0 ,\ N \right]$
- $Z$  : Is the data set
- So $Z^N$ is the **Data Set** up to time $N$.

![[Pasted image 20220717182617.png]]
(In this case it's a **least square** function)
![[Pasted image 20220717182719.png]]
The filter $L(z)$ applied to the prediction error $\varepsilon$ is the same as filtering both output ($y(t)$) and input ($u(t)$).
We can see $L(z)H(z)^{-1}$ as a single filter.

A reason to design $L(z)$ could be if we are not interested in high frequency error, for example our system could have no response to high frequency input, then we could design $L(z)$ as a low pass filter, or another more general, example could be that we are just interested in a specific band of the system (pass-band filter).

---
We can create an ARX cost function as:
![[Pasted image 20220717183154.png]]
Then we will have that:
![[Pasted image 20220717183300.png]]
![[Pasted image 20220717184433.png]]
![[Pasted image 20220717184508.png]]
Also remember that $R(N) \in \mathbb{R}^{d\times d}$

![[Pasted image 20220717184637.png]]
![[Pasted image 20220717184723.png]]
![[Pasted image 20220717184758.png]]
![[Pasted image 20220717184914.png]]
![[Pasted image 20220717185123.png]]

---
![[Pasted image 20220717185346.png]]
![[Pasted image 20220717185402.png]]
![[Pasted image 20220717185430.png]]
Where in the last formula we can see:
![[Pasted image 20220717185529.png]]
![[Pasted image 20220717185601.png]]
![[Pasted image 20220717185632.png]]
![[Pasted image 20220717185715.png]]
![[Pasted image 20220717185744.png]]
![[Pasted image 20220717192913.png]]
![[Pasted image 20220717193007.png]]

---
![[Pasted image 20220717193215.png]]
![[Pasted image 20220717193253.png]]
![[Pasted image 20220717193340.png]]

---
