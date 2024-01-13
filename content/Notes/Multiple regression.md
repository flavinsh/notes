---
tags:
  - Maths
  - Statistics
  - CFA2/QM
---
#WIP

> [!info] Objectives
> - Test the effectiveness of [[Multiple linear regression]] models
> - Effects of [[Heteroskedasticity]] on regression results
> - Effects of [[Serial correlation]]
> - Effects of [[Multicolinearity]]
> - Use of logistic regression models

## Basics of multiple regression and underlying assumptions

**Definition**
- [[Multiple linear regression]] models explain the variation in a dependent variable using more than independent variables
- Allow for consideration of multiple underlying influences

**Uses**
1. Identify relationships between variables
2. Forecast variables
3. Test existing theories

### Multiple regression Basics

The general multiple linear regression model is:
$$\boxed{Y_{i}=\sum^{n}_{i=1}{b_{k}X_{ki}}+\varepsilon_{i}}$$

The multiple regression methodology estimates:
- the **intercept** and 
- **slope coefficients** 
- such that the **sum of the squared error terms** is **minimised**
$$
\boxed{\sum^{n}_{i=1} \varepsilon_{i}^2}
$$

- The result of the process is the following **regression equation**:
$$\boxed{\hat{Y_{i}}=\sum^{n}_{i=1}{\hat{b_{k}}X_{ki}}}$$

- The **residual** is the difference between the:
	- observed value
	- predicted value
$$
\boxed{\hat{\varepsilon_{i}}=Y_{i}-\hat{Y_{i}}}
$$
$$\boxed{\hat{\varepsilon_{i}}=Y_{i}-\sum^{n}_{i=1}{\hat{b_{k}}X_{ki}}}$$
![[Multiple regression model.png#invert|300]]

### Formulating the multiple regression equation
> [!Example] Example: Formulating the regression equation
> Hypothesis that the future 10-year real earnings growth in the S&P 500 (EG10) can be explained by the trailing dividend payout ratio (PR) and yield curve slope (YCS)
>
>
$\text{EG10}=b_{0}+b_{1}\text{PR}+b_{2}\text{YCS}+\varepsilon$
>
> where:
>  - $\text{EG10}=\text{real earnings growth in the S\&P 500}$
>  - $\text{PR}=\text{Trailing dividend payout ratio}$
> - $\text{YCS}=\text{Yield curve slope}=\Delta \text{YTM}_{\text{10-year T-Bond vs 3-month T-Bill}}$
>   
>   ![[Coefficient and standard error estimates for regression of EG10 on PR and YCS.png#invert|300]]


### Interpreting the multiple regression results

- The **intercept term** is the value of the dependent variable when the independent variables are all equal to zero
- Each **partial slope coefficient** is the estimated change in the variable for a 1-unit change in that independent variable, holding other independent variable constant.

> [!Example] Example: Interpreting multiple regression results
> - **Intercept term** ($b_{0}$): If the dividend payout ratio and the slope of the yield curve are zero, we would expect the subsequent 10-year real earnings growth rate to be –11.6%
> 
> - **PR partial slope coefficient** ($b_{1}$): If the payout ratio increase by 1%, we would expect the subsequent 10-year earnings growth rate to increase by 0.25%, holding YCS constant
>
> - **YCS partial slope coefficient** ($b_{2}$): If the yield curve slope increases by 1%, we would expect the subsequent 10-year earnings growth rate to increase by 0.14%, holding PR constant

✅ **Assumptions** underlying a multiple regression model:
1. A linear relationship exists between the dependent / independent variables
2. Normally distributed residuals
3. Constant variance of the error terms
4. No correlation between residuals
5. Not random independent variables
6. No exact linear relation between any two independent variables

**Residual plots** allow analysts to get a preliminary indication of violation of regression assumptions. 

❌ **Violations** of assumptions of multiple regression model include:
- Non-constant variance
- Correlation between residuals
- Random independent variables
- Exact linear relation between two independent variables

> [!Example] Interpret residual plots
> **Office rent model**: Hypothesis that the monthly rate per square feet for office properties in a large city in the US can be explained by the:
> - age of the property
> - distance from the nearest metro station
> - number of lunch locations within walking distance
>
> ![[Multiple regression - Office rent example.png#invert|450]]
>
> **Regression output** (191 observations)
> 
> ![[Multiple regression - Office rent model regression output.png#invert|250]]
> 
> **Residuals vs Predicted values**
> 
> ![[Multiple regression - Office rent model - Exhibit 1.png#invert|350]]
> - The plot does not indicate a systematic pattern or directional relationship between the predicted value
> - The dependent variable and the model residuals as indicated by the horizontal lines centered on 0.
> 	- ✅ residuals are independent of the predicted dependent variable
> 	- ✅  residuals have a constant variance
> 	- ✅  residuals are uncorrelated with each other
> 
> **Residuals vs Independent variables**
> 
> ![[Multiple regression - Office rent model - Exhibit 2.png#invert|350]]
> - The plots do not indicate a directional relationship between the residuals and any of the independent variable
> - The residuals are scattered around the horizontal line 0 across different different values of the independent variables
> 	- ✅ Residuals are unrelated to the independent variables
> 
> **Normal Q-Q plot of residuals**
> 
> ![[Multiple regression - Office rent model - Exhibit 3.png#invert|350]]
> - For a standard normal distribution, only 5% of the observations should be beyond –1.65 standard deviations of 0
> - We see that a few observations are beyond –2 standard deviations, with one outlier beyond –3 standard deviations
> - It appears that there are a higher-than-expected number of observations beyond +2 standard deviations
> - It also shows [[Skewness|skewness]] in the right tail (positive skewness)
> 	- The observations are skewed above the line of theoretical distribution the distribution.
> 	- The distribution of the residuals deviates from a normal distribution as it has fatter tails and right skewness

## Evaluation regression model fit and interpreting model results
### ANOVA Tables
### Coefficient of determination (R²)
#### Adjusted R²
### Predicting the dependent variable

## Model specification
### Model specification
### Examples of misspecification of functional form
#### Misspecification 1 — Omitting a variable
#### Misspecification 2 — Variable should be transformed
#### Misspecification 3 — Inappropriate scaling of the variable
#### Misspecification 4 — Incorrectly pooling data
### Violations of regression assumptions
### Heteroskedasticity
#### Effects on regression analysis
#### Detecting
#### Correcting
### Serial correlation (Autocorrelation)
#### Effects on model parameters
#### Effects on standard errors
#### Detecting
#### Correcting
### Multicolinearity
#### Effects on model parameters
#### Effects on standard errors
#### Detecting
#### Correcting

## Extension of model regression
### Detecting influential datapoints
### Interpreting the coefficients in a dummy variable regression

