---
level:
  - "[[CFA Level 2]]"
topic: "[[Fixed Income]]"
---
## Arbitrage-free 
Method to value securities such that no market participant can earn an arbitrage (riskless) profit.

- **Arbitrage-free** = consistent with market price of other securities:
- Upholds [[Value additivity (arbitrage)]] principle (no stripping / reconstruction)
- Does not allow for [[Dominance (arbitrage)]] (no cheaper identical asset)

> [!Question]
> ![[Arbitrage value additivity.png#invert]]
> 
> > [!Answer]-
> > $V_{Bond}=\frac{4.5}{1.01}+\frac{4.5}{1.0125^2}+\frac{104.5}{1.015^3}=108.78$
> > 
> > If $P_{Bond}>108.78$ : 
> > - Buy separate components
> > - **Reconstitute** the bond
> > - Sell the bond
> >   
> >   If $P_{Bond}<108.78$:
> >   - Buy the bond
> >   - **Strip** it into components
> >   - Sell the components separately

## Binomial interest rate model
System for building interest rate trees:
 - Start = **current** 1-period spot rate
 - Assumes **equal** probability of upward / downward interest rate movements
 - Node = future 1-period **expected** spot rate (up / down)
 - Relationship among the set of rates is a function the **assumed volatility** (can be based on historical data or implied from interest rate derivatives)

Arbitrage-free pricing:
1. Create tree
2. **Calibrate** arbitrage-free interest rates
		- Interest rate tree should generate values for on-the-run benchmark securities equal to market prices
		- Ho Lee model: **lognormal distribution**

> [!NOTE]
> For the exam, just know how to **use** the tree (no need to create it from scratch). 

## Backward induction methodology
Value a bond by moving backward from last period to time zero.

Assumptions:
- $V_{Maturity}$ is known
- $V_{Node}$ = average PV of two possible values from next period
- Discount rate is the rate for that node

> [!Question]
> ![[Backward induction.png#invert]]
> 
> > [!Answer]-
> >$V_{1,U}=\frac{107+107}{2\times1.08}=99.07$
> >
> >$V_{1,D}=\frac{107+107}{2\times1.05}=101.90$
> >
> >$V_{0}=\frac{(99.07+7)+(101.90+7)}{2\times1.03}=104.35$
> >
> >### Conclusion
> >$V_{Bond}=104.35$

> [!Question]
> ![[Bond valuation using spot rates.png#invert]]
> 
> > [!Answer]-
> > $V_{Bond}=\frac{7}{1.03}+\frac{107}{1.0473^2}=104.35$
> > ### Remark
> > Valuation would be the same for an option-free bond.

### Pathwise valuation
Mathematically identical approach to binomial model:
- Rates come from binomial modle
- $2^{n-1}$ paths for $n$ periods
- Each cashflow is discounted at appropriate 1-period spot / forward rate
- Based on equal weight for each path

> [!Question]
> ![[Pathwise valuation.png#invert]]
> 
> > [!Answer]-
> > ### Number of paths
> > $n=2$
> > 
> >$N_{paths}=2^{n-1}=2$
> >
> > ### Value
> > $V_{Path\:1}=\frac{7}{1.03}+\frac{107}{1.03\times 1.08}=102.98$
> > 
> > $V_{Path\:2}=\frac{7}{1.03}+\frac{107}{1.03\times 1.05}=105.73$
> > 
> > $V_{0}= \frac{102.98+105.32}{2}=104.35$

## Monte Carlo method
Generates random interest rate paths bases on a probability distribution and assumed volatility:
- Uses pathwise valuation
- May impose upper / lower bounds consistent with mean reversion of rates
- Paths are calibrated to ensure [[Arbitrage-Free Valuation Framework|arbitrage-free]] valuation of benchmark securities
- Useful valuation of securities whose value is path dependent (e.g. MBS)

## Interest rate models
1. Equilibrium term structure models
	- Vasicek model (single-factor model)
	- Cox-Ingersoll-Ross (CIR) model (single factor model)
1. Arbitrage-free models
	- Ho-Lee model
	- Kalotay-Killiams-Fabozzi (KWF) model
2. Other models
	- Gauss+

### Vasicek model 1977
Suggests that interest rates are **mean reverting** to a long-run value

$\boxed{dr=a(b-r)dt+\sigma dz}$
- The $a(b-r)dt$ (deterministic) forces the interest rate to mean-revert toward the long-run value $b$, at a speed determined by $a$.
- $dr$: change in short term interest rates
- $b$: long-run mean reverting level
- $r$: current rate
- $a$: mean reversion parameter
- $\sigma dz$: random walk movement (stochastic)

Remarks:
- Volatility does not increase as the level of interest rates increase
- Interest rates could become negative

### Cox-Ingersoll-Ross (CIR) model 1985
$\boxed{dr=a(b-r)dt+\sigma \sqrt{r}dz}$
- $a(b-r)dt$: deterministic term (same as the [[Vasicek model]])
- $\sigma \sqrt{ r }dz$: stochastic term (improvement over the [[Vasicek model]])

Remarks:
- Volatility related to the current level of the interest rates (prevents negative interest rates)

### Ho-Lee model 1986
$\boxed{dr_{t}=\theta_{t}dt+\sigma dz_{t}}$
- $\theta_{t}$: time-dependent drift term
- Calibrated by using market prices to find the $\theta_{t}$ that generates the current term structure
- Model can be used to price zero-coupon bonds and determine the spot curve
- Produces a normal distribution of rates

### Kalotay-Williams-Fabozzi (KWF) model
$\boxed{d\ln(r_{t})=\theta_{t}dt+\sigma dz_{t}}$
- Assumes that the short rate has a **lognormal** distribution
- Right hand side is the same as the [[Ho-Lee model]]
- Still assumes constant volatility and drift

---

###### Navigate
````col
```col-md
flexGrow=1
===
> [! prev]
> [[Term structure and interest rate dynamics]]

```
```col-md
flexGrow=1
===
> [! next]
> [[Valuation and Analysis of Bonds with Embedded Options]]

```
````

###### See also
```dataview
Table Topic, Level
FROM #CFA2 AND #FI AND -#MOC AND -#TOPIC AND -#TopFinance
```
