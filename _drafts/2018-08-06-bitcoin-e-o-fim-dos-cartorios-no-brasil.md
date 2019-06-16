---
title: "Mac Mini Memory Upgrade"
date: 2013-05-26
modified: 2018-09-08T12:04:00-03:00
categories:
  - Tech
tags:
  - mac-mini
  - apple
---

**Watch out!** I no longer use a Mac Mini or Apple's products since I migrated to a Linux Notebook in 2013 due to the evolution of the Linux Desktop in the last years.
{: .notice--info}

If you are thinking to buy a Mac Mini or a Mac in general, I'm telling you, doesn't worth to buy it with more memory then the standard. You can find cheaper memories right there.

## Which memory to buy?
			
The Mac Mini (Mid 2011) uses notebook memories. So you ask me: Can I use generals notebook's memories like the Kingston's Valued Ram for example? Well, Apple has some specifications for memories. For the Mac Mini (Mid 2011) these specifications are:

* C3-10600 DDR3
* Unbuffered
* Non-parity
* 204-pin module
* 1333 MHz

Despite I read some people saying that they had no problem using general memory I prefer not to risk. It's because Apple's compatible memories can't have the resources bellow:

* Registers or buffers
* PLLs
* ECC
* Parity
* EDO RAM

Some generals memories brings these resources and this can cause compatibility problems. A lot of manufacturers follows Apple's specifications: Kingston, OWC, Corsair, etc. Despite being more expensive then their own general memories it's a lot more cheaper then Apple's memories.

I bought the Kingston's KTA series (KTA-MB1333/4G) which is Kingston's memories for Apple products.

Mac Mini (Mid 2011) accepts a pair of 1 GB, 2 GB, or 4 GB memory modules. The maximum memory is 8GB (4GB each slot). I would like to say to use both slots to take the benefits of Dual Channel.

## The installation trouble

The access to the memories is pretty simple, just rotate the bottom cover counterclockwise to the unlocked position. I don't need to say that power cord and other cables should be disconnected from the Mac Mini, right? Apple has a very illustrated guid of [how to remove or install Mac Mini memories](http://support.apple.com/kb/ht4432).

Well, after changing the memories and power on the machine I got the famous memories's beeps error. I froze up. Two things could have happened: I broke the memories or they came broken. For my happiness: none of them.

![Open Mac Mini](/assets/images/memoria-mac-mini.jpg)

I placed back the originals memories sticks and the problem continues going (I don't remember if I placed them in the same order). I started testing the memories slots with the originals and the new sticks. I observed that at upper slot both (new and originals) sticks works, the problem was the down slot.

## The solution

* I left the down slot alone, placed the **new** stick at upper slot and power on. At the login screen I turned it off;
* Turned it on again and before the gray screen appears (you need to be a little fast), I hold the keys <code>Command (⌘) + Option + R + P</code> simultaneously (yes, simultaneously means at the same time);
* Hold the keys down until the computer restarts and you hear the startup sound for the second time.
* At the startup screen I turned it off again, removed power cord and all others cables, placed the other new memory stick at down slot and waited more 15 seconds before replug everything and power on the machine again.
* For my happiness everything works again \o/

All of this is a [NVRAM/PRAM reset](http://support.apple.com/kb/HT1379) and a [SMC reset](http://support.apple.com/kb/HT3964) both of them explained at Apple's site.

## Conclusion

The Mac OS X (Mountain Lion) has an extraordinary memory management. The system worked perfectly with the standard 2GB of memory (Mac Mini mid 2011), with 8GB the machine flies. For me the Mac Mini with 8GB is the best personal computer you can have (at least in my country where a Mac Mini costs about US$ 1.000 because of taxes and, of course, Apple's hungry for profits). It has a nice cost x benefit relation: It's not so expensive as an Apple's notebook (again, here an Apple machine can take you to ruin), has an extraordinary hardware, its quiet, compact and comes with an unique OS: the stability and secure of linux without you have to give an eye to take something to work and the beauty and ease very, very, very... (write this a thousand times) superior to Windows. I use the Mac Mini for desktop and the iPad and Android Smartphone for mobility.

![Mac Mini Fusion 5](/assets/images/excel-fusion.jpg)

When I migrated to Mac I really, really though to go back to Windows, I will not deny. And this was because one thing: The MS Office. There is no such thing as Excel yet. For the other MS Office tools there is an alternative better and cheaper. The MS Office and the games are still the Microsoft's joker. But now, with 8GB ram and the Office 2013 running inside BootCamp with Fusion 5 virtualization there is nothing that make me want to go back to a pure Windows computer solution.
