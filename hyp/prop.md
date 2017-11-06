Hypothesis Testing - Proportions
========================================================
author: Math 145
date: 
autosize: false
width:1920

A Confidence Interval As A Test
===
* An $\alpha$ level is stated *before* data is collected to determine a level of acceptable risk in the test (we'll be more specific about this later).
* If you make a 95% CI, $\alpha=0.05$
* If you make a 99% CI, $\alpha=0.01$
* In general, is the level of confidence is $X$, $\alpha=1-X$

What is a hypothesis test?
===
* We compare two hypotheses
* These are called the null hypothesis ($H_0$) and the alternative hypothesis ($H_A$)
* $H_0$ is always the claim we are testing
* $H_A$ is the/a alternative to that hypothesis

Example
===
During the Mozambique trial of a potential malaria vaccine, the effect of the drug was measured on:

* The number of children infected
* The length of time until infection

Are the variables quantitative? Or categorical?

Without the drug, the rate of severe malaria infection in the area of the study was 34.9 children per 1000. Of 745 children given the drug, 11 got severe malaria during the course of the study. Does this data suggest that the drug reduces the rate of severe malaria infections?

Population? Sample? Statistic? Parameter?

<small>
“Efficacy of the RTS,S/AS202A vaccine against Plasmodium falciparum infection and disease in young African children: randomized
controlled trial” by P. Alonso et al, The Lancet, Oct 16, 2004.
</small>

Solution
===
Note that 34.9/1000 = 0.0349 = 3.49%. This is the infection rate for the untreated population.

Let $p$ be the proportion of treated children in the population who get sick if we treated all of them.

* Step 1
    * Null hypothesis: We assume drug does not work: $H_0: p=0.0349$
        * Proportion of treated population getting sick = Proportion of untreated population getting sick = 0.0349.
    * Alternative hypothesis: Assume the drug works, we have a choice here
        * One sided test / one tailed test: The drug decreases the proportion of people who are sick, $H_A: p<0.0349$
        * Two sided test / two tailed test: The drug changes the proportion of people who are sick, $H_A: p \neq 0.0349$
        * The CIs we've been creating are equivalent to two-tailed tests
* Step 2
    * Find your $\hat{p}$, SE, ME, CI

Continued
===
* Step 3
    * Interpret (draw a picture)
* Step 4
    * Make a conclusion about the hypotheses - reject $H_0$ or fail to reject $H_0$
    
Another example
===
incremental: true

* A reporter in 2003 stated 2/3 population were in favor of sending troops to Iraq.
    * How would we test this claim?
* In 2003, a February 24-26 CNN poll of 1004 Americans found that 59% supported sending
troops to Iraq.
* Conduct a two-tailed hypothesis test for the claim made by the reporter, using $\alpha=0.1$

