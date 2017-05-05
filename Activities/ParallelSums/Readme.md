# Parallel Sums

## Objectives

* Explore a way of doing sums in parallel
* Employ:
   * a master-slave way of solving the problem
   * a peer-based method without using a master
* Discuss the pros-cons of each method

## Learning objectives

* Benefits of doing a task in parallel
* Awareness of the overheads that parallelism introduces
* Two different parallel implementation models that can be used with the pros and cons of each approach

## Equipment

* List of cards with a number printed on each card, repetitions allowed, make them quite
  low as they will be have to be added by the participants. Note the total sum.
* A set of empty cards for people to fill their local summation in. If you laminate and
  use dry wipe pens you may be able to re-use these - in which case you may also want a set of cloths to wipe the numbers out.

## Method

### Master-slave model

* Give all participants a blank card and a pen.
* Decide who is going to take on the role of the master. Give them all the 
   numbered cards.
* Get the master to shuffle the cards and distribute them evenly amongst the
  worker nodes. If there are spare cards get the participants to decide on the best
  way to distribute these, e.g.
   * If all participants are of the same ability you could distribute the remainder
     evenly amongst some of the participants, so some will end up with an extra card.
   * If participants are of different abilities you could give the extra cards to 
     the person who is best at sums or the oldest.
   * etc.
* Each participant will calculate the sum of all the cards they have been assigned
  and return the sum to the master process once they are finished. The master just has to wait until he receives all the partial sums.
* Master process sums up the partial sums to calculate
  the global sum.
* Check that the global sum agrees with your precalculated value - if not you
  may have to undergo a debugging phase.

#### Discussion points

* Trying to achieve good parallelism means keeping all the processors busy doing
  useful work. Where do the weaknesses in the above algorithm lie?

### Peer-based model

In principle all processes would open and read 
from the same file - the remainder will have been
worked out and a strategy chosen before hand, so 
for this example all participants will start with
a set of cards. For this example say N is the total number of participants. Each participant will need a piece
of paper as to do their sums as well as one of the 
blank cards. Get the participants to stand in 
a ring then:

* Each participant will calculate the sum of their
  cards and write it down on their blank card (and
  also on the bit of paper they have).
* Each participant will send their total, which they
  wrote on one of the blank cards,to the person
  on their left and receive the partial sum from the
  person on their right. Get them to keep a count 
  of the number of times they are passing on a 
  number. They want to do this N-1 times.
* Each person will add the partial sum they got on
  to the total they are keeping on the bit of paper.
* Each participant will send the partial sum they 
  received to the next participant on the left and
  receive a new partial sum from the right (an
  alternative might be to send the running total
  along the ring but if someone makes a mistake
  the error will propagate - this way you are  
  localising the problem).
* Repeat this N-1 times.

After N-1 communications all participants should 
have calculated the global sum. Check they have all
added numbers correctly.

#### Discussion points

* Compare and contrast this approach with the 
  master-slave approach. What are the disadvantages of 
  this approach?
* Is this the best communications pattern that could
  be used?

<!-- Licensing and copyright stuff below -->
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

