### Random Variables
##### [[SI&DA - Definition of 'CDF (Cumulative Distribution Function)']]
##### [[SI&DA - Definition of 'PDF (Probability Density Function)']]
###### Uniform PDF
###### Gaussian PDF
##### [[SI&DA - Properties of the CDF and PDF]]
##### [[SI&DA - Multivariate Distributions]]
##### [[SI&DA - Definition of 'Joint CDF']]
##### [[SI&DA - Definition of 'Joint PDF']]
##### [[SI&DA - Definition of 'Marginal PDF']]
##### [[SI&DA - Mean & Variance]] (and Standard Deviation)
##### [[SI&DA - Definition of 'Confidence Interval']]
##### [[SI&DA - Definition of 'Covariance Matrix']]
##### [[SI&DA - Definition of 'Independent Random Variables']]
##### [[SI&DA - Definition of 'Uncorrelated Random Variables']]
##### [[SI&DA - Theorem 'Independent RVs are also Uncorrelated']]
##### [[SI&DA - Gaussian Random Variables]]
###### [[SI&DA - Theorem 'Independent or Uncorrelated Gaussian RVs']]
###### [[SI&DA - Property of Multivariate Gaussian RVs]]
##### [[SI&DA - Theorem 'Affine RV']]
##### [[SI&DA - Definition of 'Cross-Covariance']]
##### [[SI&DA - Central Limit Theorem]]
##### [[SI&DA - Functions of RVs]]
##### [[SI&DA - Multivariate Functions of RVs]]
##### [[SI&DA - Definition of 'Conditional Distribution']]
###### [[SI&DA - Definition of 'Conditional Mean']]
###### [[SI&DA - Definition of 'Conditional Variance and Covariance']]
###### Important Formulas for Gaussian Conditional Distribution
$$
f_{X|Y}(x \ | \ y) = \frac{f_{XY}(x ,\ y)}{f_{Y}(y)}
$$
$$
\begin{align}
& \text{If : } 
\left[\begin{array}{ll}
X \\ Y
\end{array}\right]
\sim
N \left(\begin{array}{ll}
\left[\begin{array}{ll}
m_x \\ m_y
\end{array}\right],
\left[\begin{array}{ll}
P_x & P_{xy} \\ P_{yx} & P_{y}
\end{array}\right]
\end{array}\right)
\\[10px]
& f_{X|Y}(x \ | \ y) = N(m_{x|y} ,\ P_{x|y})
\\
& m_{x|y}(y) = m_x + P_{xy} \kern1px P_y^{-1} \kern0px (y-m_y)
\\
& P_{x|y} = P_x - P_{xy} \kern1px P_y^{-1} \kern0px P_{xy}^T
\end{align}
$$
**NOTE**:
The new mean $m_{x|y}$ depends on the observation $y$, while the new covariance $P_{x|y}$ does not it depends only on the covariance and cross-covariance of $X$ and $Y$.

---
### Estimation Theory
#### [[SI&DA - Difference from Parametric and Bayesian Estimation]]
---
#### [[SI&DA - Parametric Estimation]]
##### [[SI&DA - Definition of 'Estimator']]
##### [[SI&DA - Definition of 'Unbiased Estimator']]
##### [[SI&DA - Definition of 'Consistent Estimator']]
##### [[SI&DA - Theorem 'Sequence of Unbiased Estimators']]
##### [[SI&DA - Theorem 'Law of Large Numbers']]
##### [[SI&DA - Definition of 'MSE (Mean Square Error)']]
##### [[SI&DA - Definition of 'MSE Estimator Comparison']]
##### [[SI&DA - Definition of 'Uniformly Minimum Variance Unbiased Estimator (UMVUE)']]
##### [[SI&DA - Definition of 'BLUE (Best Linear Unbiased Estimator)']]
##### [[SI&DA - Theorem 'The Cramer-Rao Bound']]
##### [[SI&DA - Definition of 'Efficient Estimator']]
##### [[SI&DA - Property the Fisher Information Matrix for i.i.d. RVs]]
##### [[SI&DA - Properties of the Sample Mean]]
##### [[SI&DA - Definition of 'Maximum Likelihood (ML) Estimators']]
##### [[SI&DA - Definition of 'Logarithmic Likelihood Function']]
##### [[SI&DA - Definition of 'Gauss-Markov Estimator']]
###### [[SI&DA - Least Square Estimator]]
###### [[SI&DA - Summary of GM and LS estimator Properties]]

---
#### Bayesian Estimation
##### [[SI&DA - Definition of 'Bayes Risk Function']]
##### [[SI&DA - Definition of 'Minimum Square Error Estimator']]
##### [[SI&DA - Definition of 'Linear Minimum Square Error Estimator']]
##### [[SI&DA - Theorem 'Schur Complement']]
##### [[SI&DA - Discrete solution to the Linear Minimum Square Error Estimate]]

----
#### [[SI&DA - Definition of 'Stochastic Process']]
##### [[SI&DA - Difference between Random Variable and Realization of a Stochastic Process]]
##### [[SI&DA - CDF and PDF of a Stochastic Process ]]
##### [[SI&DA - First and Second Order Statistics]]
##### [[SI&DA - Mean and Covariance of an SP]]
##### [[SI&DA - Definition of 'Strong Stationarity']]
##### [[SI&DA - Definition of 'Weak Stationarity']]
##### [[SI&DA - Theorem 'Covariance Function of a Stationary SP']]
##### [[SI&DA - Definition of 'Joint Stationarity']]
##### [[SI&DA - Properties of the Covariance Matrix of SPs]]
##### [[SI&DA - Definition of 'Normalized Covariance']]

----
##### Type of Stochastic Processes
###### [[SI&DA - Definition of 'Purely Deterministic SP']]
###### [[SI&DA - Definition of 'White SP']]
###### [[SI&DA - Definition of 'Wiener Process (or Brownian Motion)']]
###### [[SI&DA - Definition of 'Exponentially Correlated SPs']]

---
#### [[SI&DA - Linear Stochastic Systems]]
##### [[SI&DA - Time Shift Operator]]
##### [[SI&DA - Characteristic Polynomial]]
##### [[SI&DA - Free and Forced Response of the System]]
##### [[SI&DA - Transformation of an SP]]
##### [[SI&DA - Definition of 'Spectrum']]
##### [[SI&DA - Definition of 'Spectral Density']]
##### [[SI&DA - Definition of 'Cross-Spectrum']]
##### [[SI&DA - Properties of the Spectrum, Spectral Density and Cross-Spectrum]]
##### [[SI&DA - A General Result for Linear Stochastic Systems]]
##### [[SI&DA - Definition of 'Moving Average (MA) SP']]
##### [[SI&DA - Definition of 'Auto-regressive (AR) SP']]
##### [[SI&DA - Definition of 'Auto-regressive Moving Average (ARMA) SP']]

---
### [[SI&DA - Time Series Prediction]]
##### [[SI&DA - Spectral Factorization]]
##### [[SI&DA - k-Step Ahead Predictor]]
##### [[SI&DA - k-Step Ahead Prediction Error]]
