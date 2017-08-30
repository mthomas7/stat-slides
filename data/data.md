<style>
.footer {
    color: black;
    background: #E8E8E8;
    position: fixed;
    top: 90%;
    text-align:center;
    width:100%;
    font-size:0.75em;
}

.midcenter {
    position: fixed;
    top: 50%;
    left: 50%;
}

</style>


Data
========================================================
author: Math 145
incremental:false


An Experiment
===
<center>
Who likes tea?
</center>

A Typical State
===
Look at the number of death penalty cases - what is typical?
![](./exec.png)

<div class="footer">Footer</div>


===
How do we measure "typical"?
![](./table.png)

Handedness
===
How do we measure a person's handedness?


===
<center>
![](hand.png)
</center>

Distracted drivers
===
Are drivers more distracted when using a cell phone than when talking to a passenger in the car?  Researchers wanted to find out, so they designed an experiment.  Here are the details.

In a study involving 48 people, 24 people were randomly assigned to drive in a driving simulator while using a cell phone. The remaining 24 were assigned to drive in the driving simulator while talking to a passenger in the simulator. Part of the driving simulation for both groups involved asking drivers to exit the freeway at a particular exit. In the study, 7 of the 24 cell phone users missed the exit, while 2 of the 24 talking to a passenger missed the exit.  (from the 2007 AP* Statistics exam, question 5)



===
Let’s start by summarizing the data from this study.  Each of the 48 people in the experiment can be classified into one of the four cells in the table below based on the experimental condition to which they were assigned and whether they missed the designated exit.  Use information from the previous paragraph to complete the table.


|              |     | Distraction |           |
|--------------|-----|-------------|-----------|
|              |     | Cell phone  | Passenger |
| Missed exit? | Yes |             |           |
|              | No  |             |           |


How could we visualize these data?
===

What are the proportions of each group?
===
(And why is this a badly posed question?)

What if it didn't make a difference?
===
- What would we expect then?
- What would happen if we reassigned the 48 people in this experiment to the cell phone and passenger groups many times, assuming that the group assignment had no effect on whether each driver missed the exit?  Let’s try it and see.

The Plan
===
We need 48 cards to represent the 48 drivers in this study.  In the original experiment, 9 people missed the exit and 39 people didn’t miss the exit.  If the group assignment had no effect on drivers' distraction, these results wouldn’t change if we reassigned 24 people to each group at random.  For a physical simulation of these reassignments, we need 9 cards to represent the people who will miss the exit and 39 cards to represent the people who won’t miss the exit.  With your group members, discuss which cards should represent which outcomes.  When you have settled on a plan, designate one member of your group to share your plan with the class.  

Experiment
===
Now you’re ready to simulate the process of reassigning people to groups.  “Shuffle up and deal” two piles of 24 cards—the first pile representing the cell phone group and the second pile representing the passenger group.  Record the number of drivers who missed the exit in each group.

More Experimenting
===
Repeat this process 9 more times so that you have a total of 10 trials.  Record your results in a table.

| Trial | Number who missed exit in cell phone group | Number who missed exit in passenger group |
|:-----:|:------------------------------------------:|:-----------------------------------------:|
|   1   |                                            |                                           |
|   2   |                                            |                                           |
|   3   |                                            |                                           |
|   4   |                                            |                                           |
|   5   |                                            |                                           |
|   6   |                                            |                                           |
|   7   |                                            |                                           |
|   8   |                                            |                                           |
|   9   |                                            |                                           |
|   10  |                                            |                                           |



Compare
===
In the original experiment, 7 of the 24 drivers using cell phones missed the freeway exit, compared to only 2 of the 24 drivers who were talking to a passenger.  How surprising would it be to get a difference this large or larger simply due to chance if the effects of the two experimental conditions on drivers’ distraction were actually the same?  You can estimate the chance of this happening with the results of your simulation.

In how many of your 10 simulation trials did 7 or more drivers in the cell phone group miss the exit?  Why don’t you need to consider the number of people in the “talking to a passenger group” who missed the exit?

===
Combine results with your classmates.  In what percent of the class’s simulation trials did 7 or more people in the cell phone group miss the freeway exit?

Based on the class’s simulation results, do you think it’s possible that cell phones and passengers are equally distracting to drivers, and that the difference observed in the original experiment could have been due to the chance assignment of people to the two groups?  Why or why not?

===
Here are the results of 1000 trials of a computer simulation, like the one you did with the playing cards, showing the number of drivers who missed the exit in the cell phone group.

![](./hist.png)


In general...
===
* How do we decide what is "surprising?"
* What do we compare our results to?

Cases vs variables
========================================================
Suppose you are conducting a test on a webpage redesign. You create two versions, randomly showing the different versions to different people. You measure how much time each person spends on the page, how many links they click on, and their operating system.

What are the:
* Cases?
* Variables?

Types of variables
====
incremental:false
What type of variable is:

Hair color?

Continuous

Discrete

Nominal

Ordinal

Types of variables
====
incremental:false
What type of variable is:

Age?

Continuous

Discrete

Nominal

Ordinal


Types of variables
====
incremental:false
What type of variable is:

The state you were born in?

Continuous

Discrete

Nominal

Ordinal


Types of variables
====
incremental:false
What type of variable is:

The day's high temperature?

Continuous

Discrete

Nominal

Ordinal

Types of variables
====
incremental:false
What type of variable is:

A Likert scale?

Continuous

Discrete

Nominal

Ordinal


Types of variables
====
incremental:false
What type of variable is:

