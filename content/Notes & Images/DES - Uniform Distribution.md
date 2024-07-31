[Wikipedia](https://en.wikipedia.org/wiki/Continuous_uniform_distribution)

---
# Uniform Distribution:
## PDF
"Probability Density Function"
![[Pasted image 20220121161056.png]]
### Formula:
$$
\Large
\left\{ 
\begin{array}{ccl}
\frac{1}{b - a} & for \space x \in \left[a, b\right]
\\
0 & otherwise
\end{array}
\right.
$$

---
## CDF
"Cumulative Distribution Function"
![[Pasted image 20220121161205.png]]
### Formula:
$$
\Large
\left\{ 
\begin{array}{ccl}
0 & for \space x < a
\\
\frac{x - a}{b - a} & for \space x \in \left[a, b\right]
\\
1 & otherwise
\end{array}
\right.
$$
---
### Notes:
- Notation: $\sim U(a,b)$
- Parameters: $- \infty \lt a \lt b \lt \infty$ 
- Support $x \in [a, b]$
- Mean: $\frac{1}{2}(a + b)$
- Median: $\frac{1}{2}(a + b)$
- Variance: $\frac{1}{12}(b - a)^2$
- The CDF is the differentiate of the PDF in respect to time:
$$
f_x(t) = \frac{dF_x(t)}{dt}
$$

---
