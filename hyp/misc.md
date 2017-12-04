Miscellaneous Tests
========================================================
author: Math 145
autosize: true
width:1920

Proportion Test
===




Analogous to t-test, but for proportions

```r
tally(~Lot.Shape, data=ames)
```

```
Lot.Shape
 IR1  IR2  IR3  Reg 
 979   76   16 1859 
```

***


```r
prop.test(~Lot.Shape, p=.25, data=ames)
```

```

	1-sample proportions test with continuity correction

data:  ames$Lot.Shape  [with success = IR1]
X-squared = 110.15, df = 1, p-value < 2.2e-16
alternative hypothesis: true p is not equal to 0.25
95 percent confidence interval:
 0.3171093 0.3515888
sample estimates:
        p 
0.3341297 
```

Chi-square test: Multiple categorical variables
===

ABC Poll of 1500 adults, 750 men, 750 women on Presidential approval rating

On March 10, 2002, 623 men, 607 women approved of Bush’s handling of job. Was there a gender gap in the approval ratings significant at the 5% level?

On Sept 9, 2001, 443 men out of 750 and 390 women out of 750 approved of Bush’s handling of
job. Is there a gender gap in the approval ratings significant at the 5% level?

Looking at counts
===
Create two-way tables for the data in the previous two problems

Create *joint* and *conditional* probability tables

Which conditional probability table is more interesting to us right now?

An Expected Count Table
===
* What would you expect if there were no relationship between the two variables? Use the same total count in each grouping.

* $Expected \ cell \ count = \dfrac{Row \ total \times Column \ total}{n}$

Difference tables
===
* Now we make a table of differences, with Observed - Expected
* What differences do you see between the tables of differences that may indicate significance?
* What do you notice about the sums of the differences in one table? How many values are needed to
determine all the others?
* *We say the table has one degree of freedom.*

INFERENCE FOR TWO-WAY TABLES: CHI SQUARE TEST FOR INDEPENDENCE
===

Null hypothesis: There is no association between variables.

*This means the columns have same % breakdown. In addition, the rows have same % break down.*

Alternative hypothesis: There is an association between the variables, but we do not specify what.

Write the null and alternative hypotheses for the example we're working on.

Chi-Square Test Statistic
===
$$\chi^2 = \sum \dfrac{(observed \ count - expected \ count)^2}{expected \ count}$$

with df = (# rows - 1)(# columns - 1)

What would a large or small value of $\chi^2$ mean?

Perform the Chi-Square hypothesis test for 2002, 2001
===

* Step 1: Hypotheses
* Step 2: Test statistic
* Step 3: p-value
* Step 4: Conclusion

* Interpret the p-value

Notes on Using the Chi-Square Test
===

* Rejecting null hypothesis does not tell us which way the interaction happens.
* Since $\chi^2$ is always positive, there is only an upper tail. We never multiply the probabilities by 2.
* Conditions: We can use the Chi-Square test when:
  * For tables larger than $2 \times 2$: Average of expected counts $\geq 5$; all expected counts $\geq 1$
  * For $2 \times 2$ tables: All expected counts $\geq 5$
  
Is the following drug effective?
===

In an experiment, 600 people were divided randomly into three groups and given a placebo, a single dose, or a double dose of a drug. The observed results were:

\      | Placebo | Single | Double |         
-------|---------|--------|--------|-------
Improve| 50      | 57     | 78     | 
Didn't | 180     | 133    | 102    |

Result
===

$\chi^2 = 22.2$

What can we say?

Interpreting
===

Since the Chi-Squared test does not tell us how the interaction happens if we reject the null
hypothesis, how do we know if the drug is effective? (Maybe it makes people worse?)

Create the conditional distribution table. Which way should we make it?

Further analysis
===

Is a double dose of the drug significantly better than single dose?

$\chi^2=7.09$

Make a conditional probability table to interpret!

Working and childcare
===

As more women work, the effect of childcare on infants has been investigated. One study
looked at the relationship between infant-mother attachment and the time spent in childcare, with the
following results:

\        | Low                   | Moderate           | High             
---------|-----------------------|--------------------|------------------
         | (0-3 hours/week)      | (4-19 hours/week)  | (20-54 hours/week)
Anxious  | 24                    | 35                 | 5
Secure   | 11                    | 10                 | 8

<small>By J. Jacobson and D. Willie, reported in Statistical Record of Women Worldwide (Galen Research, 1991) and Introduction to Practice of Statistics, 13-th ed, Mendenhall, Beaver and Beaver.</small>

Result
===

Does the data provide evidence of a difference in attachment patterns with the amount of time spent
in childcare? Give the hypotheses, the test statistic, and the p-value with your conclusion. Use a 1% confidence level. What would change if we had used a 5% confidence level?

$\chi^2 = 7.27$

Further analysis
===

Combine the moderate and high childcare groups together, and test again. What is your conclusion?

$\chi^2 = 0.00158$

In R: chisq.test()
===


```r
tally(Street~Land.Contour, data=ames)
```

```
      Land.Contour
Street  Bnk  HLS  Low  Lvl
  Grvl    4    1    1    6
  Pave  113  119   59 2627
```
***

```r
chisq.test(tally(Street~Land.Contour, data=ames))
```

```

	Pearson's Chi-squared test

data:  tally(Street ~ Land.Contour, data = ames)
X-squared = 30.96, df = 3, p-value = 8.668e-07
```


