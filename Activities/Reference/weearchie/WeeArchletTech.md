Wee Archlet
===========

Wee Archlet is the home-build cluster setup developed for demonstration purposes using
the Raspberry Pi series of single board computers.

Instructions on equipment and setup are available at (https://epcced.github.io/wee_archlet/)
 

Wee Archlet Technical Specification:
----------------------------------------

### Total Numbers

-   Number of Processors/Cores: 5/20

-   Core Speed: 1GHZ

-   RAM: 5 GB (1GB per board)

-   Storage: 80 GB (16 GB per board)

-   Operating System: Raspbian “Jessie"

 

### Components

Wee Archlet is housed in plastic 'Lego-style' casings.

The power and computation elements are:

-   5 Raspberry Pi 3 Model B

-   1 Netgear GS108 Switch


### Raspberry Pi 3 Model B Specification

-   Quad Core 1.2GHz Broadcom BCM2837 64bit CPU

-   1GB RAM

-   BCM43438 wireless LAN and Bluetooth Low Energy (BLE) on board

-   40-pin extended GPIO

-   4 USB 2 ports

-   Micro SD (16GB Cards in use)

-   Ethernet Port

 

The Raspberry Pi 3 units in Wee Archlet has been under clocked to 1GHz after
testing against applications including using OpenBLAS proved this to give stable
performance without power or heating issues in the cases. Each unit has a 16GB
MicroSD card with the operating system installed.

 

### Netgear GS108 Switch

-   Speed: 10/100/1000Mbps Ethernet

-   8 Ports with Auto-uplink negotiation

-   Max Power Consumption: 4.9W

 
The switches used in Wee Archlet are off-the-shelf Netgear units. The
Raspberry Pi network communications are well within the tolerances of the
switches and the power consumption is low. The switch has a 5V power
supply.

