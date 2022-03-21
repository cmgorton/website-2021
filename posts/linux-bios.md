---
title: Root to Linux, BIOS
description: Learn how to use BIOS
date: 2021-11-04
tags:
  - posts
layout: layouts/post.njk
---

At Forem a few coworkers and I have formed a Linux Club🤓. 
[Joe Doss](https://twitter.com/jdoss) is leading us on this adventure into Linux.  
The adventure starts by working through the [Gentoo Handbook](https://wiki.gentoo.org/wiki/Handbook:AMD64) and installing Gentoo(a distribution of Linux) on Lenovo ThinkPads. 

During our meetings, I have been [taking notes](https://github.com/cmgorton/linuxclub_notes). These notes are useful for people in our club. 
I am writing this series to take what we have learned and share with a broader audience outside of the club. 

One of the first things we did when we got our laptops was set up our BIOS. 

This post will give a brief description of what BIOS is, how to navigate to it, and some of the common settings you might change. 

## What is BIOS?
BIOS or Basic Input/Output System is a small piece of code that lives in a “read only” chip on your system board(motherboard). 
It controls low level/basic functions of a computer.

**Note:**  read-only means that a file can be opened or read but can't be deleted or renamed. 

The BIOS will identify, test, and configure your computer's hardware. It will also connect it to your OS. 

This is called the BOOT process. 

## Navigating to the BIOS
The first software that runs on your computer is the BIOS. 
As you start your computer you may see a prompt that says `f2 = Setup`.

This prompt will give you access to the BIOS setup utility. This is sometimes referred to as the Setup System. 
Other keys that can invoke BIOS depending on your computer are F1, F10, F12, Del, or Esc.

## Setting up your BIOS
In general you should leave your BIOS settings as the default settings. 

When you set up your own Linux distribution you may need to change a few settings. You can also change settings to have more control over your hardware. 

### Common Settings in BIOS
**BOOT Priority Order**
One common setting you can change is the BOOT Priority Order. 

This is a priority list that tells your computer which operating system to boot from. 
After the BIOS tests your hard drive it will check for a “bootable” drive. 
This is where tell your computer to use a Linux distribution to boot. 

The default BOOT Priority Order looks for your computer's OS. On our ThinkPads this was Windows 10. 
Our goal was to boot Gentoo instead of Windows 10. 

First, we downloaded Gentoo to a USB drive. Next, we changed the BOOT Priority Order to use our USB as the top priority. This meant our computer will look for our USB to boot up Gentoo instead of the ThinkPad's default OS.


**Secure Boot**
> **Note:** Secure Boot is technically a feature of UEFI and not legacy BIOS. 
Look at the image at the top of this post that shows our ThinkPad specs. You can see it mentions the computers UEFI BIOS version.

Secure Boot can help a computer resist attacks and infection from malware. You can find the setting for Secure Boot in the `Security` tab.

Typically, you want to keep this setting set to on. We disabled this setting because it prevents non-Microsoft OS's from working. 

**Date/Time**
You can update your systems data and time in the `Main` tab. We updated the date and time in our BIOS to reflect our timezones and correct day, month, and year. 

There are many other settings in BIOS that you can change. These are the common ones we updated.
 
## Save and Exit BIOS
To Exit out of the BIOS navigate to the Restart tab and choose `Exit Saving Changes`.
Or you can exit and save by pressing `F10`.

## A Shift to UEFI
BIOS has a long history but there has been a shift away from using it. 

Companies like Intel are phasing out BIOS in favor of the Unified Extensible Firmware Interface(UEFI) I mentioned in the Secure Boot section. 

UEFI is a lightweight BIOS alternative and newer computers are shipped with it. It has several advantages over the traditional BIOS. This post won't cover everything about UEFI but some of the advantages of UEFI are:
- it can boot from drives of 2TB or greater. 
- it has more access to [addressable space](https://searchstorage.techtarget.com/definition/address-space). The BIOS is limited to 1MB. 
- it has a user-friendly interface. Unlike the BIOS, you can navigate it with a mouse. 
- it ships with security features like Secure Boot.
