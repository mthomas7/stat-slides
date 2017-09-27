<style>
.vert {
    position: relative;
    top: 25%;
}

.footer {
    color: black;
    background: #E8E8E8;
    position: fixed;
    top: 90%;
    text-align:center;
    width:100%;
}


.container {
    display: flex;
    align-items: center;
    justify-content: center;
}

.center {
    right: 50%;
    bottom: 50%;
    transform: translate(50%,50%);
    position: absolute;
}

</style>


Probability
========================================================
author: Math 145
date: 
autosize: false

Project groups
===

Monty Hall
===

<center>
<iframe width="1120" height="630" src="https://www.youtube.com/embed/OBpEFqjkPO8" frameborder="0" allowfullscreen></iframe>
</center>

Cards
===
If I show you a yellow, what is the probability the other side is yellow?

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

Rain and snow in ithaca are likley not independent - what does this mean as a probability statement?

Sex and handedness: 13% of men and 13% of women are left handed (LH). We say handeded-ness is
independent of gender. In a population that is 50% female, we have $P(LH)=0.13$ and $P(M)=0.5$. Find $P(LH \ and \ M)$.

Test for Independence
===
$P(A)P(B) = P(A \ and \ B)$ is a way of testing for independence

Is this a statement about populations or samples?

Colorblindness
===
incremental:true

Given that 0.4% of women, 7% of men are color blind (CB), and that there are 50% women in the population,
find the proportion of color blind people in the population.

What if it's not 50/50?

Are sex and colorblindness indepdendent?


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

Indepdence and conditional probabilities
===
class:vert
What would an indepdence statement look like in the setting of conditional probabilities?


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
