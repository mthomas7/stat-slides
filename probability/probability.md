<style>
.footer {
    color: black;
    background: #E8E8E8;
    position: fixed;
    top: 90%;
    text-align:center;
    width:100%;
}

.smfooter {
    color: black;
    background: #E8E8E8;
    position: fixed;
    top: 90%;
    text-align:center;
    width:100%;
    font-size: 5em;
}

.horiz {
  text-align:center;
}

.vert {
 position: relative;
 top: 50%;
 transform: translateY(-50%);
 }

.small-code pre code {
  font-size: 40em;
}

</style>


Probability
========================================================
author: Math 145
date: 
autosize: false

Project
===
class:small-code


<!--
Monty Hall
===

<center>
<iframe width="1120" height="630" src="https://www.youtube.com/embed/OBpEFqjkPO8" frameborder="0" allowfullscreen></iframe>
</center>
-->

Questions
===

* Monty hall problem

* If I show you a blue, what is the probability the other side is blue?

* If I show you a card, what's the probability the other side is the same color?

Probability
===
How do we interpret both of these problems?

Coin flipping
===
Either flip a coin 50 times, or pretend to flip a coin 50 times. Record the results.

What is probability?
===
type:section

Probability
===
Sample space vs event

Law of large numbers
===
incremental:true

Say you flip a (fair) coin many times - what do you expect to be true about the number of heads and the number of tails? What do you expect to happen as the number of flips gets larger?

$\hat{p}_n \approx p$, and gets better as n gets larger

Terminology
===
ANDs and ORs

Disjoint / Mutually Exclusive
===
Disjoint events are those which cannot happen simultaneously.

E.g. draw a card. It is either a heart, spade, diamond, or a club. It cannot be more than one of these.

Addition rule
===
$P(Club \ or \ Diamond) = P(Club) + P(Diamond)$

Non-disjoint
===
$P(Club \ or \ King)=$?

Complements
===
$P(not \ a \ club) = P(club^c) =$?

Independence
===
incremental:true
We should use a tree diagram - what does it mean for two events to be independent?

Rain in Ithaca and whether or not your cousin catches the train in LA are independent. (Unless you
call her because of the rain and delay her.....)

Rain and snow in ithaca are likely not independent - what does this mean as a probability statement?

Sex and handedness: 13% of men and 13% of women are left handed (LH). We say handeded-ness is
independent of gender. In a population that is 50% female, we have $P(LH)=0.13$ and $P(M)=0.5$. Find $P(LH \ and \ M)$.

Test for Independence
===
$P(A)P(B) = P(A \ and \ B)$ is a way of testing for independence

Is this a statement about populations or samples?

Fire alarms
===
Suppose a dorm has a 3% chance of a fire alarm going off, and there are three dorms.
Assuming the chance of a fire alarm in a dorm is independent of the other dorms, what is:

* $P(\text{no alarms go off})$
* $P(\text{exactly one alarm goes off})$
* $P(\text{at least one alarm goes off})$

Independence
===
Suppose you have a standard deck of cards.

* Are drawing a jack and drawing a heart independent?
* Are drawing a jack and drawing a 2 independent?
* Are drawing a red card and drawing a heart independent?

Colorblindness
===
incremental:true

Given that 0.4% of women, 7% of men are color blind (CB), and that there are 50% women in the population,
find the proportion of color blind people in the population.

What if it's not 50/50?

Are sex and colorblindness independent?


Multiplication rule
===
incremental:true
* $P(A \ and \ B) = P(A)*P(B)$
* This is ONLY true for independent events

Conditional probability
===
$P(A|B)$

Describe in words the difference between $P(Color \ Blind|Male)$ and $P(Male|Color \ Blind)$

An Example
===

Sensitivity: true positive rate
Specificity: true negative rate

---

Suppose:
* sensitivity is 99%
* specificity is 98%
* prevalence is 5%

If you get a positive test result, what is the probability you have the disease?

Independence and conditional probabilities
===
class:vert

What would an independence statement look like in the setting of conditional probabilities?


Types of probabilities
===
* Marginal: $P(A)$
* Joint: $P(A \ and \ B)$
* Conditional: $P(A|B)$

How they're related
===
$$P(A|B) = \dfrac{P(A \ and \ B)}{P(B)}$$

Bayes' rule
===
$$P(A|B) = \frac{P(A)P(B|A)}{P(B)}$$

* We can justify this with a tree diagram
* Good for testing hypotheses

Probability distributions
===
type:section

An example
===
incremental:true

Suppose there's a 52% chance that a couple has a girl, and that birth sexes are independent of one another.

What is the sample space, presuming the couple has 3 children?

What is:
* $P(\text{exactly 0 girls})$?
* $P(\text{exactly 1 girls})$?
* $P(\text{exactly 2 girls})$?
* $P(\text{exactly 3 girls})$?
