---
tags:
  - Finance
  - CFA2/FI
---
#Refactor 
## Credit risk measures

### Exposure at default (EAD)
> [!definition]
> **Exposure at default** (EAD)
> Total value of a loan that is exposed to when a borrower defaults (before factoring recovery)
> $$
> \bbox[15px, border: 1px solid white]{\text{EAD}_{t}=\text{PV(Remaining CF)}_{t}}
> $$
> 
> > [!example]-
> > If a borrower takes out a loan for $100,000 and two years later the amount left on the loan is $75,000, and the borrower defaults, the exposure at default is $75,000.

### Recovery rate / Loss severity
> [!definition]
> **Recovery rate**
> Extent to which principal and accrued interest on defaulted debt can be *recovered*
> 
> **Loss severity** 
> Extent to which principal and accrued interest on defaulted debt can be *lost*
>
> Therefore:   
> $$\bbox[15px, border: 1px solid white]{\text{Loss severity}=1-\text{Recovery rate}}$$
> 
> >[!example]-
> > Company A defaults on its $20m bond and is only be able to repay $12m to bondholders:
> > - 40% recovery rate
> > - 60% loss severity

### Loss given default (LGD)
> [!definition]
> **Loss given default** (LGD)
>  Estimated amount of money an investor loses when a borrower defaults on a loan.
> $$\bbox[10px, border: 1px solid white]{\text{LGD}_{t}=\text{EAD}_{t}\times \text{Loss severity}}$$

### Hazard rate (HR)
> [!definition]
> **Hazard rate** (HR)
> Exposure at default times initial probability of default.
> $$\bbox[10px, border: 1px solid white]{
\text{HR}=\text{EAD}\times\text{POD}_0
}$$

### Probability of survival (POS)
> [!definition]
> **Probability of survival** (POS)
> $$\bbox[10px, border: 1px solid white]{
\text{POS}=(1-\text{Hazard rate})^t
}$$

### Probability of default (POD)
$$\bbox[10px, border: 1px solid white]{
\text{POD}_{t}=\text{Hazard rate}\times \text{POS}_{{t-1}}
}$$

## Credit valuation adjustment (CVA)

### Expected loss
$\bbox[10px, border: 1px solid white]{\text{Expected loss}_{t}=\text{Probability of default}_{t}\times \text{Loss given default}_{t}}$

### Credit value adjustment (CVA)
$\bbox[10px, border: 1px solid white]{\text{Credit value adjustment}=PV(\text{Expected value of comparable risk-free bond}-\text{Value of risky bond})}$

or: $\bbox[10px, border: 1px solid white]{\text{CVA}=\sum \text{PV(Expected loss)}}$

