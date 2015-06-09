####Note
Personal notes, not meant to be accurate or understood by others

##R<sup>2</sup>

 * **R<sup>2</sup>** is the percentage of the total variability that is explained by the linear relationship with the predictor
 * 0≤R<sup>2</sup>≤1
 * R<sup>2</sup> is the sample correlation squared
 * R<sup>2</sup> can be a misleading summary of model fit.
 * Deleting data can inflate it.
 * Adding terms to a regression model always increases R2.


## Confidence and Prediction Intervals
 * Both intervals have varying widths.
 * Least width at the mean of the Xs.
 * We are quite confident in the regression line, so that interval is very narrow.
 * If we knew β0 and β1 confidence interval would have zero width.
 * The prediction interval must incorporate the variability in the data around the line.
 * Even if we knew β0 and β1 prediction interval would still have width.

## Summary notes on linear models
* Linear models are the single most important applied statistical and machine
learning technique, *by far*.
* Some amazing things that you can accomplish with linear models
  * Decompose a signal into its harmonics.
  * Flexibly fit complicated functions.
  * Fit factor variables as predictors.
  * Uncover complex multivariate relationships with the response.
  * Build accurate prediction models.

## Multiple variable regression
```r
data(swiss)
lm(formula = Fertility ~ ., data = swiss)
```
```
Residuals:
     Min       1Q   Median       3Q      Max 
-15.2743  -5.2617   0.5032   4.1198  15.3213 

Coefficients:
                 Estimate Std. Error t value Pr(>|t|)    
(Intercept)      66.91518   10.70604   6.250 1.91e-07 ***
Agriculture      -0.17211    0.07030  -2.448  0.01873 *  
Examination      -0.25801    0.25388  -1.016  0.31546    
Education        -0.87094    0.18303  -4.758 2.43e-05 ***
Catholic          0.10412    0.03526   2.953  0.00519 ** 
Infant.Mortality  1.07705    0.38172   2.822  0.00734 ** 
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 7.165 on 41 degrees of freedom
Multiple R-squared:  0.7067,	Adjusted R-squared:  0.671 
F-statistic: 19.76 on 5 and 41 DF,  p-value: 5.594e-10
```
The Estimates are the coeffients of the independent variables of the linear model (all of which are percentages) and they reflect an estimated change in the dependent variable (fertility) when the corresponding independent variable changes. So, for every 1% increase in percent of males involved in agriculture as an occupation we expect a .17 decrease in fertility, holding all the other variables constant; for every 1% increase in  Catholicism, we expect a .10 increase in fertility, holding all other variables constant.

## Summary of dummy variables
* If we treat a variable as a factor, R includes an intercept and omits the alphabetically first level of the factor.
  * The intercept is the estimated mean for the reference level.
  * The intercept t-test tests for whether or not the mean for the reference level is 0.
  * All other t-tests are for comparisons of the other levels versus the reference level.
  * Other group means are obtained the intercept plus their coefficient.
* If we omit an intercept, then it includes terms for all levels of the factor.
  * Group means are now the coefficients.
  * Tests are tests of whether the groups are different than zero.
* If we want comparisons between two levels, neither of which is the reference level, we could refit the model with one of them as the reference level. `relevel(InsectSprays$spray, "C")`
