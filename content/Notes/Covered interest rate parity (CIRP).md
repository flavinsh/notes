---
tags:
  - Finance
  - CFA2/ECO
aliases:
  - Interest rate parity
---
**Covered interest rate parity** (CIRP) states that an investment in a foreign market that is entirely hedged against exchange rate risk should give the same return as a similar investment in a domestic market. The [[No-arbitrage forward price]]:

$$\Large F_{A/B}=S_{A/B}\times\frac{1+r_{A}}{1+r_{B}}$$

> [!example]-
> If the spot rate is USD/EUR 1.10, the interest rate in the US is 5%, and the interest rate in Germany is 3%, and covered interest rate parity holds:
> 
> **No-arbitrage forward rate**
> $$\begin{align*}
F_{USD/EUR}
&=S_{USD/EUR}\times \frac{1+r_{USD}}{1+r_{EUR}}\\
&=1.10\times \frac{1.05}{1.03}\\
&= 1.12135922
\end{align*}$$
> 
>  **Option 1: Invest in local currency**
> - Start with EUR 100 
> - Invest EUR 100 at 3%
> - ==End up with EUR 103==
>
> **Option 2: Invest in foreign currency**
> - Start with EUR 100
> - Convert EUR 100 to USD 110 (spot 1.10)
> - Invest USD 110 at 5% and obtain USD 115.5 after one year
> - Convert USD 115.5 to EUR (==no-arbitrage forward 1.12135922==)
> - ==End up with EUR 103==
> 
> > [!remark] If the forward rate is correctly priced, a hedged investment will return the same as a foreign one.

Covered interest rate parity holds by arbitrage:
- if CIRP holds, no arbitrage opportunity exists (the forward rate is correctly priced)
- if CIRP does not hold, an [[Arbitrage opportunity]] exists (the forward rate is mispriced)

> [!example]- Example: Cash and carry arbitrage when forward is *overpriced*
>  If the spot rate is USD/EUR 1.10, the interest rate in the US is 5%, and the interest rate in Germany is 3%, and the ==quoted 1-year forward rate is USD/EUR 1.15==
>  
>  The quoted forward rate (1.15) is not equal to the no-arbitrage forward rate (1.12135922), so:
>  - CIRP does not hold
>  - an arbitrage opportunity exists
>  
>  Since the ==quoted forward== rate $F_{USD/EUR}$ is ==overpriced==, sell EUR (base currency) forward:
>  - borrow USD 1 at 5\%
>  - sell USD 1 and simultaneously buy EUR 0.90909091 (spot USD/EUR 1.10)
>  - invest EUR 0.90909091 at 3\% for one year and obtain EUR 0.93636364
>  - ==sell EUR== 0.93636364 and simultaneously buy EUR 1.07681819 (quoted ==forward== USD/EUR 1.15)
>  - repay loan of USD 1.05
>  - pocket the difference of USD 0.02681819 in one year (USD 26,818 per million dollar borrowed)
>
> > [!remark] All transactions occurs at $t_{0}$, no initial investment, riskless profit made in 1 year

> [!example]- Example: Cash and carry arbitrage when forward is *underpriced*
>  If the spot rate is USD/EUR 1.10, the interest rate in the US is 5%, and the interest rate in Germany is 3%, and the ==quoted 1-year forward rate is USD/EUR 1.05==
>  
>  The quoted forward rate (1.05) is not equal to the no-arbitrage forward rate (1.12135922), so:
>  - CIRP does not hold
>  - an arbitrage opportunity exists
>  
>  Since the ==quoted forward== rate $F_{USD/EUR}$ is ==underpriced==, buy EUR (base currency) forward:
>  - borrow EUR 1 at 3\%
>  - sell EUR 1 and simultaneously buy USD 1.10 (spot USD/EUR 1.10)
>  - invest USD 1.10 at 3\% for one year and obtain USD 1.133
>  - sell USD 1.133 and simultaneously ==buy EUR== 1.07904762 (quoted ==forward== USD/EUR 1.05)
>  - repay loan of EUR 1.03
>  - pocket the difference of EUR 0.04904762 in one year (EUR 49,048 per million euro borrowed)
>
> > [!remark] All transactions occurs at $t_{0}$, no initial investment, riskless profit made in 1 year

