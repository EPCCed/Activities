Introduction Routes
-------------------

Introducing Wee Archlet depends on who you are talking to (often this will follow from Wee Archie and about doing something similar themselves), what level and the interest shown. This tries to identify the main groups of individuals and give a starting point.

General Progression:

-   Ask them what a computer is, what they use it for and what else it could be used for

    -   Ask them what a supercomputer is - try to get them to arrive at something with prompts

    -   Talk about Wee Archlet, get them to use it

    -   Show them the parts, talk about the ease of putting it together, how it can be scaled down and up, that there are instructions available

    -   Ask why we need computers to support science, what benefits it can give us, and fill in blanks/ask questions as you go along

    -   Try to get them to come up with uses of a supercomputer


Key Points
----------

It is important to place emphasis that Wee Archlet are a small 'model' of a supercomputer - it operates in the same way a supercomputer would but lacks the network bandwidth and performance of a supercomputer. Supercomputers exploit parallelism to achieve high performances.

Highlight the analogous parts of Wee Archlet to the parts of a supercomputer.

-   `Raspberry Pi` - equivalent to a compute element of a supercomputer - see technical specification for model.

-   `4 Raspberry Pis workers` - these carry out the calculations and functions of a parallel program

-   1 Raspberry Pi is the network runner, file server and job manager - this hosts all the program and data files for the parallel programs, accepts jobs on the cluster and manages the network.

**Note**: *diagram here might be useful. Not sure if this is too low level because you are getting into a complicated space of I/O, parallel file systems, etc.*

-   `Network Switch` - equivalent to the interconnects

-   Allows the Raspberry Pis to communicate and the client computers to connect to the system

-   Note that supercomputers run interconnects that can be far faster than the commodity one used in Wee Archlet

-   `Power Unit` - the USB power supply and network switch power supply sitting along side the elements

    -   Note that Wee Archlet draws less power than an bright non-LED lightbulb

-   `Cooling System` - Wee Archlet does not have one

    -   Raspberry Pis do not require cooling at the levels of a real supercomputer

    -   Introduce why cooling is needed

### Purpose - why do we need supercomputers?

Solve more complex problems

-   solve existing problems faster, tomorrows weather today not tomorrow

-   solve larger problems, higher resolution weather forecasts

-   dangerous problems

-   problems which otherwise could not be explored, how global warming impacts weather systems

### Why use parallelism?

Splitting up large problems into smaller parts, give examples of tangible things and then move to more abstract computational examples. Focus on the idea of work being spread across the different elements.

### Why parallel

Talk about communications - highlight in most parallel situations data needs to be shared and updated as the computation takes place. Talk about the differences in speed between communication and computation. Highlight that speed-up is not perfect, two CPUs don’t do it twice as fast as one but are faster and scale it up.

Bottlenecks - talk about how some parts of the code may cause the rest to have to stop/slow down while it operates - particularly talk about serial parts in relation to parallel parts.

Deadlocks - talk about the importance on ensuring that data or processes that depend on each other are kept in synch - so for example you don’t end up with a case of one wanting data the other has but it is waiting on the first one to finish something else.

 

Supplemental Points
-------------------

Computer - ensure that the audience knows what a computer is and that they understand that it is a tool to enable us to do more.

Science on Computers - why

-   Speed

-   Accuracy

-   Danger

-   Cost

Talk about how modern science is very difficult to deal with/research in without the support provided by computers and software available to us.

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

