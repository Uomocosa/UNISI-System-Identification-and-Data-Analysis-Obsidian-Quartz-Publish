0. *Basic Knowledge* and *Notation*:
![[Pasted image 20220723145359.png]]
![[Pasted image 20220723145308.png]]
![[Pasted image 20220723154213.png]]
![[Pasted image 20220723154321.png]]

1. ***PREDICTION STEP***:
![[Pasted image 20220723154352.png]]
Define the problem
![[Pasted image 20220723154532.png]]
We could also write as our objective function the **LMSE (Least Mean Square Error)**, but it will bring the exact same result. 
For simplicity we will define:
![[Pasted image 20220723154755.png]]
And since we are searching for the **LMSE** estimator (or similar, the result will still be the LSME estimator):
![[Pasted image 20220723154824.png]]
We substitute $x(t+1)$
![[Pasted image 20220723154945.png]]
We use the previous definition of $\tilde{x}$:
![[Pasted image 20220723155021.png]]
We remove the uncorrelated part:
![[Pasted image 20220723155127.png]]
So only the products of *(1)*$\times$*(1)*$^T$ and *(2)*$\times$*(2)*$^T$ remains:
![[Pasted image 20220723155227.png]]
The variance is always positive, so by choosing $\hat{x}(t \ | \ t)$ such that the first component is $0$ is the best possible result, after all the second component only depends on $w(t)$ which I cannot change.
![[Pasted image 20220723155447.png]]
Now let's see how $P(t +1 \ | \ t)$ changes, starting from its definition as the covariance matrix of the error on the prediction $\hat{x}(t+1 \ | \ t)$:
![[Pasted image 20220723155810.png]]
Knowing that since $w(t)$ is a **white process**:
![[Pasted image 20220723155926.png]]
Then:
![[Pasted image 20220723160008.png]]
We can rewrite it as we have already seen as the **Discrete Lyapunov Equation**:
![[Pasted image 20220723160050.png]]

2. ***CORRECTION STEP***:
![[Pasted image 20220723154413.png]]
Define the problem:
![[Pasted image 20220723160212.png]]
Where:
- $y_1$ is the **measurement vector** obtained at time $t=1$
- $y_2$ is the **measurement vector** obtained at time $t=2$

We already know the solution of this problem:
![[Pasted image 20220723160251.png]]
Now we need to use all the information we got:
We know that $Y$ is divided in 2 parts $y_1$ and $y_2$, so:
![[Pasted image 20220723160441.png]]
We now make a **strong assumption**, we say that $y_1$ and $y_2$ are **uncorrelated**, unfortunately in most cases this is not the case:
![[Pasted image 20220723160534.png]]
The inverse of a **diagonal matrix** is:
![[Pasted image 20220723160605.png]]
We solve the matrix product:
![[Pasted image 20220723160623.png]]
Here we can say somenting:
![[Pasted image 20220723160649.png]]
But **unfortunately**, this works only if $y_1$ and $y_2$ are **uncorrelated**:
![[Pasted image 20220723160723.png]]

Let's now define the so called **Innovation Process**:
![[Pasted image 20220723161929.png]]
The idea behind it is that we want to correct using only the **new information** contained in $y_2$, so ignore from $y_2$ the old information, already seen in $y_1$.

We can see the innovation process as the error of what the sensor measured $y(t)$ (so the "almost" ground truth, whit an added noise $v(t)$) and what our model predicted: $C \hat{x}(t+1 \ | \ t)$

Doing some simple substitutions we have that the innovation process is equal to:
![[Pasted image 20220723162530.png]]

It also has some nice properties:
![[Pasted image 20220723162438.png]]
We say that $\hat{x}(t+1 \ | \ t)$ is a **linear combination** of $Y^{t}$, because we know that the mathematical model $f$ is **linear** and as we can see from $\hat{x}(t+1 \ | \ t)$ it is a prediction of $x(t+1)$ that depends on the measurement $y(t)$ up to time $t$, ergo it's a linear combination of $Y^t$.

Now we can define the "update" process as:
![[Pasted image 20220724100156.png]]

Since $e(t+1)$ is uncorrelated with $Y^t$:
![[Pasted image 20220724100239.png]]

![[Pasted image 20220724100354.png]]

Where:
![[Pasted image 20220724100523.png]]
By the definition of covariance:
![[Pasted image 20220724100554.png]]
Like we did previously:
![[Pasted image 20220724100740.png]]
We study how the double product interact with each other:
![[Pasted image 20220724100839.png]]
And we have that:
![[Pasted image 20220724101020.png]]
We can "delete" the last two terms:
![[Pasted image 20220724101146.png]]
And we have that $R_{x(t+1) \kern2px e(t+1)}$ is equal to:
![[Pasted image 20220724101305.png]]

We calculate also the variance of $e(t+1)$:
![[Pasted image 20220724101409.png]]
(Like before we can simplify because $v(t)$ is a **White Process**)

So we can say that
$$
\hat{x}(t+1 \ | \ t+1) = \hat{x}(t+1 \ | \ t+1) + R_{x(t+1) \kern2px e(t+1)} \cdot R_{e(t+1)} \cdot \left(e(t+1) - \operatorname{E}\left[e(t+1)\right]\right)
$$
is equivalent to:
![[Pasted image 20220724101518.png]]

We define the **Kalman Gain**:
![[Pasted image 20220724101926.png]]

Such that:
![[Pasted image 20220724101949.png]]

We have seen how $\hat{x}(t+1 \ | \ t+1)$ evolves, now let's see how $P(t+1 \ | \ t+1)$ evolves, starting as always by its definition:
![[Pasted image 20220724102041.png]]
We substitute the just found $\hat{x}(t+1 \ | \ t+1)$:
![[Pasted image 20220724102139.png]]
Then we substitute $x - \hat{x} = \tilde{x}$, and $y = Cx + v$ : 
![[Pasted image 20220724102155.png]]
Simple multiplication, and substitution for $x - \hat{x} = \tilde{x}$
![[Pasted image 20220724102340.png]]
We group $\tilde{x}$:
![[Pasted image 20220724102448.png]]
Like before:
- The covariance of something (different from $v(t)$) multiplied by $v(t)$ is **zero** since $v$ is a **White Process**.
- The variance of $v(t)$ is $R(t)$, as defined in the formulation of the problem.
- The covariance of $\tilde{x}(a, \ | \ b)$ is $P(a, \ | \ b)$, from the definition of $P$
- Also note that $I$, $K(t+1)$ and $C$ are not stochastic.
![[Pasted image 20220724102515.png]]

We can simplify the formula, first we develop the matrix multiplication:
![[Pasted image 20220724102855.png]]
Then we simplify:
![[Pasted image 20220724103108.png]]

Finally we obtain the last formula for the **KF** algorithm:
![[Pasted image 20220724103133.png]]
Can also be written as:
![[Pasted image 20220724103242.png]]
3. *Iterate*