---
tags:
  - Finance
  - Derivatives
  - CFA1/ECO
  - CFA1/DER
  - CFA2/DER
---
The **no-arbitrage forward price** is the [[Forward price]] that makes the [[Value of a forward contract]] at inception equal zero. At this price, the forward contract is correctly priced and no [[Arbitrage opportunity]] is possible.
$$\Large{F_{0}=[S_{0}-PV_{\text{Benefits}}+PV_{\text{Costs}}]\times(1+r_{f})^t}$$

or:
$$\Large{F_{0}=[S_{0}\times(1+r_{f})^t]-FV_{\text{Benefits}}+FV_{\text{Costs}}}$$

## Zero-coupon bond forward

$$\Large{F_{0}=S_{0}}(1+r_{f})^t$$
## Coupon-paying bond forward

$$\Large{F_{0}=(S_{0}-PVC)\times(1+r_{f})^t}$$
or:

$$\Large{F_{0}=S_{0}\times(1+r_{f})^t-FVC}$$

## Equity forward with discrete dividends

$$\Large{F_{0}=(S_{0}-PVD)\times(1+r_{f})^t}$$
or:

$$\Large{F_{0}=S_{0}\times(1+r_{f})^t-FVD}$$

## Equity index forward with continuous dividends

$$\Large{F_{0}=S_{0}\times e^{(r_{f}-\delta)t}}$$


## Forward rate agreement
## Swap

The [[Swap fixed rate (SFR)|swap fixed rate]] is given by:

$$\Large{SFR_{periodic}=\frac{{1-DF_{n}}}{\sum DF}}$$
and:

$$\Large{SFR_{annual}}=SFR_{periodic}\times N$$
where $N$ is the number of settlements per year.