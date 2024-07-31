### Explanation of the Algorithm
~Example taken from [Youtube](https://www.youtube.com/watch?v=NrzmH_yerBU)

Given the map of a building an a robot with a laser sensor we want to estimate the position of the robot.
![[Pasted image 20220722174513.png]]

1. The robot could be anywhere on the map, to do this I take a finite set of randomly taken bot (random position, random orientation) and put the in a simulated map:
![[Pasted image 20220722174605.png]]
![[Pasted image 20220722174754.png]]
2. I take the measurement of the bot:
![[Pasted image 20220722174631.png]]
3. I estimate where the robot could be (considering a possible error in the measurements) and highlight the more probable simulated robots:
![[Pasted image 20220722174907.png]]
New simulated pdf:
![[Pasted image 20220722174941.png]]
4. Using the new pdf i re-randomize the simulated robots and their positions:
![[Pasted image 20220722175057.png]]
5. I repeat the process:
- Measurement.
![[Pasted image 20220722175243.png]]
- Estimation of pdf.
![[Pasted image 20220722175140.png]]
- Randomize new simulated robots.
![[Pasted image 20220722175306.png]]

This Algorithm is also known as **MCL (Monte Carlo Localization)**.
A variant of this algorithm, the **AMCL ( Adaptive Monte Carlo Localization)** reduces the number of simulated robots at each iteration, to speed up the algorithm, it's a little less precise, but much more quick.

---
# Algorithm
0. *Initialization*:
- We need to know the pdf: $f_x$, $f_w$, $f_v$ as well as the functions $f$ and $h$.
1. Generate $X^{(i)}$ $i = 1,\ \ldots ,\ p \kern10px$ **particles** according to the distribution $f_x(x(t) \ | \ Y^{t})$
2. Generate $W^{(i)}$ $i = 1,\ \ldots ,\ p \kern10px$ **particles** according to the distribution $f_w(w(t))$
3. $X^{(i)}_{t+1} = f\left(X^{(i)}_t ,\ u(t) ,\ W^{(i)}_t\right)$
Which are the particles rappresentative of the distribution $f_x(x(t+1) \ | \ Y^{t+1})$
4. $f_z(z(t)  \ |  \ X^{(i)}_t) = f_v\left(z(t) - h(X^{(i)}_t) \right)$
5. Generate a set of $p$ weights $q_i$ such that:
$$
\begin{align}
&q_i = \frac{f_z(y(t) \ | \ X^{(i)}_t)}{\sum_{j=1}^p f_z(z(t) \ | \ X^{(j)}_t)}
\kern25px i = 1 ,\ \ldots ,\ p
\\[7px]
&q_i \in \left[0 ,\ 1\right]
\\[10px]
&\sum_{i=1}^p q_i = 1
\end{align}
$$
6. Create a new **discrete** distribution function $f_x$ such that:
$$
\mathbb{P}\left\{x = X^{(i)}_t\right\} = q_i \kern25px i = 1 ,\ \ldots ,\ p
$$
7. Using the new $f_x$ restart from point (1.)