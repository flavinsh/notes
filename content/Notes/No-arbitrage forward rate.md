---
tags:
  - Finance
  - Derivatives
  - FX
---
The **no-arbitrage forward rate** is the [[forward exchange rate]] that makes the initial value of a [[currency forward]] equal zero. In these conditions, the forward rate is correctly priced, [[Covered interest rate parity (CIRP)|covered interest rate parity]] holds and no [[arbitrage opportunity]] exists.

$$\Large{F_{A/B}=S_{A/B} \times \frac{1+r_{A}}{1+r_{B}}}$$

> [!example]- Example: Calculate no-arbitrage forward rate
>  If the spot rate is USD/EUR 1.10, the interest rate in the US is 5\%, and the interest rate in Germany is 3\%, the forward price for a 6-month forward rate is:
>
> $$\begin{align*}
F_{USD/EUR}
&=S_{USD/EUR} \times \frac{1+r_{USD}\cdot t}{1+r_{EUR}\cdot t}\\\\
&=1.10 \times \frac{1+0.05 \times 0.5}{1+1.03\times 0.5}\\\\
&=1.10 \times \frac{1.025}{1.015}\\\\
&=1.10 \times 1.00985222\\\\
&\approx1.1108
\end{align*}$$
>
> The 6-month forward premium for the euro (base) is:
> 
> $$\begin{align*}
FP_{USD/EUR} 
&=\frac{F_{USD/EUR}}{S_{USD/EUR}}-1\\\\
&\approx \frac{1.1108}{1.10}-1\\\\
&\approx 0.98\%
\end{align*}$$
>
> The annualised forward premium for the euro (base) is: 
> $$\begin{align*}
&\approx2 \times 0.98\% \\\\
&\approx 1.96\%
\end{align*}$$
>
> Interpretation:
> - The forward quote for the euro (base) is greater than the spot
> - The euro (base) is selling at a forward premium
> - The exchange rate is expected to increase
> - It will take more dollars to buy one euro
> - The euro is expected to appreciate against the dollar

The [[Forward premium]] depends on the interest differential for the currency pair: 
- the currency with the *lower* rate will always sell at a forward premium
- conversely, the currency with the *higher* rate will sell at a forward discount

![[Forward premium#^c681d0|proof]]

