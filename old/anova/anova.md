Comparing multiple groups with numerical variables: ANOVA
========================================================
author: Math 145

What is ANOVA?
===
ANOVA stands for “Analysis of Variance”, but in spite of its name, it tests whether the means of several populations are equal.

We’ll start with examples where there are only two samples (which we could have done with a Z or T test) and then go on and use the method when there are three or more samples.

Examples
===

In which of the following examples do the two samples appear to have come from populations with
the same mean and which look like they came from populations with different means?

***

Example 1

Sample 1 | 8 | 9 | 11 | 12
---------|---|---|----|----
Sample 2 | 18|19 | 21 | 22

Example 2

Sample 1 | 8 | 9 | 11 | 12
---------|---|---|----|----
Sample 2 |8.1|9.1|11.1|12.1


Example 3

Sample 1 | 8 | 9 | 11 | 12
---------|---|---|----|----
Sample 2 |18 | 19|121 | 122

Graphing the values
===
![](1.png)

What are we looking at to answer the question?

General idea
===
* If the difference between the sample means is *small* compared with the variation within the
samples, then the means of the populations could be the same.
* If the difference between the sample means is *large* compared with the variation within the
samples, then the means of the populations are not likely to be the same.

The samples are often called *groups*.

Test statistic
===
incremental:true

$$F = \dfrac{Average \ between \ group \ variation}{Average \ within \ group \ variation}$$

What would our null hypothesis be? What types of values for $F$ would cause us to reject $H_0$?

The F-statistic has the F-distribution which has two degrees of freedom, one determined by the
numerator and one by the denominator. The calculations to find F are messy, so we will mostly look at them on the computer.

The F Test
===
Null hypothesis: The means of all the populations are equal.

Alternative hypothesis: The means of all the populations are not all equal. Thus at least one population has a different mean, but ANOVA does not tell us which. (We have to look back at the data.)

This is exactly like the chi-squared test, when if we rejected the null hypothesis, we knew there
was an interaction, but we didn’t know what it was.

Sample ANOVA output
===
Example 1
![](2.png)

Sample ANOVA output
===
Example 2
![](3.png)

Example 3?
===
incremental:true
What would you expect?

$p = 0.09029$

Degrees of freedom
===
incremental:true
Between groups DF (DFG): # groups -1

Within groups DF (DFE): N - # groups

Total DF: N - 1

Notice: Total DF = Between groups DF + Within groups DF

We need to report both degrees of freedom: F(Between groups DF, Within groups DF)

This is why we don't use a table for the F distribution!

An example F calculation
===
(this will be long)

Sum of squares (SS)
===
Between groups: Sums of squares of deviation of group mean from the overall mean, weighted by the
size of group:

$$SSG = \sum_{all \ groups} n_i (\bar{x}_i-\bar{x})^2$$

Within groups: Sums of squares of deviations of individual observations from the group (sample) mean, summed across groups. Often called *error*, so if $x_{ij}$ is a typical element in Group $i$
$$SSE = \sum_{groups} \sum_{group \ i} (x_{ij}-\bar{x}_i)^2$$
$$SST = \sum_{all \ observations, \ all \ groups} (x_{ij}-\bar{x})^2$$

Note Total SS (SST) = Between group SS + Within group SS

Mean squares (MS)
===
Between Groups: Mean between group variation

$$MSG = \dfrac{SSG}{DFG}$$

Within Groups: Mean within group variation, or error

$$MSE = \dfrac{SSE}{DFE}$$

Finally, F
===
$$F = \dfrac{MSG}{MSE}$$

Using $F(DFG,DFE)$, or $F(k-1,N-k)$

Fill in the blank
===
![](4.png)

Assumptions
===
For the F-statistic to have the F-distribution, we have to assume:
* Each sample comes from a normal population
* The population standard deviations are all equal

Note: The means of the normal distributions do not need to all be equal — that’s what we are testing

Fortunately, the F-Test is not very sensitive to unequal standard deviations:
* We can use the F-Test if the largest sample standard deviation is less than twice the smallest one.
* In other words, the largest variance should be no more than 4 times the smallest one

Example
===
The “fog index” measures the difficulty in a passage or writing. A sample of passages
from three magazines gave the following results.

Magazine            | S1    | S2    | S3    |S4    | S5   | S6
--------------------|-------|-------|-------|------|------|------
Scientific American | 15.75 | 11.55 | 11.16 | 9.92 | 9.23 | 8.20
Newsweek            | 10.21 | 9.66  | 7.67  | 5.12 | 4.88 | 3.12
Sports Illustrated  | 9.17  | 8.44  | 6.10  | 5.78 | 5.58 | 5.36

<small>From Shruptine and McVicar, reported by Wilde and Seber in *Chance Encounters*.The fog index is defined by Fog index = 0.4 * Average # words per sentence + % words with > 3 syllables.</small>

Is there a significant difference in fog indices between these magazines?
===
incremental:true

Write down hypotheses. We'll use $\alpha=0.05$

![](5.png)

Does the data meet the conditions for the F-Test?

How do we tell which magazine(s) have different fog indices?
===
incremental:true

How could we analyze?

Pairwise t-tests


Does the type of cooking pot affect the iron content of food?
===
Iron deficiency leads to anemia. In developing countries, iron has traditionally got into the food from iron cooking pots. But as heavy iron pots are replaced by lighter, cheaper aluminum pots, there is a concern that anemia and malnutrition may result. Use the data to decide if there is a significant relationship between type of pot and iron content in food.

![](6.png)

<small>A. A. Adish, “Effect of consumption of food cooked in iron pots on iron status and
growth of young children: a randomized trial”, *The Lancet* (1999)</small>

F-test
===
![](7.png)

Conditions met? Hypothesis test?

Combining groups
===
If we combine clay and aluminum, does the food cooked in iron pots have significantly higher
iron content?
![](8.png)

Results
===
![](9.png)

Does bread loose vitamins when it is stored?
===
![](10.png)

<small>H. Park et al “Fortifying bread with each of three antioxidants, *Cereal Chemistry*
(1997)</small>

Results
===
![](11.png)
