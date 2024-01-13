---
tags:
  - Finance
  - CFA2/FI
---
#Refactor 
## Spot rate
### Spot rate
> [!definition] 
> **Spot rate**
> Yield to maturity on zero-coupon bond

### Discount factor
> [!definition] 
> **Discount factor**
> Price today of a $1 zero coupon bond
> 
> $$\boxed{ P_{t}= \frac{1}{(1+S_{t})^t}}$$

### Spot yield curve

> [!definition]
> **Spot yield curve**
> Graph of spot rate $S_t$ versus maturity $t$

> [!remark]-
> *Shape* and *level* of the spot yield curve change continuously:

## Forward rates

### Forward rate
> [!definition]
> **Forward rate**
> Annualised interest rate on a loan to be initiated at a future period.
> ![[Forward rate – f(j,k).excalidraw]]
> $f_{(j,k)}$ : interest rate on a $k$-period loan starting at time $j$



> [!example]-
> $f_{(3,1)}$: interest rate on a 1-year loan starting in 3 years
> ![[Forward rate – Example.excalidraw]]

### Forward curve
> [!definition]
> **Foward curve**
> Graph of forward rate $f_{(j,k)}$ vs maturity $t$.

> [!example]-
> ![[YTM with spot rates.png#invert|500]]
> 
>>[!Answer]-
>>#### Step 1: Calculate bond's price
>>| Time   | CF   | PV of CF                                             |
>>| --- | ---- | --------------------------------------------------- |
>>| 1   | 50   | $$\frac{50}{1+S_{1}}=\frac{50}{1.04}=48.08$$           |
>>| 2   | 50   | $$\frac{50}{(1+S_{2})^2}=\frac{50}{1.05^2}= 45.35$$ |
>>| 3   | 1050 | $$\frac{1050}{(1+S_{3})^3}=\frac{1050}{1.06^3}=881.60$$  |
>>|     |      |                                                     |
>>Bond value $= 48.08 + 45.35 + 881.60 = 975.03$
>>
>>#### Step 2: Solve for I/Y
>>| TVM key   | Value   |
>>| --------- | ------- |
>>| N         | 3       |
>>| PV        | -975.03 |
>>| PMT       | 50      |
>>| FV        | 1000    |
>>| CPT → I/Y | 5.933        |
>> Bond YTM = 5.933 %

## Bond expected return
$E(R) = Yield$ only when:
1. The bond is held until maturity
2. Coupons and principal are received on time
3. All coupons are reinvested at the original YTM (*least* realistic assumption)

## Forward pricing model

### Forward pricing model
> [!definition]
> **Forward pricing model** 
> Values forward contracts using *arbitrage-free* pricing. 
> Investors should be indifferent between:
> - Buying today a zero-coupon bond maturing in $j+k$ years ($P_{j+k}$)
> - Entering today a contract to buy a zero-coupon bond in $j$ years, maturing $k$ years later
>   
>  The two investments should have the same price: 
>   $$\boxed{P_{j+k}=P_jF_{(j,k)}}$$
>
> Therefore:
>   $$\boxed{F_{(j,k)} = P_{j+k}/P_j}$$

See also: [[Currency forward]]

## Forward rate model

### Forward rate model
> [!definition]
> **Forward rate model**
> If we express the [[Forward pricing model]] in terms of rates, we get the forward rate model.
>
> Investors should be indifferent between buying a:
> - longer maturity bond
> - shorter maturity bond and reinvesting the proceeds with a locked-in rate
>  $$\boxed{(1+S_{j+k})^{j+k} = (1+S_j)^j (1+f_{(j,k)})^k}$$
>
> Therefore:
> $$\boxed{f_{(j,k)}=\left (\frac{(1+S_{j+k})^{j+k}}{(1+S_j)^j}\right)^{\frac{1}{k}}-1}$$

> [!question]-
> 3-year implied forward rate
> $S_{2}=6\%$, $S_{5}=8\%$
> Calculate the 3-year **implied forward rate** for a loan starting in 2 years.
>> [!Answer]-
>> $$ 
>> \begin{flalign*}
>>f_{(2,3)} &= \left(\frac{(1+S_{5})^5}{(1+S_{2})^2}\right)^\frac{1}{3}-1 \\
>> &= \left(\frac{1.08^5}{1.06^2}\right)^\frac{1}{3}-1 \\
>> &= 9.35 \%
>> \end{flalign*}
>> $$

## Par rates
### Par rates
> [!definition]
> **Par rates**
>  For each maturity on the yield curve: *YTM* on a bond trading at *Par* (price = 100).

> [!remark]
> - If P=100 ⟶ Par rate = Coupon  rate
> - If one CF remaining ⟶ Par rate = Spot rate
> - Par rates are used to generate spot curve using [[Bootstrapping]].

## Bootstrapping spot rates

> [!definition]
> **Bootstrapping spot rates** 
> Computing spot rates one by one from par rates. 

> [!question]- 
> **Bootstrapping spot rates**
> 1-year, 2-year, and 3-year par rates are 3%, 4%, and 5%, respectively.
> Using bootstrapping, calculate $S_{1}$, $S_{2}$, and $S_{3}$.
> 
> >[!Answer]-
> >### Compute $S_1$
> >By definition:
> >$S_1=Par_{1}=3\%$ as only one coupon remains
> >
> >$Par=\frac{Coupon+Principal}{1+S_{1}}$ where:
> >- $Coupon=3$ ($Par_1=3\%$)
> >- $Par=Principal=100$
> >- Solve for $S_1$
> >
> >$\begin{align} \\
> >S_{1}&=\frac{Coupon+Principal}{Par}-1 \\
> >&=103/100-1 \\
> >&=3\% \\
> >\end{align}$
> >### Compute $S_2$
> >$Par = \frac{Coupon}{1+S_{1}}+\frac{Coupon+Principal}{(1+S_{2})^2}$ where :
> >- $S_{1}=3\%$
> >- $Coupon=4$ ($Par_{2}=4\%$)
> >- $Par=Principal=100$
> >- Solve for $S_2$
> >
> > $\begin{flalign*}
>> S_{2} &= \left(\frac{Coupon+Principal}{Par-\frac{Coupon}{1+S_{1}}}\right)^\frac{1}{2}-1 \\
> > &=\left(\frac{104}{100-\frac{4}{1.03}}\right)^{\frac{1} \\{2}}-1 \\
> > &=4.02\% \\
> > \end{flalign*}$
> > 
> > ### Compute $S_3$
> >$Par = \frac{Coupon}{1+S_{1}}+\frac{Coupon}{(1+S_{2})^2}+\frac{Coupon+Principal}{(1+S_{3})^3}$ where :
> >- $S_{1}=3\%$
> >- $S_2=4.02\%$
> >- $Coupon=5$ ($Par_{3}=5\%$)
> >- $Par=Principal=100$
> >- Solve for $S_3$
> >
> > $\begin{flalign*}
> > S_3
> > &= \left(\frac{Coupon+Principal}{Par-\frac{Coupon}{1+_{S_{1}}}-\frac{Coupon}{(1+S_{2})^2}}\right)^\frac{1}{3}-1 \\
> > &=  \left(\frac{105}{100-\frac{5}{1.03}-\frac{5}{1.0402^2}}\right)^\frac{1}{3}-1 \\
> > &= 5.069\%
> >\end{flalign*}$
> >
> >### Conclusion
> >- $S_{1}=3\%$
> >- $S_{2}=4.02\%$
> >- $S_{3}=5.069\%$

## Spot and forward relationships
An active PM will try to outperform the market by predicting how the future spot rates will differ from those predicted by the *current* forward curve.

If the future spot rates are:
- Exactly as the current forward rates, then $HPR_{bond}=r_{f}$
- Below the current forward rates, then $HPR_{bond}>r_{f}$
- Above the current forward rates, then $HPR_{bond}<r_{f}$

**Remark**: 
- $↓Rates \implies \: ↑Value$
- $↑Rates \implies \: ↓Value$

> [!example]- 1Y-HPR of zero-coupons with different maturities
> ![[HPR bond.png#invert|500]]
>
> > [!answer]-
> > ### 1-year ZCB
> > - $V_{0}=\frac{100}{1+S_{1}}=\frac{100}{1.04}=96.15$
> > - $V_{1}=100$
> >   
> > $HPR=\frac{100}{96.15}=4\%$
> > 
> > ### 2-year ZCB
> > - $V_{0}=\frac{100}{(1+S_{2})^2}=\frac{100}{1.06^2}=89.00$
> > - $V_1=\frac{100}{1+S'_{1}}=\frac{100}{1.0804}=92.56$
> >   
> > $HPR=\frac{92.56}{89.00}-1=4\%$
> > 
> > ### 3-year ZCB
> > - $V_{0}=\frac{100}{(1+S_{3})^3}=\frac{100}{1.08^3}=79.38$
> > - $V_{1}=\frac{100}{(1+S'_{2})^2}=\frac{100}{1.1006^2}=82.55$
> >   
> > $HPR=\frac{82.55}{79.38}-1=4\%$
> > 
> > ### Conclusion
> > - $HPR_{ZCB_{1}}= 4\%$
>> - $HPR_{ZCB_{2}}= 4\%$
> > - $HPR_{ZCB_{3}}= 4\%$
> > ---
> > ### Additional explanation
> > #### Implied forward rates
> > $\begin{align*} \\
> > f_{(1,1)}
> > &=\frac{(1+S_{2})^2}{1+S_{1}}-1 \\
> > &=\frac{1.06^2}{1.04}-1 \\
> > &=8.04\% \\
> > &= S'_{1} \\
> > \end{align*}$
> > 
> > $\begin{align*} \\
> > f_{(1,2)}
> > &= \left( \frac{(1+S_3)^3}{1+S_1}\right)^\frac{1}{2}-1 \\
> > &=\frac{1.08^3}{1.04}-1 \\
> > &=10.06\% \\
> > &=S'_2
> > \end{align*}$
> > 
> > #### Observation
> > Over a 1-year period, $HPR=r_{f}$ for all bonds because future spot rates evolved exactly as predicted by the forward curve.

## Rolling down the yield curve
If the yield curve is *upward*-sloping:
- Investors will purchase bonds with $Maturity > HRP$
- As time passes ($↓Maturity$), the bond's cash flows will be discounted at successively lower yield ($↓Discount \:rate$), hence the bond's price will increase ($↑PV$).
- This strategy will produce superior returns *if the yield curve remains stable* over the investment horizon.

👎 Cons
- Increases interest rate risk ($↑Maturity= \: ↑Duration$)

> [!Example]- Rolling down the yield curve
> ![[Rolling down the yield curve.png#invert]]
> > [!Answer]-
> > ### Choice 1
> > - $Holding \: period=5 \: years$
> > - $Maturity = 5 \: years$
> > - $Coupon=3\%$
> > - $YTM=3\%$ 
> > - $V_{0}=100$ (as $YTM=Coupon$)
> > - $V_{1}=103$
> >   
> >   $R=3\%$
> >   - Coupon
> >   - No capital gain ($Holding \: period=Maturity$)
> >     
> >  ### Choice 2
> > - $Holding \: period=5 \: years$
> > - $Maturity = 30 \: years$
> > - $Coupon=3\%$
> > - $YTM=6\%$ 
> > - $V_{0}=58.71$ ($<100$ as $YTM>Coupon$)
> > - $V_{5}=84.38$ (*if* the yield curve remains the same)
>>
 >> | Key       | Value  |
>>  | --------- | ------ |
 >> | N         | 5      | 
 >> | PV        | -58.71 |
 >> | PMT       | 3      |
 >> | FV        | 84.38  |
 >> | CPT → I/Y | **11.99%** | 
 >>
 >>R = 11.99%
 >>
 >>### Conclusion
 >>$R_{1}=3\%$
 >>
 >> $R_2=11.99\%$ ✅

## Z-Spread
When added to each spot rate, makes the PV of a bond's cash flows equal to the bond market price.

$$ \boxed{P=\sum{\frac{CF}{(1+S_{i}+Z)^i}}}$$
- Constant spread added to the *default-free* spot curve
- Spread over the entire spot rate curve
- Z-Spread = "*Zero-volatility* spread" (assumption of zero interest rate volatility)
- Z-Spread is **not** appropriate to value bonds with embedded options


> [!Example]- Z-Spread
> ![[Z-Spread.png#invert]]

## Shape of the yield curve
Why does the yield curve take a particular shape ?

**Traditional theories**
1. Unbiased / Pure expectations theory
2. Local expectations theory
3. Liquidity preference theory
4. Segmented markets theory
5. Preferred habitat theory

### Unbiased / Pure expectations theory
Investor's expectations determine the shape of the yield curve:
- Forward rates are solely a function of expected future spot
- LT interest rates are a  mean of future *expected* ST rates
- **Risk-neutrality**: Investors don't demand a risk premium for maturity strategies that differ from their investment horizon.
- Every maturity strategy has the same expected return

If the yield curve is:
- Upward sloping: ST rates are expected to rise
- Downward sloping: ST rates are expected to fall
- Flat: ST rates are expected to remain constant

### Local expectations theory
Similar to [[Unbiased expectations theory]] except:
- Risk-neutrality assumption only preserved over **short** holding periods.
- Over longer periods, risk premiums should exist.
- Over short time periods, every bond should earn the risk-free rate

Remark:
- Does not hold in real life as over short holding periods $R_{LT \: Bond}>R_{ST \: Bond}$ 
- This is explained by liquidity premiums and hedging concerns

### Liquidity preference theory
Forward rates reflect investors' expectations of future spot rates, plus a **liquidity premium** to compensate investors for exposure to interest rate risk.
- Liquidity preference theory = Unbiased expectations theory **+ Liquidity premium**
- Liquidity premium positively related to maturity ($↑Maturity \implies ↑Premium$)
- Forward rates are **biased** estimates of the market's expectation of future spot rates (because they include a liquidity premium)

An upward-sloping yield curve may indicate that either:
	- The market expects future interest rates to rise
	- Rates are expected to remain constant / fall, but the addition of a liquidity premium results in a positive slope
	  
A downward-sloping yield curve indicates steeply falling short-term rates.


> [! Definition] Segmented markets theory
The shape of the [[Yield curve|yield curve]] is determined by the borrowers and lenders
- Borrowers and lenders drive the balance of supply and demand for loans of different maturity
- The yield at each maturity is determined independently (*segmented*)
- Yield curve **not** determined by expected spot rates and liquidity premium

Remark:
- Pension plans and insurance companies:
	- Primarily purchase long-maturity bonds for [[Asset-liability matching|asset-liability matching]] reasons
	- Are unlikely to participate in the market for short-term funds> [! Definition]


> [!definition] Preferred habitat theory
Similar to [[Liquidity preference theory]], but liquidity premium is **not** directly related to maturity
- The imbalance between supply and demand for funds in a given maturity range (*habitat*) will induce lenders and borrowers to **shift** from their preferred habitat to one that has the **opposite imbalance**.
- To entice investors to do so, investors must be offered an **incentive** to compensate for the exposure to price / reinvestment risk in the less-than-preferred habitat:
	- Borrowers require cost savings ($↓Yield$)
	- Lenders require a yield premium ($↑Yield$)

## Yield curve shifts
### Parallel shifts
- Parallel shift = Level change
- Interest rates go up/down by the same amount across all maturities
  
  ![[Yield curve - Parallel shift.png#invert|150]]

### Nonparallel shift 
- Steepness changes
- Curvature change

## Measuring yield curve sensitivity
Measures of interest rate risk:
1. [[Effective duration]]
2. [[Key rate duration]]
3. Sensitivity to parallel, steepness, curvature movements

### Effective duration
Measures bond price risk for small ***parallel*** shifts in the [[Yield curve|yield curve]]

Problem: 
- Most yield curve shifts have nonparallel characteristics.
- Use [[Key rate duration|key rate duration]] to measure the impact of nonparallel shifts.

### Key rate duration
Quantifies bond price sensitivity to ***nonparallel*** shifts in the [[Yield curve|yield curve]]
- Key rate duration = price sensitivity to 1% change in a single **par** rate (holding other par rates constant)

### Sensitivity to parallel, steepness, curvature movements
We can decompose bond price sensitivity to several kind of movements in the yield curve:
- **Level** ($\Delta X_{L}$): parallel shift
- **Steepness** ($\Delta X_{S}$): $↑r_{LT}$ and $↓r_{ST}$
- **Curvature** ($\Delta X_{C}$): $↑r_{LT}$, $↑r_{ST}$, but $r_{inter}$ don't change

We can then model the change in value of a portfolio:
$\boxed{\Delta P/P\approx-D_{L}\Delta X_{L}-D_{S}\Delta X_{S}-D_{X}\Delta X_{C}}$

where:
- $D_{L}$: sensitivity to changes in Level
- $D_{S}$: sensitivity to changes in Steepness
- $D_{C}$: sensitivity to changes in Curvature