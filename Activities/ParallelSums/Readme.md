Parallel Sums
=============

Demonstrate how to do parallel sums in two ways:

-   a coordinator-worker way of solving the problem

-   a peer-based method

Learning objectives
-------------------

-   Benefits of working in parallel

-   Awareness of overheads introduced by parallelism

-   Introduction of two parallel approaches:

    -   Advantages and Disadvantages of parallel approaches

Equipment
---------

-   Set of number cards

-   Empty Cards

-   Scrap Paper (if needed)

-   Pens

### Note - Number Cards

Each card should have one number. Numbers do not have to be unique.  Use small
positive integers as participants will need to sum the numbers. The use of small
numbers helps enable a wide range of participation. It is important to note the
total sum of the cards in use.

### Note - Empty Cards

A set of empty cards for the participants to write their local sum on. To reduce
waste, laminated blank cards and dry-wipe pens will enable re-use of empty
cards.

Method
------

### Coordinator-worker model

-   Give all participants a blank card and a pen.

-   Decide who is going to take on the role of the Coordinator and give them the
    numbered cards.

-   Get the Coordinator to shuffle the cards and distribute them evenly amongst
    the worker participants. In cases where there are spare cards, get the
    participants to decide on the best way to distribute these, e.g.

    -   If the participants are all of equal ability, the remainder could be
        distributed evenly amongst the participants such that some have an extra
        card.

    -   If the participants are of different abilities, the extra cards could be
        given to the person who is best at sums.

-   Each participant will calculate the sum of the cards they have been given.
    They will write this on their blank card and return the card to the
    Coordinator once they are finished. The Coordinator has to wait until they
    receive all the partial sums.

-   The Coordinator will add up the partial sums to calculate the global sum.

-   Check the global sum agrees with the precalculated value - if they do not
    agree you may have to undergo a debugging phase.

#### Discussion points

-   Achieving good parallelism involves keeping all processors busy doing useful
    work. Could there be any weaknesses in this algorithm?

### Peer-based model

In this approach, there is no coordinator - each worker will calculate the sum
using information from their peers.

In principle all processes would open and read from the same file - the system
or algorithm will determine what each process reads.

For this example, all participants will start with a small set of cards taken
from the full set. This is all participants reading from the same file, but
reading different bits.

We can say that N is the total number of participants.

Each participant will need one blank card, pen and a piece of paper to do their
sums.

-   Get the participants to stand in a ring, each with their small set of
    numbered cards.

-   Each participant will calculate the sum of their cards and write it down on
    their blank card and their bit of paper.

-   Each participant will pass their total, written on the blank card, to the
    participant on their left and get a card with a partial sum from the
    participant on their right. Ask them to record the number of times they pass
    a number on. They want to do this N-1 times. So far 10 participants, they
    should pass 9 times.

-   Each participant will add the partial sum they got to the total they wrote
    on their bit of paper.

-   Each participant will send their partial sum card (without changing it) to
    the participant on their left and receive a new partial sum from the right.

-   Repeat this N-1 times.

After N-1 communications all participants should have calculated the global sum.
Check the total is correct.

#### Discussion points

-   Compare this approach with the coordinator-worker approach. What is better
    or worse about this peer-based version?

-   Is this the best communications pattern that could be used?

-   An alternative might be to send the running total along the ring? Could this
    introduce problems in the process? Hint - if someone makes a mistake the
    error will propagate - sending partial sums without changing their value
    localises the problem. One process may get it wrong, but other processes
    should still get the correct answer.

<!-- Licensing and copyright stuff below -->
<br>
<a href="http://www.epcc.ed.ac.uk">
<img alt="EPCC logo" src="https://www.epcc.ed.ac.uk/sites/all/themes/epcc/images/epcc-logo.png" height="31"/>
</a>
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
<img alt="Creative Commons License" style="border-width:0"
     src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" />
</a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.<br/>
&copy; Copyright EPCC, The University of Edinburgh 2017.

