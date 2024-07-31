# System Identification
##### Main Elements of System Identification
- Data Set $Z^N$
- Model Class $\mathcal{M}$
- Cost Function $J$
- Validate the model
##### Parameter Vector $\theta$
##### A Priori Information $\Theta$
##### Gray Box / Black Box Models
##### Identification Process Algorithm
![[Pasted image 20220413114415.png]]
##### Principle of Parsimony
---
##### Parametric System Identification
##### Monic Polynomial
![[Pasted image 20220415103327.png]]
##### Generic Model Class
![[Pasted image 20220415110242.png]]
$G(z) := \frac{B(z)}{F(z)}$
$H(z) := \frac{C(z)}{D(z)}$
Also another possible parameter to be estimated is the delay $r$.

###### ARX (Auto Regressive eXoguenous) Model
![[Pasted image 20220415101717.png]]
###### FIR (Finite Impulse Response) Model
![[Pasted image 20220415101717- FIR Model.png]]
###### ARMAX (Auto Regressive Moving Average) Model
![[Pasted image 20220415103127.png]]
###### OE (Output Error) Model
![[Pasted image 20220415105238.png]]
###### BJ (Box Jenkins) Model
![[Pasted image 20220415105559.png]]

##### Meaning of Each Acronym

###### Auto Regressive
The output $\bar{y}$ in the system model is of this form: $y(t) + a_1 \kern2px y(t-1) + \ldots + a_{n_a} \kern2px y(t-n_a)$

###### Exogenous Inputs:
The input $\bar{u}$ in the system model is of this form: $b_1 \kern2px u(t-1) + b_2 \kern2px u(t-2) + \ldots + b_{n_b} \kern2px u(t-n_b)$

###### First Input Response
The output $\bar{y}$ in the system model is of this form: $y(t)$

###### Moving Average
The noise $\bar{e}$ in the system model is of this form: $e(t) + c_1 \kern2px e(t-1) + \ldots + c_{n_c} \kern2px e(t-n_c)$

###### Output Error
The error $e(t)$ is not filtered.

###### Box-Jenkins
Name of the first people to use this model, is the most complete model of all the ones seen up till now.

---
##### Choosing the Best Model
##### $\varepsilon(t, \ \theta)$ : Calculation
$$
\begin{array}{ll}
& \text{Starting from:} & y(t) = G(z) \kern2px u(t) + v(t)
\\
& \text{Arrive at:} & \varepsilon(t, \ \theta) = H^{-1}(z) \kern2px y(t) - H^{-1}(z) \kern2px G(z) \kern2px u(t)
\end{array}
$$

![[Pasted image 20220727233013.png]]
![[Pasted image 20220727233026.png]]

##### Regressor Vector
A vector containing all the past information $t \in \left[-\infty , \ t-1 \right]$ of $y(t), \ u(t) , \ \varepsilon(t)$; if any.

##### Error Function - ARX Model
![[Pasted image 20220415154929.png]]
We define the **Regressor Vector** as:
![[Pasted image 20220415155200.png]]
So that we can write:
![[Pasted image 20220415155224.png]]
![[Pasted image 20220415155427.png]]
Note how the error function is **linear** in $\theta$.

##### Error Function - ARMAX Model
$$
\begin{array}{ll}
& \text{Starting from:} 
& \hat{y}(t \ | \ t-1) = 
\left[1 - \large \frac{A(z)}{C(z)} \right] \kern0px y(t) + \large \frac{B(z)}{C(z)} \normalsize \kern0px u(t)
\\
& \text{Arrive at:} 
& \varepsilon(t) = \large  \frac{A(z)}{C(z)} \normalsize y(t) + \large \frac{B(z)}{C(z)} \normalsize  u(t)
\end{array}
$$
We also can find that:
$$
\hat{y}(t \ | \ t-1) = 
\left[1 - A(z) \right] \kern2px y(t) + B(z) \kern2px u(t) + \left[C(z) - 1 \right] \kern2px \varepsilon(t)
$$
So:
![[Pasted image 20220415155722.png]]
![[Pasted image 20220415155900.png]]
Note: 
$\varepsilon(t, \theta)$ is **non-linear** in $\theta$, ==the **pseudo-regressor** $\varphi$ contains past values of $\varepsilon$, which depend on $\theta$.==

