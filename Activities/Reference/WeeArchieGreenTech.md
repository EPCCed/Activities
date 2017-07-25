Wee Archie Green
===============

Wee Archie Green was the first unit developed for demonstration purposes using
the Raspberry Pi series of single board computers.

 

Wee Archie Green Technical Specification:
----------------------------------------

### Total Numbers

-   Number of Processors/Cores: 18/72

-   Core Speed: 900MHZ

-   RAM: 18 GB (1GB per board)

-   Storage: 144 GB (8 GB)

-   Operating System: Raspbian “Wheezy"

 

### Components

Wee Archie Green is housed in an extruded aluminium frame with polycarbonate
facings and mounts.

The power and computation elements are:

-   18 Raspberry Pi 2 Model B

-   3 Netgear GS108 Switch

-   18 8x8 LED Matrices

-   2 5V 10A PSU

-    

### Raspberry Pi 3 Model B Specification

-   900MHz quad-core ARM Cortex-A7 CPU

-   1GB RAM

-   40-pin extended GPIO

-   4 USB 2 ports

-   Micro SD (8GB Cards in use)

-   Ethernet Port

 
Each unit has a 8GB MicroSD card with the operating system installed.

 

### Netgear GS108 Switch

-   Speed: 10/100/1000Mbps Ethernet

-   8 Ports with Auto-uplink negotiation

-   Max Power Consumption: 4.9W

 

The switches used in Wee Archie Green are off-the-shelf Netgear units. The
Raspberry Pi network communications are well within the tolerances of the
switches and the power consumption is low. Each switch has its own 5V power
supply.

 
### 8x8 LED Matrix

-   I2C Communications

-   64 Element Dot Matrix Display

-   Blue colour

 

The LED Matrices are used to give information on the status of a Raspberry Pi,
including core usage, network traffic and temperature.

 

Wee Archie Green Performance
---------------------------

The performance of Wee Archie Green was assessed using the Linpack benchmark
(<http://www.netlib.org/benchmark/hpl/>). For more detailed information on the
performance of Wee Archie Green, there is a blog article available on the EPCC
blog (<https://www.epcc.ed.ac.uk/blog/2017/06/07/linpack-and-blas-wee-archie>).

For a single node (Raspberry Pi) using the standard ATLAS BLAS implementation on
Raspbian, the peak performance attained was 1.03 GFLOPS.  As detailed in the
blog linked above, this caused some queries to be raised and OpenBLAS was
complied for the Raspberry Pi 2. The performance using OpenBLAS in Linpack
caused a large increased to 1.57 GFLOPs.

For Wee Archie Green as a whole, the performance was assessed on 16 compute nodes
(16 of the Raspberry Pis with the remaining two managing the network and file
system). Using the ATLAS implementation the peak performance was 9.1 GFLOPs,
again causing concern. Then rerunning the benchmark using OpenBLAS this
increased to 12.79 GFLOPs.

These scores are not particularly impressive, but the focus of the machine is to
demonstrate how parallelism and supercomputers work not replicate the
performance. Though in the first ever top500 list, Wee Archie Green would have
been number 21. And it consumes a lot less power and takes up less space.

| Number of Nodes | Linpack (ATLAS) | Linpack (OpenBLAS) |
|-----------------|-----------------|--------------------|
| 1               | 1.03 GFLOPs     | 1.67 GFLOPs        |
| 16              | 9.1 GFLOPs      | 12.79 GFLOPs        |
