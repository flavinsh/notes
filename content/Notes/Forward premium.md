---
tags:
  - Finance
  - Derivatives
  - FX
aliases:
  - Forward discount
---
The **forward premium** (discount) for the *base currency* is the percentage difference between the forward price and the spot price. A forward premium (discount) occurs when the [[forward rate]] is greater (lower) than the [[sport rate]].

$$\Large{\text{Forward premium}_{A/B}=\frac{F_{A/B}}{S_{A/B}}-1}$$

> [!example]- Exemple: Calculate forward premium (discount)
>  Consider the following spot and forward exchange rates :
>  - USD/EUR spot = 1.1312
>  - USD/EUR 90-day forward = 1.320
>
>The 90-day forward premium for the EUR, in terms of USD, is:
> $$\begin{align*}
> FP_{USD/EUR}
> &=\dfrac{F_{USD/EUR}}{S_{USD/EUR}}-1\\\\
> &=\frac{1.320}{1.312}-1\\\\
> &\approx 0.61\%
> \end{align*}$$
> 
> The annualised forward premium for the EUR, in terms of USD, is:
> $$\begin{align*}
>&\approx 4 \times 0.61\%\\\\
>&\approx 2.44\%
>\end{align*}$$
>
> Because the USD/EUR forward quote is greater than the spot quote:
> - the euro (base currency) is sold at a forward premium
> - it will take more dollars to buy one euro 90 days from now
> - the euro (base currency) is expected to appreciate relative to the dollar (price currency)
> - the dollar is expected to depreciate relative to the euro
>
>> [!warning] Forward premium is for the *base* currency
>> If the forward premium is asked for the *price currency*:
>>  - First calculate the exchange rate for the other currency
> > - Then calculate the forward premium

## Interpretation

A currency selling at a forward premium (discount) is expected to appreciate (depreciate). Since the [[Forward premium]] depends on the interest differential for the currency pair: 
- the currency with the *lower* rate will always sell at a forward *premium* and is expected to appreciate
- the currency with the *higher* rate will always sell at a forward *discount* and is expected to depreciate

> [!proof]- 
> Starting with the no-arbitrage forward price:
>$$F_{A/B}=S_{A/B} \times \frac{1+r_{A}}{1+r_{B}}$$
>
> We can rewrite the above equation to show the forward rate as a percentage of the spot rate: 
> $$\frac{F_{A/B}}{S_{A/B}}=\frac{1+r_{A}}{1+r_{B}}$$
> 
> Subtracting one on each side, we obtain:
> $$\frac{F_{A/B}}{S_{A/B}}-1=\frac{1+r_{A}}{1+r_{B}}-1$$
> 
> That is:
> $${FP_{A/B}}=\frac{1+r_{A}}{1+r_{B}}-1$$
> 
> Hence:
> $$r_{A}>r_{B}\implies \frac{1+r_{A}}{1+r_{B}}>1 \implies FP_{A/B}>0$$
>
> That is the base currency (B) will trade at a forward premium if the other currency (A) has a higher interest rate.  
^c681d0

> [!tldr] TL;DR
> $r_{A}>r_{B}\implies F_{A/B}>S_{A/B} \implies \text{Forward premium}\implies\text{Base currency expected to appreciate}$

