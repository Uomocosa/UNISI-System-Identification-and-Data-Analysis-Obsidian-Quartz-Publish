# Professor Notes
[[notes_system_identification.pdf]]

---
# System Identification
![[Pasted image 20220412112127.png]]

Why do we need to find a model of the system?
-> Control the System
-> Prediction

---
###### ~Ex.:
![[Pasted image 20220412112544.png]]

Given the input i obtain the following output
![[Pasted image 20220412112623.png]]

-> Model of the System
![[Pasted image 20220412112655.png]]

Will be something like:
$y(t) = 4 \cdot u$ -> f(u) = $4 \cdot u$

---
###### ~Ex.:
Same input as before but the output is slightly different
![[Pasted image 20220412112849.png]]
(There is a delay in the input/output response)

-> $y(t) = 4 \cdot u(t-1)$

---
###### ~Ex.:
Same input, another output, this time really different from the output.

![[Pasted image 20220412113058.png]]

The solution this time around is:
$y(t) = -3 \cdot u(t-1) + 2\cdot u(t-2)$

---
###### ~Ex.:
![[Pasted image 20220412114544.png]]

Strangely the solution is the same as before:
$y(t) = -3 \cdot u(t-1) + 2\cdot u(t-2)$

This happens because of the **noise** affecting the system
![[Pasted image 20220412114715.png]]

-> The first 2 examples where noise-free, while in this example there is a noise.
-> We don't know the noise, it immeasurable.

---
# Noise
Assuming the noise is a Random Process that it's affecting the output we can model the system as:
![[Pasted image 20220412114858.png]]
Where:
-> $u(t)$ : input
-> $y(t)$ : output
-> $e(t)$ : noise

---
# Main Elements of System Identification
![[Pasted image 20220412115308.png]]
![[Pasted image 20220412115352.png]]

---
# Data Set
Characteristic of the Data Set
- **Data Set Domain**: in this course we will consider input/output data in the time domain (another possibility could be the frequency domain)
- **Length** of the Data Set
- **Sampling Time**

The input $u$ can be chosen by the user or not.
*~Ex.:* in an electrical circuit i can choose the input voltage and current (can be chosen by the user)
*~Ex.:* the input of the system is given by a controller (cannot be chosen by the user)

The input must be as *informative* as possible
![[Pasted image 20220412120055.png]]
-> The second definition of the input is much more meaningful

---
# Model Class: Parametric System Identification
![[Pasted image 20220413110837.png]]

What we will see is a kind of system identification called **Parametric System Identification**, this technique has the scope of finding the parameters that define a given model:
![[Pasted image 20220413111129.png]]

---
###### ~Ex.: Family of Transfer Functions
![[Pasted image 20220413111253.png]]

Then i can say that the "*parameter vector*" $\theta$ :
![[Pasted image 20220413111402.png]]
We want to find specific values of $K$ and $\alpha$, our parameters, we call this specific values $\theta$ the **parameter vector**.
While the family of all possible parameter vectors in this case $\left[K \in \mathbb{R} ,\ \alpha \in \left[0, \ 2 \pi \right]\right]$ is called $\Theta$ also called **a priori-information**.

Or i can say that:
![[Pasted image 20220413111534.png]]

---
# Model Class: Non-Parametric Models
For example i want to identify a model by its **impulse response**
Or maybe I'm interested in its **frequency response**

---
# Model Class: Gray or Black Box Model
If we have some prior information on the system.
*~Ex.:* if we have some physical information about the system.
Then we can use the "*Gray Box Model*".

Else if we **don't** have prior information we talk about "***Black Box Model***".

---
###### ~Ex.: Spring Dump Mass Model
![[Pasted image 20220413112234.png]]

We know the formula of the spring and dump, also the first law of Newton so we can use the **Gray Box Model**.

> **NOTE**:
> We can instead use the Black Box Model but we will throw away useful prior information, using only input and output response.

---
# Choice of the 'best' model
We want to find $\hat \theta ^*$ which minimizes a given cost function $J(\theta)$
![[Pasted image 20220413112728.png]]

The complexity depends on various elements:
- $J$ : the function i want to minimize
- $\operatorname{dim}(\theta)$ : how big is theta

Suppose you have a set of candidate models $\mathcal{M}$, then I want to choose a model inside $\mathcal{M}$ such that its "distance" is minimum from the theoretical model given by the input-output model (given for example by a Black Box Model).
> **NOTE**:
> We say this because often no model inside $\mathcal{M}$ respects the input-output model, and remember we can only chose a model inside $\mathcal{M}$.

-> So given a set of model $\mathcal{M}$ we need to **validate** them.

---
# Model Validation
Assess the quality of the model and it capacity to satisfy the requirements.
-> It must be able to predict (or simulate) future outputs

Given a system $S$ and the model $M$ we want to minimize the error $\varepsilon(t)$
![[Pasted image 20220413113632.png]]

Reasons to fail validation:
- Optimization process may not converge
*~Ex.:* due to numerical process (cannot find a feasible solution)
- Wrong choice of the cost function $J$
- Wrong choice of the model class $\mathcal{M}$
*~Ex.:* System of second order, we choose a first order model class
- The dataset is not informative enough

---
# Identification Process
An iterative process that I need to repeat until I find a good model.
-> A good practice is also to iterate even if I find a good model at first try.

![[Pasted image 20220413114415.png]]

---
# Principle of Parsimony
If i have 2 models that have same quality and same performance I prefer the **simplest one**.

---
