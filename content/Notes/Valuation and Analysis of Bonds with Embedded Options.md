---
tags:
  - Finance
  - CFA2/FI
---
## Valuing embedded options

### Embedded calls
Investors get a **discount** equal to call value

$\boxed{V_{\text{call}}=V_{\text{straight}}-V_{\text{callable}}}$
- Embedded calls are in favour of issuers
- Investors should get a discount to compensate

### Embedded puts
Investors pay a **premium** equal to put value

$\boxed{V_{\text{put}}=V_{\text{putable}}-V_{\text{straight}}}$
- Embedded puts are in favour of investors
- Investors should be willing to pay a premium for the feature

### Volatility and embedded options
- Straight bond values are **not** affected by volatility
- Embedded options **are** affecter by volatility

$\boxed{\text{If}↑\text{Rate volatility} \text{, then }↓V_{\text{callable}} \text{ and} ↑V_{\text{putable}}}$

Remark:
- Embedded calls benefit issuers (negative for  investors)
- Embedded puts benefit investors

### Level and shape of yield curve
Upside / Downside:
- Upside on a callable bond is limited (when rates decline)
- Downside on a putable bond is limited (when rates increase)

Yield curve changes:
- When the yield curve **steepens**:
	- a call option has low value (unlikely to be exercised)
	- a put option is valuable
	<br><br>
- When the yield curve **flattens**:
	- a call option becomes more valuable
	- a put option loses value (unlikely to be exercised)

### Valuation of bonds with options
Use [[Backward induction|backward induction]] process in a binomial tree:
1. At each node, evaluate whether the option will be exercised
2. If so, use the exercise value ($X$)
3. If not, use the calculated value (normal backward induction)

Value of a **callable** bond at any node is the **lowest** of:
- Average PV of two possible values from next period
- Call price

$\boxed{V_{\text{callable}}=\text{min(average PV, call price)}}$

Value of a **putable** bond at any node is the **highest** of:
- average PV of two possible values from next period
- Put price

$\boxed{V_{\text{putable}}=\text{max(average PV, put price)}}$

