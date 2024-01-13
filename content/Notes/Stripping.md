---
tags:
  - Finance
---
**Stripping** is a type of [[Arbitrage opportunity]] opportunity that occurs when the [[Value additivity principle]] does not hold. If the value of the whole is lower than the sum of the parts:
1. Buy the whole (lower)
2. Strip it into parts
3. Sell the parts (higher)
4. Pocket the difference

> [!Example]- 
> A three-year bond with a 10% annual coupon and $1,000 face value is priced at $1,000, and the Treasury spot rates are given by:
>  
> | Year | Spot rates |
> | :----: | :----------: |
> | 1    | 7%         |
> | 2    | 8%         |
> | 3    | 7%         |
> 
  > The value of this bond (sum of the parts) is:
  > $$V=\frac{100}{1.07}+\frac{100}{1.08^2}+\frac{1,100}{1.07^{3}}=1,077.12>1,000$$
  > 
  > An arbitrage opportunity exists:
  > 1. Buy the bond at the current market price of $1,000
  > 2. Strip the security into three zero coupon bonds 
  > 	- $100 in one year
  > 	- $100 in two years
  > 	- $1,100 in three years
  > 1. Sell these components for $1,077.12
  > 2. Pocket the difference of $77.12
  

> [!tldr] TL;DR
> $V(\sum \text{parts})>V(\text{whole})\implies \text{Stripping} \implies \text{Buy whole, Sell parts}$ 
