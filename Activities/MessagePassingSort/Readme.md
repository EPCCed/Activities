# Message passage sorting

Demonstrate how a list of numbers can be sorted in parallel.

## Learning objectives

* Demonstrate how inter process dependencies can be solved by message passing.
* Process tasks


## Equipment

The equipment required for this activity is relatively simple
and can go as far as your budget will stretch. The minimum
set-up would be:

* A set of cards with integers clearly marked from 1 to N where N
  can be as large as you like

## Overview

This activity can have as many people as you like but the larger the
set of numbered cards or people you have the longer it will take.
Perhaps, for this reason, this activity is more suitable for a
classroom environment rather than a science festival. It is also
relatively easy to get yourself and/or participants in a muddle.

For this example we will assume you have 3 people and a set of cards
numbered from 1 to 12. Get people to stand in a line, shuffle the
cards and give each of them 3 cards:

![Starting configuration](imgs/MessagePassing1.png)

Get each participant to sort the cards they have been assigned:

![Local sort](imgs/MessagePassing2.png)

Now number your participants starting from 0 to P-1, where P is the
total number of participants (you can use 1 to P but the Message
Passing Interface (MPI) library that would generally be used to
implement this type of algorithm starts counting from zero). You have
to proceed with the algorithm in two phases:

Get each even numbered participant to compare the highest number they
with have lowest number the person on the right has which means that odd
numbered participants must turn to the people on their right and
compare their lowest number with the highest number the person on the
right has. If the lower number is higher than the high number then
swap otherwise do nothing. If you are on of the participants standing
at the ends and you have no participant on your left or your right do
nothing.
	     
![First message passing](imgs/MessagePassing3.png)

Do a local sort of the numbers each participant has.
   
![Second local sort](imgs/MessagePassing4.png)

Now even numbered participants must turn to people on their right and
show their lowest number and compare it with the highest number of the
person on the right. Odd numbered people turn to people on their left
and show their left and show their highest

![First message passing](imgs/MessagePassing5.png)

Now you do another local sort:

![Second local sort](imgs/MessagePassing6.png)

and you go back to the first message passing routine until all the cards are sorted:

![Final configuration](imgs/MessagePassing7.png)

What is the terminating condition? How do you get all the processes to recognise that the entire list has been sorted if you are only privvy to your own local data?

## Scenarios

## Acknowledgements

* Male silhouette came from the [man shape](https://openclipart.org/detail/182185/man-shape) at openclipart.
* Female silhouette came from the female from the [Man/woman shape Carl Sagan plate](https://openclipart.org/detail/269831/manwoman-shape-carl-sagan-plate) at openclipart.

<!-- Licensing and copyright stuff below -->
<a href="http://www.epcc.ed.ac.uk">
<img alt="EPCC logo" src="https://www.epcc.ed.ac.uk/sites/all/themes/epcc/images/epcc-logo.png" height="31"/>
</a>
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" />
</a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
Creative Commons Attribution 4.0 International License</a>.<br/>
&copy; Copyright EPCC, The University of Edinburgh 2017.
