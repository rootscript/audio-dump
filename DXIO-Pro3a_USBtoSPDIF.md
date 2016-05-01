##DXIO Pro3a (from DIYinhk) an external DDC.

[link](http://www.diyinhk.com/shop/audio-kits/54-xmos-192khz-high-quality-usb-to-spdif-with-ultralow-noise-1uv-regulator-wauto-power-switch.html)

A good DDC is always key to a good sounding system.

###Out of stock, waiting for NEW version

DIYINHK will not make the Pro3a any more from what I understand from them. They wrote to me  in an e-mail that within about two months they will have a new and improved converter. 6th-March-2016
We should have a new usb to spdif converter based on the new 16 core xmos chip. I hope it can be available in two month.

###Using a linear power supply with the Pro3a?
 
you'll get the best results... but on usb power it's good. if your usb is super clean power than it should be great!
 
- but most people have 20mV noise on their USB line. that's...uhm. bad.

- low noise psu's like Corsair are around 8-12mV, and thats "acceptable"
 
- cheapo linear psu's like Teradak dc30w are around 1mV which is "good"
 
- high end PSUs like Paul Hynes, IFI iUSB 3.0, Mojo, and obviously the Uptone Audio JS-2 will have ultra low noise from .1uV - 40uV

**Notes:**
Anything in the low microvolt range is excellent.
the Pro3a has regulators that are 1uV so it cleans up most of the signal, so feeding it something from a teradak dc30w is usually ideal and will be sufficient for near max performance.
definitely cheapest route.

I'm going to add a belleson regulator to my Teradak DC30w to get 5uV noise output.  I'm installing a SPJ17 5V regulator. down side is that i'm going to be limited to 5V if I use that regulator. thats ok, I considered using it only for 5V anyhow.  The DC30w is awesome since you can easily switch voltage by opening it up and using the adjustment screw to change voltage. use a voltmeter to verify.

The regulators on board the Pro3a are quite good, rated for 1uV of noise.
The NDK's are pretty much the best oscillator all around. They are infamously hard to solder NDK oscillators, but are audibly the best oscillator, especially in the bass region; the crystek957's are really similar and about as good, just a little different.

**Links:**
[link](http://www.belleson.com/order.php)
SPJ High Current 2A Superpower (SPJ17 Positive Vout LM317/LM1117 pinout - 5V Vout) $59

Ask the ebay seller for a DC30W set for 5V output and ask for a DC cable that is 2.5mm inner and 5.5mm outer.

Q: What do you think about making a linear regulated power supply from one of these?
[link](http://www.diyinhk.com/shop/audio-kits/89-08uv-ultralow-noise-dac-power-supply-regulator-3357v-15ax2.html)

A1: The DIYinHK ultra low noise PS is good - but I think the DC iPurifier may make it unnecessary, certainly if your using a Regen as well. This unit works great with the TeraDak Linear Power Supplies.
[link](http://ifi-audio.com/portfolio-view/accessory-dcipurifier/)
 With trickle-down technology from Abbingdon Music Research (AMR), the very latest product from iFi is the DC iPurifier; a noise-cancellation product aimed to enhance the existing, ubiquitous Switch Mode Power Supply (SMPS).
Generic SMPS designs are very noisy because they were never intended for audiophile applications.

---

[link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/210#post_12458706)
Q: Bob, any thoughts on the Teradak Bladelius vs. DC-30 Touch?  Is the Bladelius new?

I started a thread on the DIY board just to see what happens:
 
http://www.head-fi.org/t/803109/looking-to-make-a-linear-regulated-5-volt-power-supply-suggestions-please#post_12458576
 
Bladelius
http://www.ebay.com/itm/TeraDak-BLADELIUS-USB-DAC-power-source-5V-3A-Linear-Power-Supply-/262057568111?hash=item3d03d9276f:g:lMoAAOSwFnFV~r35

DC-30W-Touch
http://www.ebay.com/itm/NEW-TeraDak-DC-30W-TOUCH-DC5V-3A-Linear-precision-linear-regulated-power-supply-/301773952382?hash=item464321157e:g:EnkAAOSwfcVUI5XK

A1: I have both and prefer the DC-30W Touch with the large Pannie Caps - I have new HWs to put in but just haven't had time.  They are very close to each other.  Hoping the new low cost Uptone PS will be good.  At $130 for the DC-30W with a $90 DC iPurifier - not a bad pairing.  Cerious has been MIA - too bad really great power cords.  Many others to choose from.  I would add a great AC line conditioner before the LPS.

So the power has been well filtered and corrected, the digital gear isolated on independent AC filters -  even before the power enters the TeraDak DC-30W.  Then the power goes through three layers of low noise regulation (DC iPur, Regen, iPur 2.0) - before powering the DDC.  The benefits extend to the DAC as well - isolated AC from DDC - power filtered and corrected by the aR1p and PB4X4Pro - also using a Cerious Tech Graphene power cord.  This may all seem obsessive - but each step has done amazing things for the sound quality.  Not just smoothness and musicality, but the greater clarity, detail and imaging focus, deeper better defined bass, wide deeper soundstaging.  The results have been truly outstanding.

---


###Intona USB isolator
To be frank, most dac's today have horrid USB inputs. most suffer from 8khz packet noise.
The only product i've found to remove this issue entirely is the Intona USB Isolator. 
I've sold all my jitterbugs, uptone regen, reclockers etc... none compare.
I'm now using the intona that feeds into my modded DIU8 w/ NDK oscillators.. from there the clock is sent out through HDMI i2s directly into my M11 which has the PLL turned off.
The intona isolates ground from power AND data at full high speed 480mbps usb. Not even the ifi iusb3.0 does this. Albeit the noise level is less on the ifi iusb3.0
The intona isn't bad at 40-60uV.
I have the intona to isolate and basically I don't need the fancy USB or powered usb anymore. I found that it works quite well on normal USB ports if I'm using the intona! since it reclocks, isolates power and data! and also outputs ultra low noise-  once it gets to my DDC (ground isolated as well) the signal is pure with no packet noise and then is clocked by the NDK's and sent out through HDMi i2s directly to my pcm1704uk's that pickup the clock from the ndk's. the sound is stellar imho.  :)
[link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/120#post_12420917)

The Intona USB isolator is pricey, but does wonders for many people with dirty power, mediocre usb etc. It will make your gear sound it's best.
I chose the industrial version as it apparently is slightly more compatible with more usb modules. Some require power and there is a limit to how much the intona will provide after it powers itself. I think it's still likely to support nearly 100%, but some devices need over 400mA and that might be a problem. usb max is 500mA but rarely does an audio device module use that.
**And which Intona would you get? Industrial version???! Or standard?**
Both are good but the owner highly recommended the industrial Version.
[link](http://intona.eu/en/products)
343 Euros for the Industrial version.

Other USB isolators:
Only two other devices exist that do this at true high speed 480mbps, low latency and no packet noise.
The Intona is a bit quieter than the Aqvox actually. likely better with transients and psrr too. but either way, not a HUGE difference...just notable. possibly audible.

- The Aqvox is around .1mV  (100uV)

- The Intona around 40uV

The only other one worth talking about is the Mutec Mc-3 + usb - which is on par with the intona...except price is over double!!! [link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/120#post_12422348)

BUT consider the intona. it's not hype.  I've tested in on 4-5 diff peoples setups and all of them were blown away with the results. It's a fantastic piece of gear to own.Think of it as the holy grail for making USB function as though it should have this whole time.  The thing manufacturers leave out is the critical plagued issue of usb's packet noise issue of 8khz spikes. It's truly bad for about 99% of usb implementations for audio. The intona may very well have the lowest packet noise of any device.. around -142dB for 8khz noise. compared to the average of -110dB or a fancy fiber optic usb cable can bring the noise down to around -118dB but not even close to what the intona does.
 
I recommend the Intona over any device of its kind. Which are USB cleaners, reclocker , regen, isolators for power. But this intona is one of about 2 or three products that does isolation of the USB data. It uses two Spartan fpga' to break down and rebuild the data from the dirty to clean side.it's a great piece of gear to own if you use USB at all. Simply put, it will give you the most out of your USB.
I have owned everything you can imagine from the Uptone regen, jitterbug, wyrd, etc etc. sold all of them except r wyrd, which is what my wife uses on her setup. Her psu in the computer had a noisy 5v USB line that is around 15mV-20mV
My psu is about 7-9mV and too noisey for me. That's why I got the dedicated Paul Hynes lps for the Paul pang ocxo v3 usb3.0 card... I could of saved a grip of money if I just got the intona. As it lets regular USB ports sound 98-99% as good as with the ppa3 ocxo and Hynes lps. Kinda frustrating. But true.

Q: As I understand, the intona is for galvanic isolation?
SPDIF is a good galvanic decoupler.
I think that with a SPDIF dac, the intona would be overkill

A1: SO..... SPDIF in general? or are you specifically talking about Toslink, as digital rca/coax is not good for galvanic isolation.
The intona does more than power isolation, it does data. and not just 12mpbs galvanic isolation of data, but full 480mpbs galavanic isolation. ON TOP of it all, it removes the horrible 8khz packet noise of usb. 99% of usb suffers from this problem. 
 It's simply not overkill and not even comparable to Toslink.

Q2:If I understand you right, with the Intona before my ddc I will not need anything else in the chain between pc and ddc?
I can remove that Aqvox usb psu?
It´s feeding the ddc with cleaner power.
Maybe later buy a better 19v linear psu to my Intel NUC, or is that also overkill with the Intona in the chain? [link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/240#post_12477777)

A2: I have the industrial version intona. The USB plugs are high retention and potentially are less resistance. Also the manufacturer stated the industrial version is most compatible with dacs compared to the standard version. It outputs slightly more power than the standard version.
In my tests it's made the most difference on laptops and low end pc's or average spec builds. As most pc's have horrid psu's as well as most Macs too. Ripple is quite high from 15-30mV even!
And experiment with you Acvox. I don't know. Try with and without. Buts it's likely you won't need all the clutter IMHO. I personally wouldn't add anything after the intona. Everything I tried just made sound quality to suffer. Jitterbug, wyrd, regen etc. and I just use supra USB cable now. The LH labs 2g dual didn't make enough difference to justify try price. Basically about the same yet takes twice as many USB ports.
And there are other isolation options that do data and power... Now, but few I would trust to eliminate the 8khz packet noise. As that's really the main reason I keep the intona in my setup. That alone is worth t and makes USB worth using.


###Best bang for buck USB cable
The supra sets the bar high for any USB cable imho. The best bang for buck without question.

A USB cable shouldn't cost much. If you have a nice cheap cable that is properly built like a supra then it will be as good or better than all the fancy dual ones like LH labs 10g or 2g. I've tested the 10g quite a bit, and own a 2g for some reason. I should sell it since I actually use supra cables currently. Fancy USB cables is not the answer. Likely you are having noise spikes in 8khz and 16khz from the USB port itself.
Again... I've mentioned the average PC has noisy data packets at 8khz and measured around -110dB. The intona nearly elimates it around -145dB or so. Problem is USB itself, most devices have the noisy data packet issue... I wouldn't doubt 95% or more are at least a little noisy. And most are very noisy. Hence why people prefer coax, bnc, optical etc. but USB could be better if its implemented correctly.

I used HDMI yet still have a DDC that starts with the USB input. I'm using the intona and have an improvement even with my fancy Paul Hynes linear psu , Paul pang v3 ocxo USB 3.0 card. It's crazy it still helps... Simply due to its ability to get rid of the noisey data packets.
I have the ifi ipurifier2 and ifi DC purifier and they don't work as well as the intona. For whatever it's worth.

They do work well though. If you want to get better power than what your linear psu is doing, add a ifi DC purifier in the mix. But it won't fix USB data noise.
The I purifier2 should help though, doesn't seem to be quite as effective though.

###Decent Toslink cable
Optical is a crapshoot depending on if you have good toslink from toshiba i believe...and only one cable i'd recommend. a Lifatec Silflex - real glass fiber (470strands) [link](http://www.lifatec.com/toslink2.html)
This cable surely made Toslink sound it's best. but both coax and toslink have their advantages and disadvantages.
 
I would stick to coax personally...some say Toslink if you have grounding issues. I would definitely try both and see what sounds better to you.

###Things to not waste time on
Modifying audio Clocks
Clocks will all sound pretty much the same if you your power source is crap. If the source is ultra clean the the higher performance clocks will sound audibly better.
Otherwise don't waste your time and money.

I remember our member pakultra replaced both audio clocks of his U12 with NDK NZ2520SD 3.3V, he mentioned there was acoustic difference after the modification, but the playback difference wasn't day and night.
I have a pretty old Meridian 500 CD transport, I've done load of modification on it, and I consider replacing it's audio clock would be the very last modification I should carry out for it. So I replaced it with an OCXO, and feed the OCXO with an external linear power supply. I could clearly hear the acoustic playback difference is huge.
I'm so sure, replace my CD transport's audio clock with NDK NZ2520SD 3.3V would also bring out huge playback differences, but I couldn't handle the size of NDK NZ2520SD 3.3V, so I opted for OCXO.
I would take a look on the Value of Accuracy and Phase Noise of both old and new clocks before I start the mod job. If the value differences are not considered as significant, then I would put it on pending and think twice.

NDK's are available at [diyinhk](http://www.diyinhk.com/shop/audio-kits/35-ndk-nz2520sd-20ppm-ultra-low-phase-noise-oscillator.html#/frequency-22_5792mhz):
 12mHz for USB cost $6 other frequencies cost $8
 
NDK's are by far the best option. clearly when comparing to Crystek.
 the low end all the way to 1000Hz are quite important as no other clocks come close to this performance. -13dB less for 10Hz is very significant, and this is comparing to an already stellar performance crystek!  NDK's are definitely the best option. And as you said, the cost difference is also a factor. this is a no brainer if you were designing a DDC the choice would would be NDK. 


Finally got around to modding a Breeze DUU8 with crystek 957's. And it sounds fantastic. I want to spend a little more time and compare with my AGD DIU8 with NDK's but it's really damn close. Surely a nice bump in SQ over the stock JYEC gold clocks. Those obviously have inflated specs. The soundstage on the breeze is surely improved and a touch more bass texture/control yet a touch on the high end of clarity with no hints of distortion. 
 
This mod went quite well. Here are a few photos of the process.
[link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/210#post_12466504)

---

###Others

So around lets say $200-250 range, what ready made SPDIF converters are there that significantly beat the MX-U8, preferably have a silver case and also provide AES?

I'm not sure since I didn't buy any DDC's since I sold my MX-U8, but rb2013 was very impressed by his Breeze DU-U8 in stock version (over at the U12 thread).

[link](http://www.head-fi.org/t/797881/ddc-digital-usb-interfaces-xmos-or-amanero-combo384-based-raspberry-pi-hifiberry-dac-pro-reviews-comparison-modifications-and-usb-audio-in-general/165#post_12439865)
Just popping in here for a moment - as I see I was mentioned.  Been doing much experimentation and I have to say the Yellowtec PUC2 Lite well fed is the clear winner.  It is AES only - I use a Canare AES to SPDIF adpater with 10dB attenuation. 
Now here is the feeding process - The PUC2 Lite only takes it's power from the USB power.  So I have it fed by a Regen (which has it's own ultra low noise regulators, reclocking, etc..) the Regen is fed by a TeraDak DC-30W/Cerious Graphene Xtreme PC/PB4X4Pro dedicated common and differential AC line isolator and filter.
But here is the magic part that took me weeks to nail down.  Using the excellent iFi DC Purifier between the DC-30W LPS (set to 7VDC) and the Regen.  This nifty little unit works wonders!   Now the Regen is being fed ultra low noise linear power - then the Regen's ultra low noise regulators clean it further - that power and signal is sent to the PUC2 lite...but with one additional step.... [link to iFi DC Purifier](http://ifi-audio.com/portfolio-view/accessory-dcipurifier/)

Between the Regen and the Puc2 lite a iFi Purifier2!  Another leap in SQ!  Further noise filtering (both power and data), SI improvement, reclocking, and impedance matching.  Since the Purifier2 reclocks - it's clocks are being fed ultra clean, low noise power from the Regen/DC iPurifier/DC30W/Cerious GE chain.   The iPurifier2 is basically the 'heart' of the iFi iUSB3.0. [link](http://ifi-audio.com/portfolio-view/accessory-ipurifier2/)
 
That finally feeds the PUC2 lite - and the results are truly sota outstanding  A major leap ahead of the DXIO Pro3a. The bass definition and depth is jaw dropping - same for the clarity, focus and stage depth and width.  The DU-U8 and U12 are far back in the rear view mirror...
 
The rest of the chain PPA2.0 fed by a iFi iPower 1uV power supply>Jitter Bug modded to be a VBUS and USB ground isolator (both cut),> LH labs LightSpeed 2G using only the Data leg>Regen...  **That said Uptone is about to  release a killer power supply - so that will be interesting.**

---
####WaveIO (Asynchronous USB-to-I2S interface
I'm really enjoying my WaveIO (Asynchronous USB-to-I2S interface for €99) with NDK's. Sounds very much like the DXIO Pro3A but I'm just going from memory here.
 
[From Romania:](http://luckit.biz/product/waveio/)

Still not sure why I'm the only one to have one of these. DIY is VERY minimal and I'm not even good at it.

The LuckIT waveIO (uses NDK's go figure, and has 7 ultra low noise voltage regulators/3 LDO's LP5900 6uV noise for clocks) will be the heart of my new dac project and I can't wait to hear it's potential. I'm sure it will take the cake and dominate all the DDC's i've heard. I almost went the round of JL sounds USBoverI2s module (also uses NDK's go figure, not sure if it has as many regulators, but does also have 3 LP5900 6uV LDO's for clocks) as it's spec'd better than everything out on the market today...yet it's not clearly the best option for my build. I know it will work, but was a bit more complicated and needed two separate PSU's to get the full effect. I may try it at a later date. But I plan to implement direct DSD with my new project... or the best dac is no dac...Acko is working on a dsd project that taps off the i2s lines to feed true native dsd out into analog. Has a lot of promise and it will be out soon. it doesn't need a dac, just a great usb module like WaveIO, Amanero etc etc.

---

