---
tags:
  - Finance
  - Derivatives
  - CFA1/DER
  - CFA2/DER
  - CFA3/DER
---
A **credit default swap** (CDS) is a derivative contract which allows to transfer credit risk.

To hedge against credit risk, a bond investor may take a long CDS position.

In exchange of periodic fees, CDS reduce credit risk exposure.

>[!tldr] TL;DR
>CDS = Insurance against default

### How it works

![[Credit Default Swaps.png#invert|300]]

**Protection buyer** buys credit protection from the protection seller and pays CDS spread for coverage (similar to payments on an insurance policy)
- Short credit risk
- Obligated to make CDS spread payments
  
**Protection seller** agrees to make a payment if a default occurs (value + interest)
- Long credit risk
- Obligated to make a payment if a credit event occurs

> [! info]
> Standardisation in CDS markets makes: 
> 
> $\boxed{\text{CDS coupon}\neq \text{CDS spread}}$
> 
> Hence an **upfront payment** is made by one of the counterparties to the CDS (upfront premium)


### Uses
CDS can be used for:
1. Speculation
2. Hedging
3. Arbitrage

### Types
#### Single-name CDS 
- CDS on a single specific borrower.
- Payoff on a single-name CDS is based on the **cheapest-to-deliver** (CTD) obligation with the same seniority

#### Index CDS
- CDS on an equally weighted combination of borrowers
- **Credit correlation** is an important factor in pricing of index CDS

![[Index CDS.png#invert|400]]

### CDS Spread
The **price** of a CDS is referred to as its **spread**, expressed in basis points:

> [!Example]
> A company CDS has a spread of 300bps means that to insure \$100 of this company's debt, an investor has to pay $3 per year.

CDS spread is determined by:
1. Probability of default
2. Conditional probability of default (Hazard rate)
3. Loss given default

> [! Remark]
> 
$\boxed{↑\text{Risk} \implies ↑ \text{CDS spread}}$ but $\boxed{↑\text{CDS spread}\implies \text{↑Risk (debt or economy)}}$
> 
> Thus, CDS provide insights into:
>- Company default risk
>- Country risk

#### Probability of default
Likelihood of default in any given year by the reference entity

#### Conditional probability of default (Hazard rate)
Probability of default given that no prior default has occurred

#### Loss given default
Expected amount of loss in the event a default occurs

$\boxed{\text{Expected loss}_{t}=\text{Hazard rate}_{t}\times \text{Loss given default}_{t}}$

### Upfront payment

#### Upfront payment
$\boxed{\text{Upfront payment}_{\text{from protection buyer}}=\text{PV(Protection leg)}-\text{PV(Premium leg)}}$

- $\text{Protection leg}=\text{Expected cash flows paid by protection seller upon default}$
- $\text{Premium leg}=\text{Expected coupon payments made by protection buyer}$

#### Upfront premium %
$\boxed{\text{Upfront premium \%}_{\text{from protection buyer}}\approx(\text{CDS spread}-\text{CDS coupon}) \times \text{Duration}}$

#### Price of CDS
$\boxed{\text{Price of CDS}\approx 100-\text{Upfront premium \%}}$

### Profit on CDS ater inception
$\boxed{\text{Profit}_{\text{for protection buyer}}\approx \Delta \text{Spread} \times \text{Duration} \times \text{Notional principal}}$

> [! Definition]
> **Monetising** the gains / losses of a CDS exposure:
> - Capture the gains on an existing in-the-money CDS
> - Capture the losses on an existing out-of-money CDS
> - Can be done by undertaking an offsetting transaction