> [!question]- 
> **Backward Induction**
> 
> ![[Backward induction callable bond.png#invert|400]]
> 
> 1. Value straight bond
> 1. Value callable bond
> 1. Value embedded call 
>  
> > [!Answer]-
> > ### Straight bond value
> >$V_{1,U}=\frac{107+107}{2\times1.08}=99.07$
> >
> >$V_{1,D}=\frac{107+107}{2\times1.05}=101.90$
> >
> >$V_{\text{straight}}=\frac{(99.07+7)+(101.90+7)}{2\times1.03}=104.35$
> >
> >### Callable bond value
> >$X_{t\geq1}=100$
> >
> >$V_{1,U}=99.07$ (unchanged)
> >
> >$V_{1,D}=100$ (~~101.90~~)
> >
> >$V_{\text{callable}}=\frac{(99.07+7)+107}{2\times1.03}=103.43$ 
> >
> >#### Remark
> >
> >$V_{\text{callable}}<V_{\text{straight}}$
> >
> > ### Embedded call value
> > $\begin{flalign*} V_{text{call}}&=V_{Straight}-V_{Callable}\\
&=104.35-103.43 \\ 
&=0.92 \end{flalign*}$


> [!Question]
> ![[Backward induction putable bond.png#invert]]
> 1. Value straight bond
> 1. Value putable bond
> 1. Value embedded put 
> 
> Note: Use data from [[Backward induction callable bond.png|this example]]
> > [!Answer]-
> > ## Straight bond value
> >$V_{1,U}=\frac{107+107}{2\times1.08}=99.07$
> >
> >$V_{1,D}=\frac{107+107}{2\times1.05}=101.90$
> >
> >$V_{straight}=\frac{(99.07+7)+(101.90+7)}{2\times1.03}=104.35$
> >
> >## Putable bond value
> >$X_{t\geq1}=100$
> >
> >$V_{1,U}=99.07$ (unchanged)
> >
> >$V_{1,D}=100$ (~~101.90~~)
> >
> >$V_{\text{putable}}=\frac{107+(101.90+7)}{2\times1.03}=104.81$ 
> >
> >#### Remark
> >
> >$V_{\text{putable}}>V_{\text{straight}}$
> >
> > ## Embedded put value
> > $\begin{flalign*} V_{\text{put}}&=V_{\text{putable}}-V_{ \text{straight}}\\
&=104.81-104.35 \\ 
&=0.46 \end{flalign*}$

## Option-adjusted spread (OAS)
Constant interest rate spread added to all rates in binomial tree so that $P_{\text{model}}=P_{\text{market}}$
- The spread is accounting for option risk
- A better name would be **option-removed spread**
### Remarks
- Interest rate trees do not produce arbitrage-free values for credit risky bonds with embedded options (the tree is incorrectly calibrated)
- Spot and expected future spots are derived from credit risk-free bonds (treasuries)
- Corporate bonds exhibit credit risk

> [!Question]
> **OAS**
> ![[OAS callable bond.png#invert]]
> 
> Note: Use data from [[Backward induction callable bond.png|this example]]
> 
> > [!Answer]-
> > ### Callable bond using backward induction
> > $V_{\text{callable}}=102.71$
> > 
> > $V_{1,U}=98.62$
> > 
> > $V_{1,D}=101.42$ → 100
> > 
> > ### Callable bond using OAS
> >Using $\text{OAS}=50 \text{bps}=0.005$:
> >
> >$V_{1,U}=\frac{1}{2}\left(\frac{107}{1.085}+\frac{107}{1.085}\right)=98.62$
> >
> >$V_{1,D}=\frac{1}{2}\left(\frac{107}{1.055}+\frac{107}{1.055}\right)=101.42$ → 100
> >
> >$V_{\text{callable}}=\frac{1}{2}\left(\frac{98.62+7}{1.035}+\frac{107}{1.035}\right)=102.71$
> > 
> > ### Conclusion
> > We obtain the same value, so $OAS=50bps$

### OAS and volatility
The assumed level of volatility in a binomial interest rate tree affects the value of underlying options:

$\boxed{↑\text{Volatility} \implies ↑\text{Call}}$

$\boxed{↑\text{Volatility} \implies ↑\text{Put}}$


> [!info] 
> Keeping the market *price* of the bond *constant*:
> - $↑Volatility \implies ↓ OAS_{callable}$ (callable less attractive)
> - $↑Volatility \implies ↑ OAS_{putable}$ (putable more attractive)

## Effective Durations
$\boxed{\text{Duration}_{\text{callable or putable}}\leq \text{Duration}_{\text{straight}}}$

$\boxed{\text{Duration}_{\text{zero-coupon}}\approx \text{Maturity}}$

$\boxed{\text{Duration}_{\text{fixed-rate}}<\text{Maturity}}$

$\boxed{\text{Duration}_{\text{floater}}\approx \text{Time to next reset}}$

## One-sided durations
Impact of yield changes on price of bonds with embedded options is **asymmetric**:
- **Callable** bonds will have **lower** one-sided **down-duration** than one-sided up-duration ($↓↓r\implies ↑Callable$)
- **Putable** bonds will have **higher** one-sided **down-duration** than one-sided up-duration ($↓r\implies ↑↑Putable$)

## Key rate duration
Price impact of **par rate** changes for specific maturities
- Applicable for nonparallel shifts in yield curve
- Captures **shaping risk**

Option-free bond's maturity-matched rate is the most important (highest key rate duration)

**Callable** bond with option deep **out of the money** (low coupon rate, high market rate) will have **highest key rate durations** corresponding to their **maturity**

**Putable bond** with option deep **out of the money** (high coupon rate, low market rate) will have highest key rate durations corresponding to their **maturity**

As the option **moves into money**, the **time-to-exercise rate** becomes more important: key rate duration corresponding to the time-to-exercise will be highest

## Effective convexity
Convexity is positive for **straight** bonds and **putable** bonds:

$\boxed{\text{Convexity}_{\text{straight}}>0}$

$\boxed{\text{Convexity}_{\text{putable}}>0}$

Convexity is **negative** for **callable** bonds, when the call  is near the money:
- Price appreciation is limited due to the short call
- *"Price compression"*

$\boxed{\text{Convexity}_{\text{callable}}<0\text{ when call is near the money}}$

## Convertible bond
Bond convertible into fixed number of shares:
- Investors effectively hold a straight bond, plus a call on stock
- Limits downside (vs stock): if stock price is low, convertible is still worth something as a bond

$\boxed{\text{Convertible bond}=\text{Straight bond}+\text{Call on stock}}$


> [!NOTE] 
> Conversion option is **not** interest-rate sensitive

### Convertible bond valuation
#### Conversion ratio
$\boxed{\text{Conversion ratio}=\text{Number of shares per bond}}$

#### Initial conversion price
$\boxed{\text{Initial conversion price}=\frac{\text{Issue price}}{\text{Conversion ratio}}}$

#### Market conversion price
$\boxed{\text{Market conversion price}=\frac{\text{Effective price per share}}{\text{Conversion ratio}}}$

#### Conversion value
$\boxed{\text{Conversion value}=\text{Market price of stock after conversion}\times \text{Conversion ratio}}$

#### Straight value
$\boxed{\text{Straight value}=\text{PV of Cash flows if not convertible}}$

#### Minimum value of a convertible bond
$\boxed{{\text{Minimum value}}=\text{max}(\text{Conversion value},\text{Straight value})}$

#### Market conversion premium
$\boxed{\text{Market conversion premium}=\text{Market conversion price}-\text{Market price of stock}}$

#### Maket conversion premium ratio
$\boxed{\text{Maket conversion premium ratio}=\frac{\text{Maket conversion premium}}{\text{Market price}}}$

#### Premium over straight value
$\boxed{\text{Premium over straight value}=\frac{\text{Market value}}{\text{Straight value}}-1}$

> [!Question]
> ![[Convertible bond.png#invert]]
> 
> > [!Answer]-
> > ### Minimum value
> > $\text{Conversion value}=29\times30=870$
> > 
> > $\text{Straight value}=910$
> > 
> > $\text{Minimum value}=910$
> > 
> > ### Market conversion price
> > $\text{Market conversion price}=960/30=32$
> > ### Market conversion premium
> > $\text{Market conversion premium}=32-29=3$
> > 
> > ### Market conversion premium ratio
> > $\text{Market conversion premium ratio}=\frac{3}{29}=10.3 \%$
> > 
> > ou
> > 
> > $\text{Market conversion premium ratio}=\frac{32}{29}-1=10.3 \%$
> > 
> > ### Premium over straight value
> > $\text{Premium over straight value}=\frac{960}{910}-1=5.5 \%$

## Callable convertible bond
$\boxed{\text{Callable convertible bond}=\text{Straight bond}+\text{Call on stock}-\text{Call on bond}}$

## Stocks vs Convertible bond
Convertible bonds limit stock downside risk:
$\boxed{↓\text{Stock price}\implies \text{Convertible outperforms stock}}$

Conversion premium lower returns:
$\boxed{↑\text{Stock price}\implies \text{Stock outperforms convertible}}$

Convertible pay coupons:
$\boxed{\text{Flats stock price} \implies \text{Convertible outperforms stock}}$ 