> [!Question]
> A 3-year, $100 par, zero-coupon corporate bond has a:
> - hazard rate of 3% per year
> - recovery rate of 65%
> - and benchmark rate curve is flat at 4%
>
> Calculate the:
> - Expected exposure
> - Probability of survival (**PS**)
> - Probability of default (**PD**)
>  - Loss given default (**LGD**)
>  - Credit value adjustment (**CVA**)
> > [!Answer]-
> > ### Expected exposure
> > $\text{EE}_{1}=100/{1.04^2}=92.46$
> > $\text{EE}_{2}=100{1.04}=96.15$
> > $\text{EE}_{3}=100$
> > 
> > ### Probability of survival
> > $\text{Hazard rate}=3\%$
> > 
> > $\text{PS}_{1}=(1-0.03)^1=0.97^1=97\%$
> > $\text{PS}_{2}=(1-0.03)^2=0.97^2=94.09\%$
> > $\text{PS}_{3}=(1-0.03)^3=0.97^3=91.27\%$
> > 
> > ### Probability of default
> > $\text{PD}_{1}=3\%$
> > $\text{PD}_{2}=0.03\times 0.97=2.91\%$
> > $\text{PD}_{3}=0.03\times 0.9409=2.82\%$
> > 
> > ### Loss given default
> > $\text{Recovery rate}=65\%$
> > $\text{Loss severity}=1-65\%=35\%$
> > 
> > $\text{LGD}_{1}=92.46\times 0.35=32.36$
> > $\text{LGD}_{2}=96.15\times 0.35=33.65$
> > $\text{LGD}_{3}=100\times 0.35=35$
> > 
> > ### Credit value adjustment
> > #### Expected loss
> > $\text{Expected loss}_{1}=0.03\times 32.36=0.97$
> > $\text{Expected loss}_{2}=0.0291\times 33.65=0.98$
> > $\text{Expected loss}_{3}=0.0282\times 35=0.99$
> > 
> > #### PV(Expected loss)
  > > $\text{PV(Expected loss)}_{1}=\frac{0.97}{1.04}=0.93$
  > > $\text{PV(Expected loss)}_{2}=\frac{0.98}{1.04^2}=0.91$
  > > $\text{PV(Expected loss)}_{3}=\frac{0.99}{1.04^3}=0.88$
  > > 
  > > #### Credit value adjustment
  > > $\text{CVA}= \sum \text{PV(Expected loss)}=0.93+0.91+0.88=2.72$
  > > 
  > > An identical benchmark bond should trade at:
  > > $V_{\text{benchmark}}=\frac{100}{1.04^3}=88.90$
  > > 
  > > The credit risky bond should trade at:
  > > $V_{\text{risky bond}}=88.90-2.72=86.16$

## Risk-neutral probability of default
Probability of default *implied* in the current market price:
- Calculated by assuming a certain recovery rate
- Assumed recovery rate and risk-neutral probability of default are positively correlated
  
