1. Sensor fusion:
![[Pasted image 20220725154653.png]]
So given $p$ measurement of the same state $x(t)$, where each sensor has it's own model $C_p$, we can still apply the **KF** to find the estimate $\hat{x}$, this time with more information, so it's better.

2. Control
![[Pasted image 20220725154932.png]]
In adaptive control we can also change how the controller controls the system, this can be due to the lack of a mathematical model of the plant.

3. Fault detection:
![[Pasted image 20220725155210.png]]
![[Pasted image 20220725155232.png]]

4. Recursive system identification:
![[Pasted image 20220725155301.png]]
![[Pasted image 20220725155345.png]]
So we can only identify the system once "all" the output is given, or we can still use it at it is at each time $t$, but is not optimized. %%also note that we need $N \ge d$.%%
![[Pasted image 20220725155638.png]]
For simplicity let's define two function $R(t)$ and $f(t)$ such that:
![[Pasted image 20220725155751.png]]
So:
![[Pasted image 20220725155810.png]]
We can then write a recursive equation:
![[Pasted image 20220725155838.png]]
![[Pasted image 20220725155859.png]]
We have now obtained a recursive algorithm, to find the parameter vector $\theta$ :
![[Pasted image 20220725155928.png]]
Still the algorithm could be upgraded:
![[Pasted image 20220725162120.png]]
![[Pasted image 20220725162139.png]]
![[Pasted image 20220725162202.png]]
![[Pasted image 20220725162228.png]]
![[Pasted image 20220725162253.png]]
Finally we can summarize and define the **RLS (Recursive Least Squares)** algorithm:
![[Pasted image 20220725162321.png]]
