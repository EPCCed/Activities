# Postal sort

## Motivation
This is an example of a [bucket
sort](https://en.wikipedia.org/wiki/Bucket_sort). For this activity we have a number
of letters with specific postcodes that need to be sorted for
delivery. We first separate the postcodes into the major components:
so for the example provided all of the EH10, EH21 and EH32 need to be aggregated into an EH box,
the TR10, TR21 and TR32 get aggregated into a TR box and so on.
The letters are later separated into the individual postcodes ready for
the postman to deliver them.

In general, bucket sorts start by separating the numbers into groups
– called buckets. In the example below the numbers are first separated
into three buckets: numbers below or equal to 10, numbers between
11 and up to and including 20 and over 20.

![An example of a bucket sort](imgs/bucket-sort.png)


The numbers inside each bucket are then sorted. There are two
different stages that can thus be parallelised and different strategies
can be explored to obtain the optimal throughput.

## Learning objectives

* Multiple people sorting will do more than one person in the same
  time or the same end can be achieved in less time.
   * Modern computers employ parallelism to the same ends.



## Equipment

To perform this activity you will need:

  * A 30 second/minute count down timer.
  * 12 boxes/letter trays/desk trays to sort envelopes into. Examples include the
    lids of photocopier paper boxes, stackable letter desktop trays, etc. 
  * A number of boxes/bags to pre-sort envelopes to. The number of
    containers you will need depends on the type of postcodes you
    are dealing with - for instance in the picture below we are
    only dealing with KW, TR and EH postcodes so you only need 3
    pre-sorting trays. If you use all the postcodes in the samples
    below you will need four containters. You could use simple bags
    or the bottom of photocopier paper boxes for this.
  * A box/bag to act as the source for the unsorted envelopes.
  * You will need envelopes for your participants to sort. You can can make your
    own or you could print the following example 36
    [address&nbsp;labels](pdf/Post_sorting_address_labels_AveryL7163.pdf)
    on Avery No. L7163 post label pages (or equivalent).  Ideally
    print three to five copies of these first three pages, resulting
    in multiple sets. If you are feeling energetic you can also
    print a set of [stamps](pdf/Post_sorting_stamps_AveryL4736REV-25.pdf)
    for your letters. You can print these ARCHER stamps to complete
    your letters on Avery No. L4736REV-25 labels (or equivalent).
    There are 48 stamps per page. Print enough so you have one per
    address label (for three full sets of address pages you will
    need 2 sheets). As
    the completed letters are likely to get a lot of handling you
    should ideally laminate them.

You can localise the demo to use your own regional addresses. We
have provided pdf examples with ARCHER branding and UK addresses
above.

![Example kit](imgs/postal-kit.png)
Example kit with the bag containing the envelopes on the left, the
pre-sorting trays in the trolley (we were unable to use these because
of space constraints) and the labelled final pigeon holes the letters
go into.

![Kit in use](imgs/post-in-use.png)
Here is the kit in use.

## The post sorting activity

### Setting up the demo

To setup your post sorting activity, download the address labels and
stamps templates:

* **Setup up your envelopes**. Stick an address label and stamp on each
  envelope. One full set is 36 addresses, so for three sets you
  will need 144 envelopes, for five setups you will need 216 envelopes.
* **Label your boxes**. Label each sorting box, labelling one box with
  each of the following:
   * KW
      * KW1
      * KW2
      * KW3
   * EH
      * EH1
      * EH2
      * EH3
   * SN
      * SN1
      * SN2
      * SN3
   * TR
      * TR1
      * TR2
      * TR3

### Running the activity 

A single-person post sort

* Arrange your KW1, KW2, KW3, EH1, EH2, EH3, SN1, SN2, SN3, TR1, TR2,
  TR3 boxes on the floor or a table.

* Put all unsorted envelopes into an unlabelled box/bag.  

* One person: see how many envelopes they can sort in a minute by only
  taking one envelope at a time out of the bag to sort the envelopes into
  the boxes based on the first two letters and first number of the
  postcode.


### Running the activity: A two stage sort using multiple people

This activity introduces the concept of parallel sorting. The task is
now split into two 30 second jobs, instead of one 60 second job and uses four
people that we will call A, B, C, D and E.

Step one: one person for 30 seconds

Arrange your KW, EH, SN and TR boxes on a table.

Put all unsorted envelopes into an unlabelled box/bag.

Person A: taking one envelope at a time out of the bag sort the
envelopes into the boxes based on the first two letters of the
postcode.

**Question**: How many envelopes can you sort in 30 seconds? 

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

## Discussion points

**Question**: How could you sort more envelopes in the same amount of time? 

**Question**: How could you use multiple people to do this sort?

**Question**: How many envelopes do People B, C, D and E sort in 30 seconds? 

**Question**: How does this compare to a single person sort?

**Question**: How could you make this more efficient? (consider placement
of boxes, overlapping step one and step two etc.)

**Question**: What happens when you add more friends? Could you
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
