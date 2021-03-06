---
layout: post
title: "How to recover from Grub Rescue"
date:  2016-08-23 19:42:42 +05:30
categories: Linux
---

If you are new to Linux and have just installed it, or even if you have used it for a while, there may come a time when something as silly as accidentally unplugging the power adapter from your laptop while updating it can cause the Boot loader to go kaput.

So, when you now try to boot the dreaded Grub Rescue screen shall appear. Many people if they have recently installed any of the distro of linux simply reinstall it, trust me i did the same earlier.

But in many cases you would have updated few things, installed a few softwares or even written few lines of code which now cannot be recovered if you were to format.

Ideally, i prefer to use a Bootable CD/DVD to install Linux distributions instead of an USB. So all you need to do to fix this is:

* Insert the bootable CD/DVD/USB and boot from it. Though you may have to change the BIOS setting depending on the choice of device you make
* Once the boot is completed you'll have 2 options: Install or Try
* Choose TRY.
* Open Terminal and type in the following commands
    * sudo add-apt-repository ppa:yannubuntu/boot-repair
    * sudo apt-get update
    * sudo apt-get install -y boot-repair && boot-repair
* Once this finishes executing, select *Recommended Repair* and click *YES* when it asks.
* Restart the system and remove the device(CD/DVD/USB)

