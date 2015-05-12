#Statistical inference
notes from the course Statistical Inference on Coursera

##Definition
Statistical Inference = from sample *guess* the properties of the population

##Kolmogorov’s Three Rules

Consider an experiment with a random outcome. Probability takes a possible outcome from an experiment and:
 0. assigns it a number between 0 and 1
 0. requires that the probability that something occurs is 1 required
 0. required that the probability of the union of any two sets of outcomes that have nothing in common (mutually exclusive)

##Derivative from the thress rules
From the Kolmogorov axioms, one can deduce other useful rules for calculating probabilities.
 0. The probability that nothing occurs is 0
 0. The probability that something occurs is 1 
 0. The probability of something is 1 minus the probability that the opposite occurs 
 0. The probability of at least one of two (or more) things that can not simultaneously occur (mutually exclusive) is the sum of their respective probabilities 
 0. For any two events the probability that at least one occurs is the sum of their probabilities minus their intersection.

## Odds
d=p/(1-p)

##Probability mass function
*a probability mass function (PMF) is a function that gives the probability that a **discrete** random variable is exactly equal to some value.*

http://en.wikipedia.org/wiki/Probability_mass_function

Valid PMF:
 0. It must always be larger than or equal to 0. 
 0. The sum of the possible values that the random variable can take has to add up to one.

## Density or PDF (probability density function)
*a probability density function (PDF), or density of a continuous random variable, is a function that describes the relative likelihood for this random variable to take on a given value. *

http://en.wikipedia.org/wiki/Probability_density_function

Areas under PDFs correspond to probabilities for that random variable.

VAlid PDF:
 0. It must be larger than or equal to zero everywhere. 
 0. The total area under it must be one.

## Cumulative distribution function (CDF) 
*Cumulative distribution function of a random variable X, returns the probability that the random variable is less than or equal to the value x.*

## Survival function
*The survival function of a random variable is defined as the probability that the random variable X is greater than the value x. *

##Diagnostic test
* The **sensitivity** is the probability that the test is positive given that the subject actually has the disease
* The **specificity**  is the probability that the test is negative given that the subject does not have the disease
* The **positive predictive value** is the probability that the subject has the disease given that the test is positive
* The **negative predictive value** is the probability that the subject does not have the disease given that the test is negative
* The **prevalence** of the disease - which is the marginal probability of disease
* The **diagnostic likelihood ratio of a positive test** , labeled DLR+ is sensitivity/(1-specificity)
* The **diagnostic likelihood ratio of a negative test** , labeled DLR- is (1-sensitivity)/specificity

##IID
*Random variables are said to be independent and identically distributed ( iid ) if they are independent and all are drawn from the same population.* The reason iid samples are so important is that they are are model for random samples. This is a default starting point for most statistical inferences.

## Sample and population mean
The sample mean estimates the population mean. The population mean is the center of mass of the population distribution, the sample mean is the center of mass of the data.

* Expected values are properties of distributions. 
* The population mean is the center of mass of population. 
* The sample mean is the center of mass of the observed data. 
* The sample mean is an estimate of the population mean
* The sample mean is unbiased => the population mean of its distribution is the mean that it’s trying to estimate. 
* The more data that goes into the sample mean, the more concentrated its density / mass function is around the population mean.

##“What does the distribution of averages look like?”.
Notably, it’s centered at the same spot as the original distribution! Thus, the distribution of the estimator (the sample mean) is centered at the distribution of what it’s estimating (the population mean). When the expected value of an estimator is what its trying to estimate, we say that the estimator is unbiased .
