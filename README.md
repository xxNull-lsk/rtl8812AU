# Rtl8812AU
Downloaded from [Realtek](http://ftp3.realtek.com.tw/Linux/WIFI/USB/)
Version RTL8812AU_linux_v5.2.9_22809.20170621

Supports USB 3.0

# Support Device List
This list is from the source USB IDS
+ Belkin sercomm  
+ D-Link ALPHA  
+ Edimax Edimax  
+ Sitecom Edimax  
+ I-O DATA Edimax  
+ Logitec Edimax  
+ NEC *  
+ ASUS Edimax  
+ HAWKINGEdimax  
+ ZyXEL *  
+ D-Link ALPHA  
+ WD Cybertan  
+ EnGenius EnGenius  
+ Phlanex Abocom
+ Abocom Abocom
+ D-Link Cameo
+ Tp-Link Archer T4U v1, T4U v2, T4UH V1

This List is from WebSite:
+ D-Link DWA-182

# My Modifications
- Support Tenda U12.

## Test
Ubuntu 14.04&16.04

Fedora 25

Kernel 3.16.x--4.12.x

## Build
``` sh
# make
# sudo make install
# sudo modprobe -a 8812au
```

## DKMS

``` sh
# sudo make -f Makefile.dkms install
```

## Something else
You may have to install some additional packages to build it.
``` sh
# sudo apt-get install build-essential
# sudo apt-get install linux-headers-4.4.0-67-generic
```
Change 4.4.0-67 to your kernel version.