Telephone number?

Continuous

Discrete

Nominal

Ordinal

PPSS
===
incremental:false

Situation: You want to estimate the average height of all IC students, so you measure 150 heights. The **parameter** is:

A. The average height of the 150 student

B. The average height of all IC students

C. The 150 students that were measured

D. All IC students

PPSS
===
incremental:false

Situation: You want to estimate the average height of all IC students, so you measure 150 heights. The **statistic** is:

A. The average height of the 150 student

B. The average height of all IC students

C. The 150 students that were measured

D. All IC students

PPSS
===
incremental:false

Situation: You want to estimate the average height of all IC students, so you measure 150 heights. The **population** is:

A. The average height of the 150 student

B. The average height of all IC students

C. The 150 students that were measured

D. All IC students

PPSS
===
incremental:false

Situation: You want to estimate the average height of all IC students, so you measure 150 heights. The **sample** is:

A. The average height of the 150 student

B. The average height of all IC students

C. The 150 students that were measured

D. All IC students

Returning to the decks of cards
===
incremental:false

Report:
* Which deck?
* Methods
  * How many cards?
  * How was each selected?
* List of parameters
* List of statistics and the value of each one
* Expected value for each statistic (assuming a fair deck)
* Conclusion
  * Is the deck fair?
  * How much $ would you wager?

The questions
===
incremental:false
1. What will your sample be? How many cards will you
draw?

2. How will you select each card from the deck? Be 
specific enough so that a classmate could do exactly 
what you did. 

3. What parameters would you like to estimate? (For 
example, “the % of all cards that are face cards” is a 
possible parameter.) List all of the parameters you will 
look at.

4. For each parameter, what statistic will you measure? 
List all of them.

5. For each statistic, what value would you expect it to 
have if your deck were fair?


Independence vs association/dependence
===
What does it mean for variables to be independent?

An example
===
incremental:false
Associations of handedness with hair color and learning disabilities
Steven C. Schachter, Bernard J. Ransil, Norman Geschwind
<small>http://www.sciencedirect.com/science/article/pii/0028393287901370</small>

Abstract

Forms containing the Edinburgh handedness inventory and questions about learning disabilities, hair color, self-described handedness, age, gender, parental handedness and twinning were received from 1117 randomly selected professionals. Laterality scores (LS, range −100 to + 100) were calculated for each respondent based on the handedness inventory and were correlated with the above variables. Among blonds, the frequency of non right-handedness (NRH, LS ⩽70) was 44% compared to 24% of non-blonds (x2=23.5, P <0.0001). Learning disabilities (LD) were present in 9% of NRH (LS ⩽70) as against 3% of those with LS > 70 (x2=22.1, P<0.0001). Associations between LS and self-described handedness, parental handedness, gender, and age are also presented. Possible explanations for the association of hair color and handedness are discussed in light of recent data on altered visual system pathways in albinos. Problems in the measurement of handedness are discussed.

Explanatory vs response variables
===
What would each be in the previous example?

Association vs causation
===
What's the difference?

* Ice cream sales and shark attacks
* Children with larger shoe sizes read better
* Countries with more TV sets per person have longer life expectancy
* Study time and test scores

Another example
===
<div align="center">
<img src="correlation.png" width=800>
</div>

Interpreting experiments
===
To investigate the safety of the anesthetics used in surgery, records from 850,000 operations in 34
major hospitals were examined. The death rates for four common anesthetics are shown in the table.

| Anesthetic | A    | B    | C    | D    |
|------------|------|------|------|------|
| Death Rate | 1.7% | 1.7% | 3.4% | 1.7% |

Which is the explanatory variable and which is the response variable?

Observational or experimental study?

Which hospital would you go to?


Sampling
===
Sampling techniques:
* Simple random sampling
* Stratified sampling
* Cluster sampling
* Multistage sampling

When might you use each?

An Example
===
incremental:false
You want to know the caloric intake of MLB players. You survey 3 players from each team. This is:

A. Simple random sampling

B. Stratified sampling

C. Cluster sampling

D. Multistage sampling

An Example
===
incremental:false
You want to know the caloric intake of MLB players. You survey 2 entire teams. This is:

A. Simple random sampling

B. Stratified sampling

C. Cluster sampling

D. Multistage sampling

An Example
===
incremental:false
You want to know the caloric intake of MLB players. You survey 3 players from each of 7 randomly chosen team. This is:

A. Simple random sampling

B. Stratified sampling

C. Cluster sampling

D. Multistage sampling

Means
===
For what kind of data?

How do we compute?

Histograms
===
What kind of data?

Skew
===
What does skew measure?

Mode
===
What does it measure?

Median
===
What does is measure?

What if there are an even number of numbers?

Standard deviation vs IQR
===
How are each computed?

SD: Why do we take the square root?

$\sigma$ vs $s$

Why denominator of $n-1$?

On a histogram...
===
* Mean is a balance point
* Median has half the data on either side
* SD is the "average distance from the mean"

Sensitivity
===
Which of the statistics are sensitive vs robust?

How can we tell?

In the # of death penalty cases, what happens if Texas is removed?

Example
===

Data set: 1, 2, 9, 20, 5

Mean? Median? SD?

Why is the mean larger than the median?

Making box plots
===
What kind of information does this display?


Contingency tables
===
For what type of data?

Notation
===
* Sample mean: $\bar{x}$
* Population mean: $\mu$
* Sample proportion: $\hat{p}$
* Population proportion: $p$
