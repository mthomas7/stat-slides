Inference with categorical variables
========================================================
author: Math 145
date: 

The problem
===
Suppose we want to compare proportions of men, women, and children? Or we want to compare the mean effect of a drug on Whites, African-Americans, Hispanics, and Asians?

New tests
===
* Chi-Square Test: For categorical variables, more than two samples
* ANOVA (Analysis of Variance): For quantitative variables, more than two samples

ABC Poll of 1500 adults, 750 men, 750 women on Presidential approval rating
===
incremental:true

On March 10, 2002, 623 men, 607 women approved of Bush’s handling of job. Was there a gender gap in the approval ratings significant at the 5% level?

On Sept 9, 2001, 443 men out of 750 and 390 women out of 750 approved of Bush’s handling of
job. Is there a gender gap in the approval ratings significant at the 5% level?

Looking at counts
===
incremental:true
Create two-way tables for the data in the previous two problems

Create *joint* and *conditional* probability tables

Which conditional probability table is more interesting to us right now?

An Expected Count Table
===
incremental:true

What would you expect if there were no relationship between the two variables? Use the same total count in each grouping.

$Expected \ cell \ count = \dfrac{Row \ total \times Column \ total}{n}$

Difference tables
===
incremental: true

Now we make a table of differences, with Observed - Expected

What differences do you see between the tables of differences that may indicate significance?

What do you notice about the sums of the differences in one table? How many values are needed to
determine all the others?

*We say the table has one degree of freedom.*

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

Comparing the tests
===
incremental: true
Compare the results of the proportion tests with the $\chi^2$ tests?

Will the results always be the same?

NO!

Examining the vote
===
![](graph.jpg)
from http://theithacan.org/news/ithaca-college-students-vote-no-confidence-in-president-rochon/

Schools
===
The results also varied by school. Of the 351 students who voted in the School of Business, 42.45 percent voted no confidence. The Roy H. Park School of Communications had 1,041 respondents, with 76.95 percent voting no confidence. The School of Health Sciences and Human Performance had 804 students vote, with 59.95 percent voting no confidence. The School of Humanities and Sciences had 1,238 students vote, with 81.58 percent voting no confidence. The School of Music had 314 students vote with 78.66 percent voting no confidence.

Is there a relationship between voting and school?


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

       | Placebo | Single | Double |         
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
incremental:true
Is a double dose of the drug significantly better than single dose?

$\chi^2=7.09$

Make a conditional probability table to interpret!

Working and childcare
===

As more women work, the effect of childcare on infants has been investigated. One study
looked at the relationship between infant-mother attachment and the time spent in childcare, with the
following results:

         | Low                   | Moderate           | High             
---------|-----------------------|--------------------|------------------
         | (0-3 hours/week)      | (4-19 hours/week)  | (20-54 hours/week)
Anxious  | 24                    | 35                 | 5
Secure   | 11                    | 10                 | 8

<small>By J. Jacobson and D. Willie, reported in Statistical Record of Women Worldwide (Galen Research, 1991) and Introduction to Practice of Statistics, 13-th ed, Mendenhall, Beaver and Beaver.</small>

Result
===
incremental:true

Does the data provide evidence of a difference in attachment patterns with the amount of time spent
in childcare? Give the hypotheses, the test statistic, and the p-value with your conclusion. Use a 1% confidence level. What would change if we had used a 5% confidence level?

$\chi^2 = 7.27$

Further analysis
===
incremental:true
Combine the moderate and high childcare groups together, and test again. What is your conclusion?

$\chi^2 = 0.00158$
