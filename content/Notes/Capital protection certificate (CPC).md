#Finance 

Structured product that offers:
- Minimum cash settlement at maturity guaranteed (**Capital protection**)
- A portion of underlying's upside (**Participation**) 

![[Capital protection certificate - Chart.png#invert|400]]

Usually, the lower the **↓capital protection**, the higher the **↑participation**.

## CPC without a cap
> [!example]
> - Underlying = ABB stock
> - Initial fixing level = CHF 80
> - Denomination = CHF 1000
> - Capital protection = 80% (CHF 800)
> - Strike level = 80% (CHF 64)
> - Participation = 60%
>
> ---
>
> :TiCircleNumber1: If the underlying is **down at maturity**:
> - Final fixing level = CHF 40 (–50%)
> - Cash settlement = CHF 800 (–20%)
>
> > The performance is better with the certificate thanks to its capital protection feature: capital will not go below a threshold (80% of the initial amount). 
> 
> 
> :TiCircleNumber2: If the underlying is **up at maturity**:
> - Final fixing level = CHF 140 (+75%)
> - Cash settlement = $1000 \times (0.8+0.6 \times (\frac{140-64}{80}))$ = CHF 1370 (+37%)
>   
>  > The performance is limited (+37% vs +75%) due to the participation rate (60%).
>   
>   - 100-64 = CHF 76 → upside above the strike
>   - 76/80 = 0.95 → compared to the initial fixing level
>   - 0.6 x 0.95 = 0.57 → after factoring in the participation rate
>   - 0.80 + 0.57 = 1.37 → cash settlement (+37%)

## CPC with a cap
> [!example]
> - Final fixing level = CHF 140 (+75%)
> - Cap level = 150%  / CHF 120
>   
>  :TiCircleNumber3: If the underlying is **above the cap at maturity**:
>  - Cash settlement = $1000 \times(0.8 + 0.6 \times (1.5-0.8))$ = CHF 1220 (+22%)
>    
>  > The performance is even more limited with a cap (+22% vs +37% vs +75%).  
>    
> - 1.5 – 0.8 = 0.7 → maximum performance until the cap (+70%)
> - 0.7 x 0.6 = 0.42 → after factoring in the participation rate (+42%)
> - 0.42 + 0.80 = 1.22 → cash settlement (+22%)

---

###### Links
- [Voltylab](https://www.voltylab.com/capital-protection.php#top-ancora)
- [Six](https://www.six-structured-products.com/en/know-how/product-know-how/capital-protection-products/capital-protection-with-participation)