Hypothesis Testing - Means
========================================================
author: Math 145
date: 
autosize: false
width:1920

Means
===
* This process will be very similar to hypothesis testing with proportions

An Improvement: The t-distribution
===
* We made an assumption: that $\sigma$ and $s$ were the same.
* If we use $s$, we can get better results by using a distribution which allows for variation in the standard deviation due to sampling variation
* The t-distribution requires "degrees of freedom"
    * This is given by 
* The t-statistic is given by almost the same formula as z:
$$t = \frac{\bar{x}-\mu}{s/\sqrt{n}}$$
(z would be the same formula but with $\sigma$ instead of $s$)
* How do the z and t distrbutions differ?
    * Using R for t values
* If we use the t-distribution instead of the normal (z) distribution, how do we change our formula for confidence intervals?

Example
===
* US traffic police often use radar to catch drivers speeding. To alert them to the presence of police radar,
some drivers mount radar detectors in their cars. This has led to a debate: Are radar detectors a useful
reminder to stay within the speed limit, or are they simply a way of avoiding police detection?

* How can we set this question up as a hypothesis test? What is $H_0$? What is $H_A$?

The Study
===
* A study in Maryland found that a sample of 22 cars with radar detectors slowed down an average of 11
mph in the presence of radar. Suppose that the speed reduction of individual cars was normally distributed
with standard deviation 2 mph.

<small>
www.afn.org/nafn09444/scanlaws/
</small>

* How can we use this data to help us answer the question?
    * Construct a 95% CI for the drop in speeds among all cars
    * What does this tell us?
    
* How is this different when using a t vs z setup?

Sampel size
===
What sample size would be needed to have a ME of 0.5 mph? (Keeping a 95% CI)

Returning to the malaria drug
===
Before the drug trial, the average length
of time before a child in the population got malaria was 89 days with standard deviation 41 days.
During the experiment, 724 children were treated with the drug and their average length of time until
infection of was 97.5 days.

How can we frame our hypothesis tests?

This can be framed as whether the change from 89 to 97.5 days is a *statistically significant* change at the $\alpha=0.05$ level.

* $H_0$?
* $H_A$?
