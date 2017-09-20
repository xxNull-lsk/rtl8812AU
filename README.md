# Rtl8812AU Realtek 802.11ac Linux Driver (rtl8812au)

This driver is an update to version 5.1.5 (rtl8812AU_linux_v5.1.5_19247.20160830) of Realtek's 8812AU USB WiFi Linux driver for AC1200 (801.11ac) adapters. 

It supports supports USB 3.0 and has been succesfully tested to work with *Linux Kernels 3.16.x to 4.12.x* as well as AMD's Radeon Open Compute (ROCm) kernel.

The original version of this driver was downloaded from [Tenda](http://www.tenda.com.cn/download/detail-2614.html).  However, several improvements have been made including support for the Tp-Link Archer and Tenda U12 dongles as well as THE addition of an [LED control module (rtw_led_ctrl)](https://github.com/xxNull-lsk/rtl8812AU/pull/6#issuecomment-3261505020).


# Supported Device List

From driver's device USB ID list and independent testers:

| D-Link		 | Edimax			| Others		 | Others 			  | Others |
-----------------|------------------|----------------|--------------------|----------------------------------------|
| ALPHA			 | I-O DATA Edimax  | HAWKING Edimax |  EnGenius EnGenius | Belkin Sercomm 
| DWA-182  		 | Logitec Edimax   | ASUS Edimax  	 | 	Phlanex Abocom    | Tenda U12
| Cameo			 | Edimax Edimax  	| NEC *  		 |  Abocom Abocom     | Tp-Link Archer: T4U v1, T4U v2, T4UH V1
| 		  		 | Sitecom Edimax	| ZyXEL *		 |  WD Cybertan 	  | BrosTrend Long Range 1200Mbps     


## Enviroments Tested In
* Ubuntu 14.04 and 16.04
* Fedora 25
* Kernels
	* 3.16.x to 4.12.x
	* AMD ROCm Linux Kernel: 4.11.0-kfd-compute-rocm-rel-1.6-148


## Building (How to Install)

To build and install module manually:

```
$ make
$ sudo make install
$ sudo modprobe -a 8812au
```

To use dkms install:

``` 
$ sudo make -f Makefile.dkms install
```

### Additional Info
You may have to install additional packages to complete the build:
``` 
$ sudo apt-get install build-essential
$ sudo apt-get install linux-headers-4.4.0-67-generic #Change "4.4.0-67" to your desired kernel version
```