# Rtl8812AU Realtek 802.11ac Linux Driver(rtl8812au)

This driver is an update to version 5.1.5 (rtl8812AU_linux_v5.1.5_19247.20160830) of RealTek's 8812AU USB WiFi Linux driver for AC1200 (801.11ac) adapters. 

It supports supports USB 3.0 and has been succesfully tested to work with *Linux Kernels 3.16.x to 4.12.x* as well as AMD's Radeon Open Compute (ROCm) kernel.

The original version of this driver was downloaded from [Tenda](http://www.tenda.com.cn/download/detail-2614.html).  However, several improvements have been made including support for the Tenda U12 and the addition of a rtw_led_ctrl module parameter.


# Supported Device List

From driver's device USB ID list and independent testers:

| - | - | - | - | - |
-----------------|------------------|----------------|--------------------|----------------------------------------|
| Belkin Sercomm | I-O DATA Edimax  | HAWKING Edimax |  EnGenius EnGenius | Tp-Link Archer: T4U v1, T4U v2, T4UH V1
| D-Link ALPHA   | Logitec Edimax   | ZyXEL * 		 | 	Phlanex Abocom    | D-Link DWA-182
| Edimax Edimax  | NEC *  			| D-Link ALPHA   |  Abocom Abocom     | BrosTrend Long Range 1200Mbps
| Sitecom Edimax | ASUS Edimax      | WD Cybertan    |  D-Link Cameo


New Device Support Added by [@xxNull-lsk](https://github.com/xxNull-lsk):
* Tenda U12


## Enviroments Tested In
* Ubuntu 14.04 and 16.04
* Fedora 25
* Kernels
	* 3.16.x to 4.12.x
	* AMD ROCm Linux Kernel: 4.11.0-kfd-compute-rocm-rel-1.6-148


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

### Additional Info
You may have to install additional packages to complete the build:
``` sh
$ sudo apt-get install build-essential
$ sudo apt-get install linux-headers-4.4.0-67-generic #Change "4.4.0-67" to your desired kernel version
```