# Rtl8812AU Realtek 802.11ac Linux Driver(rtl8812au)

This driver is an update of version 5.1.5 (rtl8812AU_linux_v5.1.5_19247.20160830) of the RealTek 8812AU USB WiFi Linux driver for AC1200 (801.11ac) adapters. 

It supports supports USB 3.0 and has been succesfully tested to work with Linux Kernels 3.16.x to 4.12.x as well as AMD's Radeon Open Compute (ROCm) kernel.

The original version of this driver was downloaded from [Tenda](http://www.tenda.com.cn/download/detail-2614.html).  However, several improvements have been made including the addition of a rtw_led_ctrl module parameter. This allows setting the led to blink normally or stay in an always on or off state.


# Supported Device List
This list is from the source USB IDs:
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

Tested by [@codesport](https://github.com/codesport):
+ BrosTrend Long Range 1200Mbps

# My Modifications
- Added support for Tenda U12.

## Tested On
Ubuntu 14.04 and 16.04
Fedora 25
Kernels
** 3.16.x to 4.12.x
** AMD ROCm Linux Kernel: 4.11.0-kfd-compute-rocm-rel-1.6-148

## Building (How to Install)

To build and install module manually:

``` sh
# make
# sudo make install
# sudo modprobe -a 8812au
```

To use dkms install:

``` sh
$ sudo make -f Makefile.dkms install
```

## Something else
You may have to install additional packages to build it
``` sh
$ sudo apt-get install build-essential
$ sudo apt-get install linux-headers-4.4.0-67-generic #Change "4.4.0-67" to your desired kernel version
```