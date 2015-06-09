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

### Summary of dummy variables
* If we treat a variable as a factor, R includes an intercept and omits the alphabetically first level of the factor.
  * The intercept is the estimated mean for the reference level.
  * The intercept t-test tests for whether or not the mean for the reference level is 0.
  * All other t-tests are for comparisons of the other levels versus the reference level.
  * Other group means are obtained the intercept plus their coefficient.
* If we omit an intercept, then it includes terms for all levels of the factor.
  * Group means are now the coefficients.
  * Tests are tests of whether the groups are different than zero.
* If we want comparisons between two levels, neither of which is the reference level, we could refit the model with one of them as the reference level. `relevel(InsectSprays$spray, "C")`
