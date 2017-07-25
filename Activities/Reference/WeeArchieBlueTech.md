Wee Archie Blue
===============

Wee Archie Blue is the second unit developed for demonstration purposes using
the Raspberry Pi series of single board computers. The blue name comes from the
use of the blue LEDs.

 
Wee Archie Blue Technical Specification:
----------------------------------------

### Overview Numbers

-   Number of Processors/Cores: 18/72.

-   Core Speed: 1GHZ.

-   RAM: 18 GB (1GB per board).

-   Storage: 408 GB (16 GB per board plus 120GB network shared).

-   Operating System: Raspbian “Jessie".


### Components

Wee Archie Blue is housed in an extruded aluminium frame with polycarbonate
facings and mounts.

The power and computation elements are:

-   18 Raspberry Pi 3 Model B

-   3 Netgear GS108 Switch

-   120 GB Sandisk Portable SSD

-   18 8x8 LED Matrices

-   2 5V 10A PSU



### Raspberry Pi 3 Model B Specification

-   Quad Core 1.2GHz Broadcom BCM2837 64bit CPU

-   1GB RAM

-   BCM43438 wireless LAN and Bluetooth Low Energy (BLE) on board

-   40-pin extended GPIO

-   4 USB 2 ports

-   Micro SD (16GB Cards in use)

-   Ethernet Port

 

The Raspberry Pi 3 units in Wee Archie Blue has been under clocked to 1GHz after
testing against applications including using OpenBLAS proved this to give stable
performance without power or heating issues in the cases. Each unit has a 16GB
MicroSD card with the operating system installed.

 

### Netgear GS108 Switch

-   Speed: 10/100/1000Mbps Ethernet

-   8 Ports with Auto-uplink negotiation

-   Max Power Consumption: 4.9W

 

The switches used in Wee Archie Blue are off-the-shelf Netgear units. The
Raspberry Pi network communications are well within the tolerances of the
switches and the power consumption is low. Each switch has its own 5V power
supply.

 

### 120 GB Sandisk Portable SSD

-   120 GB Capacity

-   USB3.0 Capable

-   Solid State

-   Low Operating Temperature

-   Silent Operation

 

The Sandisk SSD is a low power, portable drive used to hold the shared network
files for Wee Archie Blue.

 

### 8x8 LED Matrix

-   I2C Communications

-   64 Element Dot Matrix Display

-   Blue colour

 

The LED Matrices are used to give information on the status of a Raspberry Pi,
including core usage, network traffic and temperature.

 

Wee Archie Blue Performance
---------------------------

The performance of Wee Archie Blue was assessed using the Linpack benchmark
(<http://www.netlib.org/benchmark/hpl/>). For more detailed information on the
performance of Wee Archie Blue, there is a blog article available on the EPCC
blog (<https://www.epcc.ed.ac.uk/blog/2017/06/07/linpack-and-blas-wee-archie>).

For a single node (Raspberry Pi) using the standard ATLAS BLAS implementation on
Raspbian, the peak performance attained was 0.63 GFLOPS.  As detailed in the
blog linked above, this caused some queries to be raised and OpenBLAS was
complied for the Raspberry Pi 3. The performance using OpenBLAS in Linpack
caused a large increased to 3.58GFLOPs.

For Wee Archie Blue as a whole, the performance was assessed on 16 compute nodes
(16 of the Raspberry Pis with the remaining two managing the network and file
system). Using the ATLAS implementation the peak performance was 7.1 GFLOPs,
again causing concern. Then rerunning the benchmark using OpenBLAS this
increased to 25.1 GFLOPs.

These scores are not particularly impressive, but the focus of the machine is to
demonstrate how parallelism and supercomputers work not replicate the
performance. Though in the first ever top500 list, Wee Archie Blue would have
been number 5. And it consumes a lot less power and takes up less space.

| Number of Nodes | Linpack (ATLAS) | Linpack (OpenBLAS) |
|-----------------|-----------------|--------------------|
| 1               | 0.63 GFLOPs     | 3.58 GFLOPs        |
| 16              | 7.1 GFLOPs      | 25.1 GFLOPs        |

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
