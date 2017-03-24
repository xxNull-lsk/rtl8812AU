# Rtl8812AU
Download from[Tenda](http://www.tenda.com.cn/download/detail-2614.html)  
Version rtl8812AU_linux_v5.1.5_19247.20160830

Support USB 3.0

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

This List is from WebSite:
+ D-Link DWA-182

# My Modifications
- Support Tenda U12.

## Test
Ubuntu 14.04&16.04
Kernel 3.16.x~4.4.x

## Build
``` sh
# make
# sudo make install
# sudo modpro -a 8812au
```

## Something else
Maybe you should install some packet to build it.
``` sh
# sudo apt-get install build-essential
# sudo apt-get install linux-headers-4.4.0-67-generic
```
Change 4.4.0-67 to your kernel version.
