# Parallel Sums

## Objectives

* Examine a way of doing sums in parallel
* Employ a:
   * master-slave way of solving the problem
   * a peer-based method without using a master
* Discuss the pros-cons of each method

## Learning objectives

* Benefits in doing a task in parallel
* Awareness of the overhead that parallelism introduces
* Different parallel models that can be used with the pros and cons of each method

## Equipment

* List of cards with a number on each card, repetitions allowed, make them quite
  low so that they will be have to be added by the participants.
* A set of empty cards for people to fill their local sums in. If you laminate and
  use a white board pen you may be able to re-use these - in this instance it might
  also be helpful to have a set of cloths to wipe the numbers.
* It might also be useful to have precomputed the sum of the cards that you will use
  to ensure that you get the correct answer at the end.

## Method

### Master-slave model

* Give all participants a blank card and a pen.
* Decide who is going to take on the role of the master slave. Give them the 
   numbered cards.
* Get the master to shuffle the cards and distribute the cards evenly amongst the
  worker nodes. If there are spare cards get the participants to decide on the best
  strategy, e.g.
   * If all participants are of the same ability you could distribute the remainder
     evenly amongst participants, so some end up with an extra card.
   * If participants are of different abilities you could give the extra cards to 
     the person who is best at sums or the oldest.
   * etc.
* Each participant will calculate the sum of all the cards they have been assigned
  and return the sum to the master process.
* Master process will sum up the partial sums as they receive them to calculate
  the global sum.
* Check that the global sum agrees with your precalculated value - if not you
  may have to undergo a debugging phase.

Discussion points:

* Trying to achieve good parallelism means keeping all the processors busy doing
  useful work. Where do the weaknesses in the above algorithm lie?

### Peer-based model

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