##### Error Function - OE Model
$$
\begin{array}{ll}
& \text{Starting from:} 
& y(t) = w(t) + e(t)
\\
& \text{Arrive at:} 
& \hat{y}(t \ | \ t-1) = w(t)
\end{array}
$$
Since $w(t) = \hat{y}(t \ | \ t-1)$, the **pseudo-regressor** contains the terms $\hat{y}(t-1 \ | \ t-2), \ \hat{y}(t-2 \ | \ t-3) , \ \ldots ,\ \hat{y}(t-n_f \ | \ t-n_f-1)$, each of this **prediction** depends on $\theta$, so the error function $\varepsilon(t ,\ \theta)$ is **non-linear** in $\theta$.

##### Paradox of the Optimal Prediction
In the OE model, since $w(t) = \hat{y}(t \ | \ t-1)$, the **pseudo-regressor** contains the terms $\hat{y}(t-1 \ | \ t-2), \ \hat{y}(t-2 \ | \ t-3) , \ \ldots ,\ \hat{y}(t-n_f \ | \ t-n_f-1)$ so we theoretically need all the estimates from $t = -\infty$.
Similar with **ARMAX** model, the **pseudo-regressor** contains $\varepsilon$ values from $t-n_c$ , where $\varepsilon(t-n_c ,\ \theta)$ depends on $y$ starting from $y(t-n_c-n_a)$, which recursively depends on $\varepsilon(t-n_c-n_a-n_c)$ and so on.

To solve this "paradox" we consider all output and prediction before $t_0$ equal to $0$.

##### Prediction Error
###### Linear: ARM Models
###### Non-Linear: ARMAX, OE, BJ Models
---
##### Cost Function
![[Pasted image 20220717182431.png]]
![[Pasted image 20220717182617.png]]

##### Prediction Error Filter:
![[Pasted image 20220717182719.png]]

##### Cost Function - ARX Model
$$
\begin{array}{ll}
& \text{Starting from:} 
& V_N\left(\theta ,\ Z^N \right) = \large \frac{1}{2N} \sum_{t=1}^N \normalsize \varepsilon^2(t ,\ \theta)
\\
& \text{Arrive at:} 
& \hat{\theta}^{*} = R^{-1}(N) \cdot \large \frac{1}{N} \sum_{t=1}^N \normalsize \varphi(t) \kern1px y(t)
\end{array}
$$
![[Pasted image 20220727233058.png]]

##### Cost Function - ARMAX, OE, BJ Models
The ARMAX, OE, BJ Models are **non-linear** in $\theta$, so:
![[Pasted image 20220717193007.png]]
![[Pasted image 20220717193215.png]]
![[Pasted image 20220717193253.png]]

---
##### Preliminary Analysis of Data
![[Pasted image 20220718102846.png]]

##### Compare Different Model Classes / K-Step Ahead Prediction
![[Pasted image 20220718102856.png]]

##### Overfitting
![[Pasted image 20220718103216.png]]
![[Pasted image 20220718103250.png]]

##### Increase the Cost according to the Number of Parameters
![[Pasted image 20220718103327.png]]
![[Pasted image 20220718103352.png]]
##### Types of $U(d)$
- **AIC** : Akaike Information Criteria
- **FPE** : Final Prediction Error
- **MDL** : Minimum Description Length.

![[Pasted image 20220718103405.png]]

##### Change the Cost Function for Validation
![[Pasted image 20220718103608.png]]

---
##### Differentiate the Data Sets: Estimation and Validation
Usually the entire data set $Z^N$ it's split in half.

##### Residual Analysis
Estimate the covariance function between the prediction error $\varepsilon$ and the input $u$ and the variance of the prediction error $\varepsilon$.
![[Pasted image 20220718113758.png]]
Both of them have to be small $\forall \ \tau$ because we don't want the prediction error to have any relationship from the input or past residuals.
![[Pasted image 20220718113818.png]]
![[Pasted image 20220718113841.png]]

##### Whiteness Test of the Residuals
![[Pasted image 20220718114600.png]]

##### Input Selection
Things to remember when choosing an input for the system identification:
![[Pasted image 20220718114646.png]]
![[Pasted image 20220718114703.png]]
![[Pasted image 20220718114753.png]]
![[Pasted image 20220718114818.png]]

##### Typical Noises:
- **White Noise**
- **RBS** : Random Binary Sequence
- **PRBS** : Pseudo Random Binary Sequence
- **Sum of Sinusoids**
- **Chirp**
