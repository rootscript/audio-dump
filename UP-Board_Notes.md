#Can the UP-Board be used with Pi2Media 503SPD1 DAC HAT?

[superbestaudiofriends link](http://www.superbestaudiofriends.org/index.php?threads/raspberry-pi-i2s-to-spdif-hat.1990/page-9)

Pi 2 Design, my company, already has a relationship with up-board. They are re-selling our 502SSD Storage Hat. The early versions of the up-board did not have the I2S bus enabled. Not sure why, but that's what they told us after we spent a few hours trying to get our 503DAC1 running. However, we are told the final rev will have it. As soon as we get one we'll test and all our hats will be tested on the up-board.

As for ROON we are currently working with them to add support for our 503HTA Hybrid Tube amp, and will add support for all our audio hats, including 503SPD1 and 2. Of great excitement to us regarding Roon is getting support in place for our up-coming 35W/channel Class-D Amp w/HP out hat. Not Audiophile level, but great for dorm rooms, game rooms, etc.

Cheers,
Michael


[kickstarter comments](https://www.kickstarter.com/projects/802007522/up-intel-x5-z8300-board-in-a-raspberry-pi2-form-fa/comments)

We designed UP to be fully electrically compatible with ANY R-Pi2 HAT expantion boards; we will provide several of this board on future UP-Shop web site after validating hw and sw.

How is UP support of Wake-On-Lan? Does the Ethernet Chipset has an EEPROM or the Chipset is connected to the USB BUS (like USB to Ethernet adapter)?

1G Ethernet is supported full speed cause we use a Ethernet controller on 1x PCIe gen2 lane. The ETH controller is Realtek RTL8111G-CG and support WOL



the schema and layout will not be shared with the community (sorry). We are working together with Intel on RD; the power supply and mem-interface are same as Intel CRB. We will answer to specific hw related questions. There will be a FULL Linux support by Emutex

Does anybody know what graphics chip this board has? What is it equivalent to?
 It is integrated graphic Intel® HD Graphics 12 EU GEN 8, up to 500MHz. 
 
---
##Power:

 What are the dimensions and polarization of the barrel jack?

	The connector type is 5.5mm/2.1mm plug same as Galileo; and power input is 5V@3A.
	UP has 6x USB2 ports and 1x USB3 port so total USB/VBUS max Icc is around 4A, that's why we preferred a JACK and could not use micro-USB as power supply. In case your application wont need all this current then it will be possible to use an USB-to-JACK cable adapter; we will provide some models on UP-shop soon.
 
---

 4K@60 output would be nice. But this would require either DisplayPort 1.2 (or higher) or HDMI 2.0. Does it support 4K@30?
 x5-z8300 doesn't support 4K and only has HDMI1.4b. If we would like to have 4K, we need to change x5-Z8500. So far we also don't see any specification change on x5-z8350 in graphic.
 

 
 is it possible to boot and run the Up board from a USB 3.0 SSD?
 Yes, you can use USB3.0 storage as your booting device.
 
 ---

##Rasberry Pi Pin Compatibility:
 
Hi, as the maintainer for the software for the "LCD display shield" you feature in your product shots, and the designer of some very popular Raspberry Pi HAT products I'd like to know what steps you've made to ensure electrical and functional compatibility with HATs.
I presume you're copying the mechanical layout presumably to take advantage of the existing market, but this potentially causes us makers an extra support burden when our customers use our products with your board. We like to help where we can, and don't tend to turn customers away with "we don't support that", so knowing the pitfalls ahead of time would be preferable.
Looking over your Pinout diagram ( which is unnecessarily cryptic, please orient it vertically and put the labels next to the pins, like: http://pinout.xyz/ ) it looks like the placement and function of key features like I2C, UART and SPI matches the Pi's 40pin header. However there's no telling if things like PCM_CLK will be up to the task of producing, for example, the tightly-timed signal required to drive the WS2812 on the Unicorn HAT.

Thanks for your reminder. It is our goal to provide same pin definition and same electrical characteristic . Actually this is task for these 2 weeks, we are verifying it in every pin. In our community, we will be able to share how every pin works. It may help developers in more efficient way.



Is it possible to get the I2S digital audio signals from the same gpio pins as on the Raspberry Pi? 
PIN 35 - GPIO19 - LRCLOCK 
PIN 40 - GPIO21 - DATA 
PIN 12 - GPIO18 - BITCLOCK
If yes, can 32bit 384khz audio be outputted over this pins?

	Yes,you can access digital audio cross I2S as you do on Rasberry-Pi today.

Do you use integer or fractional clock dividers? I.e. would you be able to support both: 
44.1 KHz - 44.1KHz, 88.2KHz, 176.4KHz, 352.8KHz and 
48 KHz - 48KHz, 96KHz, 192KHz, 384KHz 
audio families over I2S?
Would you be able to output DSD over the same I2S pins? 
BCLK - DSD Clock 
LRCLK - DATA Left 
DATA - DATA Right
If yes UP would be the best audiophile board ever!

Where can I find more information about the CSI bus on this board? 
Is it the same as the Raspberry Pi?

	The CSI connector will be different from Raspberry Pi's as we are following Intel's connector type.

Any word on whether this board will work with the official raspberry pi display that uses the dsi connector?	
The official R-Pi DSI display will not work because we change the connector type to Intel DSI connector. 

---

##OS Support:

In the update we mentioned there will be 3 Linux distribution to be supported .Ubilinux, Ubuntu and Snappy. Unfortunately Red Hat Enterprise is not in the support list.
 
This may be a strange request but would it be possible to install OSX (unofficially) on this board as it is an Intel Based device?

	It is not in our current plans, but if any of you guys is capable to do that pls contact info@up-board.org and we can cooperate

I wanted to ask if it supports Raspberry , to install OpenELEC for a XBMC?
Yes, UP will support KODI. and we plan to build a demo.
We are going to try Kodi on UP , as we believe UP is perfect to be a media center. That's why we design VESA mountable chassis. :-)

How much of the Cherry Trail driver support issues are down to the Kernel version used in the distros? Many distro's are still using a 3.x based Kernel which has limited Cherry Trail support, while Kernel 4.1 onwards appears to be receiving many commits related to the Cherry Trail platform from Intel. These updates aren't backported into the older 3.x series Kernels, so would a change to a 4.x Kernel simplify the amount of work required to support the platform and decrease the number of additional drivers needing to be written?

	We got your points, that's why we can not say we support all Linux distribution. In the beginning , we will target at Ubilinux, Ubuntu, and Snappy. We are considering Yocto, which has kernel version 3.x; however, we still look for partners to develop it.	
Interesting to hear you are considering Yocto. It is a distro I am intending to try running on my UP board when I receive it. I have been playing with the Jethro release candidates and a Celeron 2957U (HP G260) as my target to get to learn the Yocto way of working. 
Now 2.0 is officially released with 3.14, 4.1.8-stable and 4.2 (dev) kernel support I'm hoping it will be a relatively smooth journey to get it to play nicely with the UP board :) 