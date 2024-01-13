---
tags:
  - Finance
  - FX
  - CFA2/ECO
---
## Definition
Implied cross rate = combination of two currency pairs to get a third one

## Usage
Given dealer quotes for three currency pairs, compute implied cross rates and compare it to the corresponding dealer quote to check if there is discrepancy. If there is, a [[Triangular arbitrage|triangular arbitrage]] profit is possible.

### Without bid-ask spread
$\boxed{\text{If Implied cross-rate}>\text{Dealer cross rate}\implies \text{Buy dealer / Sell implied}}$

$\boxed{\text{If Implied cross-rate}<\text{Dealer cross rate}\implies \text{Buy implied / Sell dealer}}$

$\boxed{\text{If Implied cross-rate}=\text{Dealer cross rate}\implies \text{No arbitrage opportunity}}$

### With bid-ask spread
$\boxed{\text{If Implied cross-rate}_{bid}<\text{Dealer cross rate}_{ask}\implies \text{Buy implied / Sell dealer}}$

$\boxed{\text{If Implied cross-rate}_{bid}>\text{Dealer cross rate}_{ask}\implies \text{Buy dealer / Sell implied}}$

> [! Remark] Dealer always makes a profit
> - Buy high (ask)
> - Sell low (bid)

## Questions

> [!Question] Implied cross rate with bid-ask spread
> Assume that the bid-offers in a certain interbank for USD/EUR are 1.3850/1.3851, and JPY/USD is 75.66/75.68. The market-implied bid-offer on the JPY/EUR cross rate is _closest_ to:
> 
> > [!Answer]-
> > ### Compute bid and ask
> >  - $\begin{flalign*}
> > \text{JPY/EUR}_{bid} 
> > &=\text{JPY/USD}_{bid} \times \text{USD/EUR}_{bid} \\
> > &= 75.66 \times 1.3850 \\
> > &= 104.7891 \\
> > \end{flalign*}$
> >
> > - $\begin{flalign*}
> > \text{JPY/EUR}_{ask} 
> > &=\text{JPY/USD}_{ask} \times \text{USD/EUR}_{ask} \\
> > &= 75.68 \times 1.3851 \\
> > &= 104.824368 \\
> > &\approx 104.8244
> > \end{flalign*}$
> >
> > ### Conclusion
> > Implied cross-rate is:
> > 
> > $\text{JPY/EUR } 104.7891/104.8244$
> > 
> > ---
> >  #### Source
> >  [Analyst Prep](https://analystprep.com/study-notes/cfa-level-2/the-triangular-arbitrage-opportunity/)

> [!Question] Implied cross rate with inversion
> Assume that the USD/GBP is 1.5846/1.5848, and the USD/EUR is 1.3850/1.3851. Calculate the implied GBP/EUR cross rate.
> 
> > [!Answer]-
> > $\boxed{\text{GBP/EUR} = \text{GBP/USD} \times \text{USD/EUR}}$
> > 
> > ### Invert to get missing quote
> > First, we need to compute $\text{GBP/USD}$ by inverting $\text{USD/GBP}$.
> > - $\text{GBP/USD}_{bid}=\frac{1}{\text{GBP/USD}_{ask}}=\frac{1}{1.5848}=0.63099445 \approx 0.6310$
> > - $\text{GBP/USD}_{ask}=\frac{1}{\text{GBP/USD}_{bid}}=\frac{1}{1.5846}=0.67358211 \approx 0.6736$
> >   
> >  ### Compute bid and asks
> >  Then we can compute implied bid and ask :
> >  - $\begin{flalign*}
> >    \text{GBP/EUR}_{bid}
> >     &=\text{GBP/USD}_{bid} \times \text{USD/EUR}_{bid} \\
> >     &= 0.6310 \times 1.3850 \\
> >     & \approx 0.8739
> >    \end{flalign*}$
> >  - $\begin{flalign*}
> >    \text{GBP/EUR}_{ask}
> >     &=\text{GBP/USD}_{ask} \times \text{USD/EUR}_{ask} \\
> >     &= 0.6736 \times 1.3851 \\
> >     & \approx 0.9330
> >    \end{flalign*}$
> >    
> >  ### Conclusion
> >  Implied cross rate is:
> >    
> >   $\text{GBP/EUR } 0.8739–0.9330$
> >   
> > ---
> >  #### Source
> >  [Analyst Prep](https://analystprep.com/study-notes/cfa-level-2/the-triangular-arbitrage-opportunity/)


> [!Question] Triangular arbitrage
> 
> ![[FX arbitrage (Kaplan).png#invert|300]]
> 
>> [!Answer]-
>>  ### Implied cross rate
>> 
>> $\boxed{\text{CHF/GBP} = \text{CHF/USD} \times \text{USD/GBP}}$
>> 
>>- $\begin{flalign*}
>>\text{CHF/GBP}_{Bid} &= \text{CHF/USD}_{Bid} \times \text{USD/GBP}_{Bid} \\
>> &= 1.25 \times 1.8 \\
>> &= 2.25
>> \end{flalign*}$
>> 
>> - $\begin{flalign*}
>> \text{CHF/GBP}_{Ask} &= \text{CHF/USD}_{Ask} \times \text{USD/GBP}_{Ask} \\
>> &= 1.251 \times 1.8010 \\
>> &= 2.253051 \\
>> \end{flalign*}$
>>
>> - $\text{CHF/GBP } 2.25-2.253051$
>> 
>>### Quoted rate 
>>- $\text{CHF/GBP } 2.3 – 2.301$
>> 
>>### Conclusion  
>>- **Sell GBP** at 2.301 (overvalued), Buy CHF
>>- Buy USD at 1.25, Sell CHF 
>>- Buy GBP at 1.8, Sell USD
>>  
>> ---
>>  #### Source
>>  Kaplan-Schweser

> [!Question] Triangular arbitrage
> Consider the following spot rates in an interbank market:
>
> Currency | Quotation
> -|:-:
> SEK/USD|$6.7738-6.7740$
> JPY/USD|$80.86-80.88$
> CAD/USD|$0.9543-0.9545$
> USD/EUR|$1.35458-1.3560$
>
> Assume that an inexperienced dealer quotes a bid-offer rate of JPY/CAD as $84.63-84.70$. Identify and implement a triangular arbitrage.
> 
> > [!Answer]-
> >  In order to identify a potential triangular arbitrage opportunity, we need to compare $\text{JPY/CAD}_{Dealer}$ with $\text{JPY/CAD}_{Implied}$
> > 
> > ### Compute implied cross rate
> > $\boxed{\text{JPY/CAD}=\text{JPY/USD} \times \text{USD/CAD}}$
> > 
> > - $\begin{flalign*}
> >   \text{JPY/CAD}_{Bid}
> >   &=\text{JPY/USD}_{Bid} \times \text{USD/CAD}_{Bid} \\
> >   &=\text{JPY/USD}_{Bid}  \div \text{CAD/USD}_{ \color{red}Ask} \\
> >   &= 80.86 \div 0.9545 \\
> >   &= 84.71451021 \\
> >   &\approx 84.71
> >   \end{flalign*}$
> >  
> > - $\begin{flalign*}
> >   \text{JPY/CAD}_{Ask}
> >   &=\text{JPY/USD}_{Ask} \times \text{USD/CAD}_{Ask} \\
> >   &=\text{JPY/USD}_{Ask}  \div \text{CAD/USD}_{ \color{red}Bid} \\
> >   &= 80.88 \div 0.9543 \\
> >   &= 84.75322226 \\
> >   &\approx 84.75
> >   \end{flalign*}$
> >   
> >  ### Compare implied cross rate with dealer cross rates
> >    
| JPY/CAD | Bid                                 | Ask                               |
| ------- | ----------------------------------- | --------------------------------- |
|         | Sell CAD                            | Buy CAD                           |
| Implied | 84.71 $\color{red}\text{Sell high}$ | 84.75                             |
| Dealer  | 84.63                               | 84.70 $\color{red}\text{Buy low}$ |
> >
> > ### Implement the trade
> >  
> >  | Step                             | Buy        | Sell       |
| -------------------------------- | ---------- | ---------- |
| Buy CAD from the dealer          | ~~1 CAD~~~     | 84.70 JPY |~~~
| Sell CAD in the interbank market | 84.71 JPY | ~~1 CAD~~     |
> > > [!note]- Details
> > >  **Sell CAD in the interbank market**
> > >  
> > > $\boxed{\text{JPY/CAD}_{Bid}=\text{JPY/USD}_{Bid} \times \text{USD/CAD}_{Bid}}$
> > > 
> > > 1. Short $\text{Dealer USD/CAD}_{Bid}=\frac{1}{\text{CAD/USD}_{Ask}}=\frac{1}{0.9545}=1.04766894$
> > > 	- ~~Buy 1.04766894 USD~~
> > > 	- Sell 1 CAD
> > > 1. Short $\text{Dealer JPY/USD}_{Bid}= 80.86$
> > > 	- ~~Sell 1.04766894 USD~~
> > > 	- Buy 84.71 JPY (80.86 JPY/USD x 1.04766894 USD)
> > > 
> > ### Net profit
> > - 0.01 JPY per CAD
> > - 10,000 JPY per  1 million CAD
> >
> > ---
> > #### Source
> > [Analyst Prep](https://analystprep.com/study-notes/cfa-level-2/the-triangular-arbitrage-opportunity/)

> [!question] Triangular arbitrage
> The following are spot rates quoted in the interbank market:  
>
| Currency pair | Bid – Ask       |
| ------------- | :---------------: |
| USD/GBP       | 1.5462 – 1.5467 |
| JPY/USD       | 89.34 – 89.36   |
| JPY/GBP       | 139.02 – 139.10   |
>
> An analyst suspects that the JPY/GBP exchange rate is mispriced. After calculating the no arbitrage rate the analyst would most likely:
> 
> **A.** Conclude that the exchange rate is not mispriced.  
> **B.** Conclude that there is a mispricing and exploit it by selling GBP and buying JPY.  
> **C.** Conclude that there is a mispricing and exploit it by selling JPY and buying GBP.
> 
> > [!Answer]-
> > In order to check if JPY/GBP is mispriced, we need to compare $\text{Dealer JPY/GBP}$ with $\text{Implied JPY/GBP}$.
> >    
> >  ### Compute implied cross rate
> >  - $\begin{flalign*}
> >  \text{JPY/GBP}_{Bid} 
> >  &= \text{JPY/USD}_{Bid} \times \text{USD/GBP}_{Bid} \\
> >  &= 89.34 \times 1.5462 \\
> >  &= 138.137508
> >  \end{flalign*}$
> >  
> > - $\begin{flalign*}
> >  \text{JPY/GBP}_{Ask} 
> >  &= \text{JPY/USD}_{Ask} \times \text{USD/GBP}_{Ask} \\
> >  &= 89.36 \times 1.5467 \\
> >  &= 138.213112
> >  \end{flalign*}$
> > 
> > ### Compare implied cross rate with dealer quote
> > 
> >
| JPY/GBP | Bid                                  | Ask        |
| ------- | ------------------------------------ | ---------- |
|         | Sell GBP                             | Buy GBP    |
| Implied | 138.137508                           | 138.213112 $\color{red}\text{Buy low}$ |
| Market  | 139.02 $\color{red}\text{Sell high}$ | 139.10     |
>>
>> ### Implementation of the trade
>> - Buy GBP in the market using implied rate (lower ask of 138.213112)
>> 	- **Buy 1 GBP** / ~~Sell 1.5462 USD~~
>> 	- ~~Buy 1.5462 USD~~ / Sell 138.168432 JPY (1.5462 x 89.36)
>> - Sell GBP to the market (higher bid of 139.02)
>> 	- **Sell 1 GBP** / Buy 139.02 JPY
>> - Make a profit of 0.806888 JPY per GBP
>>   
>>  ### Answer
>>  **B.** Conclude that there is a mispricing and exploit it by selling GBP and buying JPY.  
>>  ---
>>  #### Source
>>  [300Hours](https://300hours.com/f/cfa/level-2/t/fx-rates-which-direction-to-gain-arbitrage/)


---
## Links
- [Bid-ask spreads in the FX market – Investopedia](https://www.investopedia.com/articles/forex/090914/understanding-spread-retail-currency-exchange-rates.asp)
- [Bid-ask spread – Analyst Prep](https://analystprep.com/study-notes/cfa-level-2/the-bid-offer-spread/)
- [Triangular arbitrage – Analyst Prep](https://analystprep.com/study-notes/cfa-level-2/the-triangular-arbitrage-opportunity/)

