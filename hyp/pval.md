P Values and t-tests
========================================================
author: Math 145
date: 
autosize: false
width:1920

CIs
===
* So far, we have framed hypothesis tests through the lens of confidence intervals
* There is a mirror way to answer the same questions

Gas Mileage
===
A gasoline additive claims to increase the average mileage of a certain type of car from the usual 24 miles per gallon. A store owner wants to test this claim, and if there is convincing evidence that the mean is greater than 24, he will stock this additive. He finds that the mean mileage of a sample of 45 cars using the additive is 24.7 miles per gallon with standard deviation of 2.3 miles per gallon. Using a significance level of 0.05, decide whether the store should the store stock this additive.

* 1-tail (1-sided) vs 2-tail (2-sided tests)
* Software vs table

Hypothesis Testing
===
* Always testing against the null hypothesis

![hyptest](nullhypothesis.png)

The p-value
===
incremental:true
* What does this p-value really tell us?
  * Assuming the null hypothesis is true, what is the probability of getting the result we got or more extreme
  * The meaning of *extreme* depends on whether we do a 1-sided or 2-sided test

Errors
===
* We are always taking a chance of making an error. What is the $\alpha$-level telling us?
* Type I error is incorrectly rejecting a true null hypothesis (a "false positive")
* Type II error is failing to reject a false null hypothesis (a "false negative")
* What would this look like in our examples?

===

![errors](type1type2.jpg)

Statistical Significance vs Practical Significance
===
* Practical Significance
  * even if the increase in scores is statistically significant, it may not be of practical significance.
  * e.g. What does a gain of 25 points *mean*?

T-test in software
===
* R has a t.test() command

Types of t-tests
===
* We did a one-sample t-test, compared it to a hypothetical mean
* We might want to compare two values to each other
  * These can be *paired* or not paired
  * Called a paired t-test or a 2-sample t-test

  
1 vs 2 Samples
===
* When testing a hypothesis, we ask whether the sample mean is significantly different from some
particular value—for example, if coached students had significantly higher SAT scores than the average.
* But how do we know that the coached students are like the rest of the population? Indeed, the
fact that they signed up for coaching suggests that they may be different.
* In practice, we often study a control group and compare two samples

Matched Pairs or Paired data
===
* Food on/off campus
    * http://theithacan.org/news/food-prices-found-higher-at-college-retail-than-off-campus-locations
* pre-test vs post-test
* Need two measures for each case
* Sample size of two groups must be identical

Matched pairs: On vs off campus food
===
* What would the data frame look like?
* PPSS?
* Hypotheses?
* df?
* $t^*$?
* $t$?

Assumptions
===

Assumption for t-test matched pairs:
* Random variable in original population is normally distributed, so the difference is normal

Usefulness
===
Matched pairs are useful because:

* Comparative studies enable us to avoid the avoid effects of confounding variables
  * For example: choosing to get coaching with an increase in SAT scores—the students who chose coaching may have been more likely to see an increase in scores anyway)
* Can be used even when randomization is not possible

Without matched pairs
===

* Suppose we want to compare the means of two groups, but:
    * No paring of individuals (not matched pairs)
    * Samples can be different sizes
* We will assume that
    * We want to compare means of two groups
    * Each group is a sample from a different population
    * Responses in each group are independent of those from other group

What does a 2-sample t-test do?
===
<center>
* ![mrttest.jpg](mrttest.jpg)
</center>


<!--
## Example: Booking Flights
* https://hbr.org/2016/04/women-book-business-travel-earlier-saving-companies-millions
* How do you think this study was done?
-->

Notation
===

\           | Mean            | SD        | Size
------------|-----------------|-----------|-----
Population 1| $\mu_1$         | $\sigma_1$|
Population 2| $\mu_2$         | $\sigma_2$|
Sample 1    | $\bar{x}_1$     | $s_1$     | $n_1$
Sample 2    | $\bar{x}_2$     | $s_2$     | $n_2$

Assumptions
===
Assumption for Two Sample Test:

* The two samples must be independent.

Two-samples
===
Are the following two schools comparable in SAT scores?

School 1: A random sample of 43 students has mean SAT of 502, and standard deviation of 60

School 2: A random sample of 35 students has mean SAT of 480, and standard deviation of 50

What are we trying to estimate? PPSS?

Standard error for two-sample t-test
===

* Remember: $Var(\bar{x}_1) = \frac{s_1^2}{n_1}$

* So $SE_{\bar{x}_1-\bar{x}_2} = \sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}$

Performing the test
===
* Do we use a $z$ or a $t$?
* Degrees of freedom:
    * By hand: min($n_1-1,n_2-1$)
    * Computer: $\dfrac{\left( \dfrac{s_1^2}{n_1} + \dfrac{s_2^2}{n_2} \right)^2}{\dfrac{1}{n_1-1} \left( \dfrac{s_1^2}{n_1} \right)^2 + \dfrac{1}{n_2-1} \left( \dfrac{s_2^2}{n_2} \right)^2}$

Is there a difference?
===
Are the following two schools comparable in SAT scores?

School 1: A random sample of 43 students has mean SAT of 502, and standard deviation of 60

School 2: A random sample of 35 students has mean SAT of 480, and standard deviation of 50

Confidence interval for two sample means
===
If we know $\sigma$:
$(\bar{x}_1-\bar{x}_2-z \cdot \sigma_{\bar{x}_1-\bar{x}_2},\ \bar{x}_1-\bar{x}_2+z \cdot \sigma_{\bar{x}_1-\bar{x}_2})$

If we don't know $\sigma$:
$(\bar{x}_1-\bar{x}_2-t \cdot SE_{\bar{x}_1-\bar{x}_2},\ \bar{x}_1-\bar{x}_2+t \cdot SE_{\bar{x}_1-\bar{x}_2})$

where\ 
$SE_{\bar{x}_1-\bar{x}_2}=\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}$ \ and\ 
$\sigma_{\bar{x}_1-\bar{x}_2}=\sqrt{\frac{\sigma_1^2}{n_1}+\frac{\sigma_2^2}{n_2}}$

Code
===
Can also use t.test() for 2-sample t-test