> [!Question]-
  > ![[Expected return credit risky bond.png#invert]]
  > 
  > > [!Answer]-
  > >  $\text{Recovery rate}=65\%$
  > >  
  > >  $V_{0}=86.18$
  > > ### If default in year 1
  > > $\text{Exposure}_{1}=92.46$
  > > 
  > > $\text{Recovery given default}_{1}=92.46\times 0.65=60.01$
  > > 
  > > | Key | Value |
  | --- | ----- |
  | N   |  1     |
  | **CPT → I/Y** | **-30.37%**       |
  | PV  | -86.18     |
  | PMT | 0      |
  | FV  | 60.01      |
  > >
  > > $\text{IRR}_{1}=-30.37\%$
  > > 
  > > ### If default in year 2
  > > $\text{Exposure}_{2}=96.15$
  > > 
  > > $\text{Recovery given default}_{2}=96.15\times 0.65=62.50$
  > > 
  > > | Key | Value |
  | --- | ----- |
  | N   |  2     |
  | **CPT → I/Y** | **-14.84%**      |
  | PV  | -86.18      |
  | PMT | 0      |
  | FV  | 62.50      |
  > > 
  > > $\text{IRR}_{2}=-14.84\%$
  > > 
  > > ### If default in year 3
  > > $\text{Exposure}_{3}=100$
  > > 
  > > $\text{Recovery given default}_{3}=100\times 0.65=65$
  > > 
  > > | Key | Value |
  | --- | ----- |
  | N   |  3     |
  | **CPT → I/Y** | **-8.97%**      |
  | PV  | -86.18      |
  | PMT | 0      |
  | FV  | 65      |
  > > 
  > > $\text{IRR}_{3}=-8.97\%$
  > > 
  > > ### If no default
  > > 
  > > | Key | Value |
  | --- | ----- |
  | N   |  3     |
  | **CPT → I/Y** | **5.08%**      |
  | PV  | -86.18      |
  | PMT | 0      |
  | FV  | 100      |
  > > 
  > > $\text{IRR}_{\text{no default}}=5.08\%$
  
> [!Question]-
  > ![[Relative risk analysis credit risky bond.png#invert]]
  > 
  > > [!Answer]-
  > > ### Bond DDF
  > > $\text{LGD}=104\times (1-0.45)=57.2$
  > > 
  > > $\text{Expected loss}=57.2\times 0.014=0.8$
  > > 
  > > ### Bond HJI
  > > $\text{LGD}=90\times (1-0.50)=45$
  > > 
  > > $\text{Expected loss}=45\times 0.0135=0.6$
  > > 
  > > ### Bond NDS
  > > $\text{LGD}=96\times (1-0.30)=67.2$
  > > 
  > > $\text{Expected loss}=67.2\times 0.0175=1.2$
  > > 
  > > ### Conclusion
  > > Bond NDS has the highest risk
  > > 
  > > ### Remark
  > > Absent price information, no conclusion can be reached about value

## Credit scoring and rating
**Ordinal** rankings that categorise credit quality
- They provide **no** information on the **degree** of difference in quality between rankings
  
### Credit scoring
Used for small businesses and individuals (↑Score = ↑ Credit quality)
  
### Credit ratings
Credit ratings are issued for:
- Corporate debt
- [[Asset-backed securities]] (ABS)
- Government debt
- Quasi-government debt
  
  Credit ratings:
- Provide a letter grade
- Specify outlook (positive, negative, stable)
  
### FICO score
Used in the US, the [FICO score](https://www.investopedia.com/terms/f/ficoscore.asp) factors in the:
- Age of accounts
- Delinquencies
- Utilisation of lines of credit
- Types of accounts
- Number of hard inquiries
  
### Notching
Notching in credit ratings (between several issues of the same issuer) accounts for:
- Seniority
- Loss given 

> [!Question]-
> ![[Bond price after downgrade.png#invert]]
>  
> > [!Answer]-
> > $\text{Change in spread}=0.075-0.050=0.025$
 > 
> > $\text{Change in price}=-5.89\times 0.025=-1.47\%$

## Structural models
Based on:
- Structure of a company's balance sheet
- Insights from option pricing

Shareholders have a call option on the company's assets ($A_{t}$) with the face value of debt ($K$) as the strike price.

### 👍 Strengths
- Provide an economic rationale for default ($A_{t}<K$)
- Explains why default occurs

### 👎 Weaknesses
- Company assets are not actually traded (value not directly observable)
- Assumes a simple balance sheet structure (complex balance sheets, and those with off-balance sheet liabilities would be poorly modelled)

### Value of stock  
$\bbox[10px, border: 1px solid white]{\text{Value of stock}=\text{max}(0,A_{t}-K)}$

### Value of debt
  $\begin{flalign*}
  \text{Value of debt}&=\text{Value of assets}-\text{Value of equity} \\
  &= A_{t}-\text{max}(0,A_{t}-K) \\
  &= \text{min}(A_{t},K)
  \end{flalign*}$
  
  $\bbox[10px, border: 1px solid white]{\text{Value of debt}=\text{min}(A_{t},K)}$
### Value of risky debt
  $\bbox[10px, border: 1px solid white]{\text{Value of risky debt}=\text{Value of risk-free debt}-\text{Value of a put option on company's assets}}$

### Value of debt at maturity
#### No default
  $\bbox[10px, border: 1px solid white]{\text{If} A_{t}>K \text{ (no default)} \implies\text{Value of debt at maturity}_{\text{no default}}=K}$
#### Default
$\bbox[10px, border: 1px solid white]{\text{If} A_{t}<K \text{ (default)} \implies\text{Value of debt at maturity}_{\text{default}}=A_{t}}$
  
$\bbox[10px, border: 1px solid white]{\text{Loss given default}=K-A_{t}}$
  
> [!Remark]
> $\bbox[10px, border: 1px solid white]{\text{Payoff on a put option}=X-S_{t}}$
  
$\bbox[10px, border: 1px solid white]{\text{Value of put option on assets}=\text{CVA}}$
  
> [!Remark]
> $\bbox[10px, border: 1px solid white]{\text{Credit value adjustment}=PV(\text{Expected value of comparable risk-free bond}-\text{Value of risky bond})}$
### Probability of default
  ![[Probability of default structural models.png#invert|300]]
## Reduced form models
- Treats default as **exogenous**
- Does not explain why default occurs
- Uses **default intensity** (estimated using a regression model)
- Allows linkage of default intensity, risk-free rate, and recovery rate to the state of the economy
  
### 👍 Strength
- Does not assume that company assets trade
- Default intensity is allowed to fluctuate as company fundamentals change, as well as with business cycle
  
### 👎 Weaknesses
- Does not explain why default occurs
- Treats defaults as random surprises
  
## Credit spread analysis
### Credit spread
Credit spread is:
- Compensation for default risk
- A function of default probability and recovery rate
- Calculated as the difference between the YTM of a credit-risky bond and a risk-free bond
  
Credit spreads:
- Change as expectations about the state of the economy change
- Increase as expectations of an impending recession increase
  
Formula:  
$\bbox[10px, border: 1px solid white]{\text{Credit spread}=\text{YTM}_{\text{credit-risky bond}-\text{YTM}_{\text{risk-free bond}}}}$
  
> [!Question]-
> ![[Credit spread and CVA.png#invert]]
> 
> > [!Answer]-
> > ### Value of credit-risky bond
> > | Key | Value |
  | --- | ----- |
  | N   |  4     |
  | I/Y | 3.7      |
  | **CPT → PV**  |  **97.44**     |
  | PMT | 3      |
  | FV  | 100      | 
> > $V_{\text{credit-risky bond}}=97.44$
> > 
> > ### Value of risk-free bond
> > | Key | Value |
  | --- | ----- |
  | N   |  4     |
  | I/Y | 2.5      |
  | **CPT → PV**  |  **101.88**     |
  | PMT | 3      |
  | FV  | 100      | 
>> Value if no default:
>>
>> $V_{\text{credit-risky bond}}=101.88$ 
>> 
>>### Credit value adjustment
>> $\text{CVA}=101.88-97.44=4.44$

## Binomial tree
  $\bbox[10px, border: 1px solid white]{\text{Expected exposure}_{t}=\sum(\text{Value}_{\text{Node t}}\times \text{Probability}_{\text{Node t}})+\text{Coupon}}$

> [!Question]-
  > ![[Binomial tree and bond value.png#invert]]
  > 
  > > [!Answer]-
  > > ### Value if no default
  > > #### Step 1: $\text{Node}_{t=2}$
  > > $V_{2,U}=\frac{103+103}{2\times 1.107383}=93.01$
  > > 
  > > $V_{2,M}=\frac{103+103}{2\times 1.071981}=96.08$
  > > 
  > > $V_{2,D}=\frac{103+103}{2\times 1.048250}=98.26$
  > > 
  > > #### Step 2: $\text{Node}_{t=1}$
  >>  $V_{1,U}=\frac{(93.01+3)+(96.08+3)}{2\times 1.057883}=92.21$
  >>  
  >>  $V_{1,D}=\frac{(96.08+3)+(98.26+3)}{2\times 1.038800}=96.43$
  >>  
  >>  #### Step 3: $\text{Node}_{t=0}$
  >>  Value if no default:
  >>  
  >>  $V_{0}=\frac{(92.21+3)+(96.43+3)}{2\times 1.03}=94.49$
  >>  
  >>  ### Expected exposure
  >>  $\text{Expected exposure}_{1}=0.5\times 92.21+0.5\times 96.43+3=97.32$
  >>  
  >>  $\text{Expected exposure}_{2}=0.25\times 93.01+0.5\times 96.08+0.25\times 98.26+3=98.86$
  >>  
  >>  $\text{Expected exposure}_{3}=103$
  >>  
  >>  >[!Remark]
  >>  >The following information could be used to calculate the CVA:
  >>  >- Estimated unconditional probability of default
  >>  >- Recovery rate
  
  > [!Question]-
  > ![[Changing expectations and credit spread.png#invert]]
  > 
  > > [!Answer]
  >