---
tags:
  - Finance
  - CFA1
  - QM
  - Formula
---
The **[[variance]] of a two-asset portfolio** is given by:
$$V_{P}=w_{A}^2 \sigma_{A}^2 +w_{B}^2 \sigma_{B}^2+2\cdot w_{A}w_{B}\cdot \textcolor{red}{\text{Cov}_{A,B}}$$
 
Substituting the [[covariance]], we get:

$$V_{P}=w_{A}^2 \sigma_{A}^2 +w_{B}^2 \sigma_{B}^2+2\cdot w_{A}w_{B}\cdot\textcolor{red}{\sigma_{A}\sigma_{B}\cdot\rho_{A,B}}$$

# Proof %% fold %%
The variance of the sum of two variables is given by:
$$\begin{align*}
\text{V}(X+Y)
&= \text{Cov}(X+Y, X+Y) \\
&= \text{Cov}(X,X+Y)+\text{Cov}(Y,X+Y)\\
&= \text{Cov}(X,X)+\text{Cov}(X,Y)+\text{Cov}(Y,X)+\text{Cov}(Y,Y)\\
&= \text{V}(X)+2\text{Cov}(X,Y)+\text{V}(Y)
\end{align*}$$

If a portfolio is made of two assets $A$ and $B$ with weights of $w_{A}$ and $w_{B}$, respectively, then:


$$\begin{align*}
\text{V}(P)
&=\text{V}(w_{A}A+w_{B}B)\\
&=\text{V}(w_{A}A)+2\; \text{Cov}(w_{A}A,w_{B}B)+\text{V}(w_{B}B)\\
&=\text w_{A}^2{V}(A)+2\;w_{A}w_{B}\text{Cov}(A,B)+w_{B}^2\text{V}(B)\\
&=\text w_{A}^2{V}(A)+w_{B}^2\text{V}(B)+2\;w_{A}w_{B}\text{Cov}(A,B)\\
&=w_{A}^2 \sigma_{A}^2+w_{B}^2 \sigma_{B}^{2}+2\cdot w_{A}w_{B}\cdot\sigma_{A}\sigma_{B}\cdot\rho_{A,B}\\
\end{align*}$$

# Related formulas %% fold %%
## Variance of $X$
$\sigma^2(X)=\text{V}(X)=\text{Cov}(X,X)$

## Variance of a $X+Y$ 
$\text{V}(X+Y)=\text{V}(X)+\text{V}(Y)+2\text{Cov}(X,Y)$

![[Variance-covariance matrix of a two-asset portfolio (example).png#invert|200]]

## Variance of $aX+b$
$\text{V}(aX+b)=a^{2} \; \text{V}(X)$

## Covariance of $aX, bY$
$\text{Cov}(aX,bY)=ab \; \text{Cov}(X,Y)$

## Correlation coefficient; Covariance
$\rho_{X,Y}=\dfrac{\text{Cov}_{X,Y}}{\sigma_{X}\sigma_{Y}} \iff \text{Cov}_{X,Y}=\rho_{X,Y}\cdot\sigma_{X}\sigma_{Y}$


---
# See also
- [[Standard deviation of a two-asset portfolio]]
- [[Correlation coefficient]]
- [[V(X+Y)]]
