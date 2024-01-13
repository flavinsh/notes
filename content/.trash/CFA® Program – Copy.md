---
Tags: CFA, MOC, Favourite 
Aliases: CFA Program
---
%%
Up:: [[Home]]
Same::
Down:: [[CFA® Level 1]], [[CFA® Level 2]], [[CFA® Level 3]]
%%

## Levels
1. [[CFA® Level 1]]
2. [[CFA® Level 2]]
3. [[CFA® Level 3]]
   
## Topics
- [[Quantitative Methods]]               
- [[Economics]]                          
- [[Financial Statements Analysis]]     
- [[Equity Investments ]]                
- [[Fixed Income]]                      
- [[Corporate Issuers ]]            
- [[Derivatives]]                        
- [[Alternative Investments]]            
- [[Portfolio Management]]              
- [[Ethical and Professional Standards]] 

## Weights
...

## Courses
```dataview
TABLE Level, Topic, Client
FROM #CFA1 OR #CFA2 OR #CFA3 AND -#MOC AND -#Topic AND #Cours
SORT file.name DESC
```

## Recent
```dataview
TABLE Level, Topic, Subject
FROM #CFA1 OR #CFA2 OR #CFA3 AND -#MOC AND -#Topic AND -#TopFinance
SORT file.mtime DESC
LIMIT 10
```
## All
```dataview
TABLE Level, Topic, Subject
FROM #CFA1 OR #CFA2 OR #CFA3 AND -#MOC AND -#Topic
SORT file.name ASC
```