# System Identification & Data Analysis
- Corso del 1° Anno di Magistrale (2° Semestre).
- Docente: **Andrea Garulli** & **Marco Casini**.
- [Link to Drive with Video Lectures](https://drive.google.com/drive/u/1/folders/0AGmg-tnFIVvsUk9PVA)
- [Notes of an old course version](http://control.dii.unisi.it/iead/Dispense_v2.1.pdf)
										<br>
---
## Cheat Sheet
- [[Si&DA - Cheat Sheet - Part 1]]
- [[Si&DA - Cheat Sheet - Part 2]]
- [[Si&DA - Cheat Sheet - Part 3]]

---
## Mind Maps:
- [[SI&DA - Recap of Previous Courses - Mind Map]]
- [[SI&DA - System Identification - Mind Map]]
- [[SI&DA - State Estimation - Mind Map]]

---
## Perquisites:
- Introduction to linear algebra: [Professor Link](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/) | [[Linear Algebra - Index|my Notes]]
- Probability and statistics: [Professor Link](http://control.dii.unisi.it/ps/) | [[Probability and Statistics - Index|my Notes]]
- Dynamic systems: [Professor's Link](https://www3.diism.unisi.it/~control/sistdin-SI/) | [[Dynamic Systems - Index|my Notes]]
- [Tutorial for dynamic system analysis and simulation with MATLAB](http://control.dii.unisi.it/sistdin-SI/elaborati/Intro_Matlab_sist_din.m)

---
## Contents and Program:
###### *Estimation Theory*
- **Course Introduction**
- **Random variables**. Probability distributions. Mean and covariance. Conditional probability. Gaussian variables. 
- **Estimation theory**. Parametric estimation. Properties of estimators. Maximum likelihood estimators. Least squares and Gauss-Markov estimators. Bayesian estimation. Minimum mean square error estimators.
- **Stochastic processes and time-series prediction**. Distributions, mean and covariance function. Stationary processes. Frequency domain representation. Stochastic dynamic systems. Time-series models: AR, MA, ARMA. Time-series prediction.
										<br>
###### *System Identification*
- **System identification theory**. Identification of linear systems: prediction error methods. Input-output models: ARX, ARMAX, OE, BJ. Least squares estimator for linear regression models. Model validation.
- **Practical system identification**. Use of software tools for system identification.
										<br>
###### *State Estimation*
- **State estimation for linear systems**. Non stationary stochastic systems. The state estimation problem and the Kalman filter. Asymptotic properties of the Kalman filter. Recursive system identification.
- **State estimation for nonlinear systems**. State estimation in nonlinear stochastic systems. The Extended Kalman Filter. Advanced nonlinear filtering techniques: unscented filter; sequential Monte Carlo methods.

---
# Lectures
###### Probability & Statistics
[[SI&DA - Lecture 1 'Recap of Random Variables (RVs) - Part I']] ✓
[[SI&DA - Lecture 2 'Recap of Random Variables (RVs) - Part II']] ✓
[[SI&DA - Lecture 3 'Recap of Conditional Distributions']] ✓
[[SI&DA - Lecture 4 'Estimation Theory - Part I']] ✓
[[SI&DA - Lecture 5 'Estimation Theory - Part II']]
[[SI&DA - Lecture 6 'Maximum Likelihood Method']]
[[SI&DA - Lecture 7 'Linear Estimation Problems']]
[[SI&DA - Lecture 8 'Bayesian Estimation']]
[[SI&DA - Lecture 9 'Stochastic Processes']]
[[SI&DA - Lecture 10 'Example of Stochastic Processes']]
[[SI&DA - Lecture 11 'Linear Stochastic System']]
[[SI&DA - Lecture 12 'Frequency Domain Analysis of Stochastic Systems']]
[[SI&DA - Lecture 13 'MA AR and ARMA Processes']]
[[SI&DA - Lecture 14 'Time Series Prediction']]
###### System Identification
[[SI&DA - Lecture 15 'System Identification']]
[[SI&DA - Lecture 16 'LTI Models']]
[[SI&DA - Lecture 17 'Model Selection Criteria']]
[[SI&DA - Lecture 18 'Optimal Model Choice']]
[[SI&DA - Lecture 19 'Model Validation - Part I']]
[[SI&DA - Lecture 20 'Model Validation - Part II']]
###### State Evaluation
[[SI&DA - Lecture 21 'State Estimation Problem']]
[[SI&DA - Lecture 22 'Derivation of the Kalman Filter - Part I']]
[[SI&DA - Lecture 23 'Derivation of the Kalman Filter - Part II']]
[[SI&DA - Lecture 24 'Properties of the Kalman Filter']]
[[SI&DA - Lecture 25 'Asymptotic Behaviour of the Kalman Filter']]
[[SI&DA - Lecture 26 'Applications for the Kalman Filter']]
[[SI&DA - Lecture 27 'Recursive Parameter Estimation']]
[[SI&DA - Lecture 28 'The Extended Kalman Filter']]
[[SI&DA - Lecture 29 'The Continuous-Discrete Kalman Filter']]
[[SI&DA - Lecture 30 'The Unscented Kalman Filter - from Online Resources']]
[[SI&DA - Lecture 30 'The Unscented Kalman Filter']]
[[SI&DA - Lecture 31 'The Particle Filter']]

---
# Index
#### Course Introduction
- [[SI&DA - Professor Links]]
										<br>
#### Random variables
- [[SI&DA - Definition of 'CDF (Cumulative Distribution Function)']]
- [[SI&DA - Definition of 'PDF (Probability Density Function)']]
- [[SI&DA - Properties of the CDF and PDF]]
- [[SI&DA - Multivariate Distributions]]
- [[SI&DA - Definition of 'Joint CDF']]
- [[SI&DA - Definition of 'Joint PDF']]
- [[SI&DA - Properties of Multivariate PDF]]
- [[SI&DA - CDF of a Generic Surface]]
- [[SI&DA - Definition of 'Marginal PDF']]
- [[SI&DA - Mean & Variance]]
- [[SI&DA - Definition of 'Confidence Interval']]
- [[SI&DA - Mean of a Vector of RVs]]
- [[SI&DA - Definition of 'Covariance Matrix']]
- [[SI&DA - Definition of 'Independent Random Variables']]
- [[SI&DA - Definition of 'Uncorrelated Random Variables']]
- [[SI&DA - Theorem 'Independent RVs are also Uncorrelated']]
- [[SI&DA - Theorem 'Independent or Uncorrelated Gaussian RVs']]
- [[SI&DA - Theorem 'Independent or Uncorrelated Gaussian RVs']]
- [[SI&DA - Theorem 'Affine RV']]
- [[SI&DA - Definition of 'Cross-Covariance']]
- [[SI&DA - Property of Multivariate Gaussian RVs]]
- [[SI&DA - Central Limit Theorem]]
- [[SI&DA - Functions of RVs]]
- [[SI&DA - Multivariate Functions of RVs]]
- [[SI&DA - Definition of 'Conditional Distribution']]
- [[SI&DA - Definition of 'Conditional Mean']]
- [[SI&DA - Definition of 'Conditional Variance and Covariance']]
- [[SI&DA - Conditional PDF for Gaussian RVs]]
										<br>
#### Estimation Theory
- [[SI&DA - Estimation Problem]]
- [[SI&DA - Definition of 'Consistent Estimator']]
- [[SI&DA - Parametric Estimation]]
- [[SI&DA - Definition of 'Estimator']]
- [[SI&DA - Definition of 'Unbiased Estimator']]
- [[SI&DA - Theorem 'Sequence of Unbiased Estimators']]
- [[SI&DA - Theorem 'Law of Large Numbers']]

---
## Exercises and Examples:
#CollectionOf #SIandDA #Example
[[SI&DA - Definition of 'PDF (Probability Density Function)'#Ex Uniform PDF|Random variables ~ Ex.: "Uniform PDF"]]
[[SI&DA - Definition of 'PDF (Probability Density Function)'#Ex Gaussian PDF or Normal|Random variables ~ Ex.: "Gaussian PDF or Normal"]]
[[SI&DA - Properties of the CDF and PDF#Ex CDF and PDF of a Coin Toss|Random variables ~ Ex.: "CDF and PDF of a Coin Toss"]]
[[SI&DA - Lecture 2 'Recap of Random Variables (RVs) - Part II'#Ex Homework 1|Random variables ~ Homework 1]]
[[SI&DA - Lecture 2 'Recap of Random Variables (RVs) - Part II'#Ex Homework 2|Random variables ~ Homework 2]]

[[SI&DA - Lecture 3 'Recap of Conditional Distributions'#Ex Estimation Problem with Noise|Estimation Theory ~ Ex.: "Estimation Problem with Noise"]]
[[SI&DA - Lecture 4 'Estimation Theory - Part I'#Ex Sample Mean|Estimation Theory ~ Ex.: "Sample Mean"]]
[[SI&DA - Lecture 4 'Estimation Theory - Part I'#Ex Another Unbiased Estimator|Estimation Theory ~ Ex.: "Another Unbiased Estimator"]]
[[SI&DA - Lecture 4 'Estimation Theory - Part I'#Ex Sample Variance|Estimation Theory ~ Ex.: "Sample Variance"]]
[[SI&DA - Lecture 4 'Estimation Theory - Part I'#Ex Homework 3|Estimation Theory ~ Homework 3]]
[[SI&DA - Lecture 4 'Estimation Theory - Part I'#Ex Consistency of the Sample Mean|Estimation Theory ~ Ex.: "Consistency of the Sample Mean"]]

----
###### All My Notes
For the best experience in reading these and all other notes, and also if you wish to EDIT them, do as follows: 
1. Install [Obsidian](https://obsidian.md), or another markdown editor.
2. Go to the Github link of this or another note
3. Download all the repo or if you know git just the 'content/' folder
4. Extract just the 'content/' folder from the repo zip file
5. Open Obsidian >> Menage Vaults >> Open Folder as Vault >> and select the 'content/' folder you just extracted

==PLEASE NOTE==:
- These notes were not revised by the professors, so take all of them with a grain of salt.
- However if you download them since they are made in markdown you can EDIT them, please do so.
- If you edit and "upgrade" them, please pass the new ones to the other students and professors.

Here are all the links to my notes:
- ***Github***: [UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Sensors-and-Microsystems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Complex-Dynamic-Systems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Discrete-Event-Systems-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-System-Identification-and-Data-Analysis-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Multivariable-NonLinear-and-Robust-Control-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Artificial-Intelligence-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Human-Centered-Robotics-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Machine-Learning-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Machine-Learning-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Machine-Learning-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Machine-Learning-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Bioinformatics-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Bioinformatics-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Bioinformatics-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Bioinformatics-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Network-Optimization-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Network-Optimization-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Network-Optimization-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Network-Optimization-Obsidian-Quartz-Publish).
- ***Github***: [UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish](https://github.com/Uomocosa/UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish);<br>***Quartz Publish***: [UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish](https://uomocosa.github.io/UNISI-Mathematical-Methods-for-Engineering-Obsidian-Quartz-Publish).
