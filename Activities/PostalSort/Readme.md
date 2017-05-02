# Postal sort

Every year in Britain, more than 15 billion (that’s 15 followed by 9
zeros!) letters and parcels are sent through the post. That’s around
40 million pieces of post per day! The Post Office has to make sure
that all of the letters and parcels gets to their destination as soon
as possible. To do this, the Sorting Office needs to have a system
that lets it sort many pieces of post at the same time. For example,
if there is only one sorting machine, they can only sort one piece of
post at a time. However, if there are five machines, they can sort
through the post much faster! This is called parallelism.

This is what EPCC does. At EPCC, we use parallelism to build very fast
computers. People can then use these to solve difficult tasks, like
designing cars, modelling the universe, seeing how molecules interact
or predicting the weather – things that are too small, too big, too
fast or take to long to do experiments on. Each computer is made of
lots of smaller computer 'brains', called cores. Our biggest computer,
ARCHER, has 118,080 cores and can do 1 600 000 000 000 000
calculations every second (that is a 16 with 14 zeros after it)! We
use this to build programs that can simulate complicated situations
very quickly, like air flowing over a car.

In this activity, you can see for yourself how parallelism makes difficult
tasks much easier, and faster.

## Sorting Algorithms

Computers, phones and tablets read in and write out lots of
data. Sorting this data is essential.

You may for example want to order your data, with the largest values
first.

Good sorting algorithms make your computer code run faster and take up
less space. This can help you fit more games on your phone!

## Parallel Sorting Algorithms

Sorting data is often used on supercomputers. On a supercomputer
you need to carry out your sort on many cores. Hence you need a
parallel sorting algorithm.

Examples include:

* [Quicksort](https://en.wikipedia.org/wiki/Quicksort)
* [Bubble sort](https://en.wikipedia.org/wiki/Bubble_sort) 
* [Radix sort](https://en.wikipedia.org/wiki/Radix_sort)

An example: The parallel bucket sort

A set of numbers can be sorted using a bucket sort. This starts by
separating the numbers into groups – called buckets.

![Bucket sort](imgs/bucket-sort.png)

The numbers inside each bucket are then sorted. Each bucket can be
sorted in parallel. This is similar to how we sort on a supercomputer
one core sorts a set of data at the same time that another core sorts
a different set of data.

# The post sorting activity

## Setup your demo

To setup your post sorting activity, download the address labels and
stamps templates:


* Print address labels: print the address labels on Avery No. L7163
  post label pages (or equivalent). This is ‘one set’ of
  labels. Ideally print three to five copies of these first three
  pages, resulting in multiple sets.
* Print the stamps. Print the ARCHER stamps to complete your letters
  on Avery No. L4736REV-25 labels (or equivalent). There are 48 stamps
  per page. Print enough so you have one per address label (for three
  full sets of address pages you will need 2 sheets). Spare labels can
  be given out as badges.
* Setup up your envelopes. Stick an address label and stamp on each
  envelope. One full set is 36 addresses, so for three sets you will
  need 144 envelopes, for five setups you will need 216 envelopes .
* Gather sorting boxes.
* Source 12 boxes to sort your envelopes into. Examples include the
  lids of photocopier paper boxes. These will be labelled
* Source 5 boxes/bags to sort envelopes from. Examples include a
  simple bag or the bottom of photocopier paper boxes. These are left
  unlabelled.
* Label your boxes. Label each sorting box, labelling one box with
  each of the following:

KW
KW1
KW2
KW3
EH
EH1
EH2
EH3
SN
SN1
SN2
SN3
TR
TR1
TR2
TR3

### Running the activity: A single-person post sort

* Arrange your KW1, KW2, KW3, EH1, EH2, EH3, SN1, SN2, SN3, TR1, TR2,
  TR3 boxes on a table.

* Put all unsorted envelopes into an unlabelled box/bag.  One person:
  taking one envelope at a time out of the bag sort the envelopes into
  the boxes based on the first two letters and first number of the
  postcode.

Question: How many envelopes can you sort in 60 seconds? 

Question: How could you sort more envelopes in the same amount of time? 

Question: How could you use multiple people to do this sort?

### Running the activity: A two stage sort using multiple people

This activity introduces the concept of parallel sorting. The task is
now split into two 30 second jobs, instead of one 60 job and uses four
people that we will call A, B, C, D and E.

Step one: one person for 30 seconds

Arrange your KW, EH, SN and TR boxes on a table.

Put all unsorted envelopes into an unlabelled box/bag.

Person A: taking one envelope at a time out of the bag sort the
envelopes into the boxes based on the first two letters of the
postcode.

Question: How many envelopes can you sort in 30 seconds? 

Step two: four people for 30 seconds

Arrange your KW1, KW2, KW3, EH1, EH2, EH3, SN1, SN2, SN3, TR1, TR2,
TR3 boxes on a table.

At the same time:

Person B: taking one envelope at a time from box KW sort the envelopes
into the boxes based on the first number of the postcode into boxes
KW1, KW2, KW3.

Person C: taking one envelope at a time from box EH sort the envelopes
into the boxes based on the first number of the postcode into boxes
EH1, EH2, EH3.

Person D: taking one envelope at a time from box SN sort the envelopes
into the boxes based on the first number of the postcode into boxes
SN1, SN2, SN3.

Person E: taking one envelope at a time from box TR sort the envelopes
into the boxes based on the first number of the postcode into boxes
TR1, TR2, TR3.

Question: How many envelopes do People B, C, D and E sort in 30 seconds? 

Question: How does this compare to a single person sort?

Question: How could you make this more efficient? (consider placement
of boxes, overlapping step one and step two etc.)

Question: What happens when you add more friends? Could you
parallelise this sort further by sorting by the second number as well?
What would be the benefit of this? Can you plot the number of letters
sorted against the number of friends helping in the sort?

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
