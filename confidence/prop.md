Statistical Confidence - Proportions
========================================================
author: Math 145
date: 
autosize: false
width:1920

Notes
===
* We're going to deviate from the order in the book a little - chapter 6
* Lab

Reminder
===
What was a sampling distribution?

Let's consider a deck of cards
===

Suppose we want to know what percent of the deck is red

Grab A Deck
===

- How many cards should we draw?
- How should we draw them?
- Draw that many, then calculate the percentage, we'll record this
- Do this 10 times
- What if we drew a different number?
- How would this change the distribution?

Let's draw the distribution
===

What do we get
===
* This is a sampling distribution for $\hat{p}$
* It should look nearly normal
* Conditions:
  * observations are independent
  * expect at least 10 successes and 10 failures in our sample ($np \geq 10$, $n(1-p) \geq 10$)
* If this is true, the sampling distribution will be nearly normal with mean $p$ and standard deviation $\sqrt{\frac{p(1-p)}{n}}$.
  * This is called the standard error (any standard deviation of a sampling distribution)
* We write this as:
$$SE_{\hat{p}} = \sqrt{\frac{p(1-p)}{n}}$$

Estimates
===
* Point estimates vs interval estimates
* Interval estimates are usually 95%, we'll make 80% now

Terms
===
Margin of error - this is the distance from the point estimate to the ends of the confidence interval

What is the formula for the margin of error?

The "Usual" Defintion
===
Confidence interval:
$$\hat{p} \pm z^* S.E. = \hat{p} \pm z^* \sqrt{p(1-p)}{n}$$

or

$$(\hat{p}-z^* S.E.,\hat{p}+z^* S.E.) = (\hat{p}-z^* \sqrt{p(1-p)}{n},\hat{p}+z^* \sqrt{p(1-p)}{n})$$

How do we make sense of the $z^*$?

What can we change
===
* $n$?
* $p$?
* $\hat{p}$?
* $z^*$?

Sample Size Calculations
===
What if we want a specific margin of error. Can we select $n$ before we conduct the experiment?

Confidence Intervals for Testing Claims
===

* Suppose you want to test a claim that 52% of students like the food on campus.
* You sample 150 people, and find that 48% of the sample likes the food.
* What can we conclude?
