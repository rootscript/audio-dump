
#Pi2Media 503SPD1 [link to start of the forum post](http://www.superbestaudiofriends.org/index.php?threads/raspberry-pi-i2s-to-spdif-hat.1990/)

> A Pi hat with I2S to SPDIF. Sounds like a Digi+ right? But they wanted a couple of items done differently. First it had to have transformer coupled coax. Second was the ability to supply 3.3V and 5V from an external linear supply, thus decoupling from the Pi supply. Third, high quality clocks were mentioned. Finally someone else mentioned it would be great to run the digi+ software "out of the box".
> 
> 1) WM8804 with GPIO selectable 24.5476Mhz/22.5792Mhz Clock input
> 
> 2) Clock are very low noise using NDK2520SD series. Not as low as Crytek's best, but not $20 each either!
> 
> 3) WM8804 runs in Master Mode, Pi in Slave mode so BCLK and LRCLK are very low jitter
> 
> 4) Transformer coupled Coax and Optical SPDIF output
> 
> 5) LT3042 Ultra-Low Noise, High PSRR LDO for SPDIF PLL and Crystal supply
> 
> 6) Jumper to isolate PI 5V from Hat 5V with 2.5mm barrel jack for external 5V input
> 
> 7) 4-Layer PCB with filtered ground from Pi
> 
> That's all the good stuff. I don't provide for external 3V since I have the LT3042 there. The one downside is that in order to switch the clock input between the two frequencies, we need to add SW to the various audio platforms. It's actually easy to do, but it means we'll have to provide the modified platforms to our users until it can be integrated into the next releases. We could make version that has a single 27Mhz clock so the Digi+ code could run without change. The main issue with that is the increased jitter from using the WM8804 internal PLL to create the proper frequencies.
> [Michael Kelly]

This is great Micheal!
I was going to say in the other thread that external 5V as the only powering way for the hat could have been a deal breaker for someone but you made a very smart move putting a jumper there.

As for the double clock... So many people would of course be happier with the liberty to try other platforms without waiting for you to provide the software. Thus the single clock looks like the better option for compatibility.
I say screw this. If we want compatibility many of us already have or can buy the digi or his chinese copy the digipi. I say go for performance with the double clock and be sure to cover the main platforms in the beginning (Rune, Moode, Volumio) and then reach out for wider software integration.

Of course if you want to make a single clock version as well to differentiate your offer, that would be good too.
[Vastx]


> The single clock option will install a single 27Mhz instead of the pair of audio clocks. The Digi+ software expects this. You will still gets you the isolated coax and the very low noise 3V LDO (LT3042 thanks to you Vastx!). I expect that even running form the Pi 5V the performance will be very good.
> 
> You know, the more I think about it, the double clock is something everyone should be able to try, even if they want start with the 27Mhz in order to run the stock drivers. Heck, it's not like another crystal is all that expensive! So, new feature, three clocks: 27Mhz digi+ clone, plus dual 24.5476/22.5792 for no PLL operation, but with a new driver.
> 
> ![image](http://www.pi2design.com/uploads/4/8/5/3/48531975/2867363_orig.jpg)
> 
> Vastx - I must give you full credit for the LT3042. I saw you mention it in your Digi+ thread. I have a couple of TI parts I've used when I need high PSRR and I've used the ADP150 for low noise. But the LT3042 combines the best of both. Thanks for that!
> 
> As for the clocking, let me think about it. I am pretty confident that as is, it's going to be very solid, but I also understand the opportunity it might represent.
> 
> Link to schematics for the brave of you who know how to read schematics.  ;)
> 
> http://www.pi2design.com/uploads/4/8/5/3/48531975/503spd1_sch_p1.pdf
> 
> It's pretty straightforward. The pullup and pulldown resistors on CKSEL0-3 select the 27Mhz by default. One we make the patches for RUNE and Volumio we'll have the ability to switch the right clock on the fly. The code to change the Wolfson WM8804 PLL is already there, so we just stick our changes in that code to select the actual clock instead of changing the PLL multiply/divide constants. Easy, right?
> [Michael Kelly]

Quick question - Does anyone have interest in SPDIF in? The WM8004 has a SPDIF input that I am currently not using. If so, would Coax or Optical be more useful? Or both? With Coax what research I did seems to disagree as to whether or not it should be transformer isolated.
[Michael Kelly]

 the spdif hat designed by Micheal, it is very similar to the digi+, very similar. But it has been designed to maximize the performance: better voltage regulator, possibility to run external power, better clock(s). It has more potential than the digi+. Theoretically it SHOULD be better.

> I added a SPDIF coax input with transformer. I also put some 0 ohm resistors to allow us to build without the transformers. Like Digi+ we'll offer with and without transformer versions. Price will be $39 without and $49 with. Although we have much better power supply specs and the better clocking option, we're just $5USD more than them. As I said before, our pricing is based on our cost. And these just don't cost that much!
> [Michael Kelly]

What did you decide about the clock upgrade pcb layout?
[Vastx]

> I stayed with the small SMT clock selected by GPIO. I really feel the NDK2520SD clocks are such a big upgrade from the PLL, while being better than much more expensive Crystek parts. See this from DIYINHK on the hifiduino web site:
> 
> ![image](https://hifiduino.files.wordpress.com/2014/01/ndkphasenoise.png?w=595&h=387)
> 
> ![image](https://hifiduino.files.wordpress.com/2014/01/cchd957.jpg?w=595&h=541)
> 
> While there is room for improvement, I just feel it's about as good as you can get for the money.
> Back in the days of my 68 Plymouth Roadrunner we had an 80/20 rule: that last 20% of performance cost you 80% of the total!
> [Michael Kelly]

I was wondering if this board will need 3.3V? From reading the description only 5V is needed? I hope so because that would make things easier.

> The 3.3V is generated by an on-board low noise LDO. It has a very high (PSRR (Power Supply Rejection Ratio) over 80db through the entire audio range. That means any noise on the 5V rail is reduced by a factor of 80db+. Coupled with the high frequency filtering we add on the 3.3V line, Power Supply noise should be virtually non-existent.
> 
> Adding you own low noise 5V supply will improve the noise and jitter as will using high quality coax cables. Whether they are audible improvements..... we shall see!
> 
> As Vastx said earlier, the board will have to tested to see if it is better than Digi+. Vastx, Fraggle and PhilMorgan have agreed to be my test dummies. Their feedback will be critical to point me in the right direction as an engineer.
> [Michael Kelly]

I need to look at the specs of the LT3042. I have some LT1963 based regulators that have very good performance. Also, in the past I have investigated Belleson regulators too which have very very good specs.

> I think you'll be happy with the LT3042! PSRR of the LT3042 is more than 80db 10Hz to 60Khz while the LT1963 is 55db at 10Khz drops to 45db at 20Khz. Noise from the LT3042 is 0.8 micro-volts RMS from 10Hz to 100Khz while the LT1963 is 40 micro-volts RMS from 10Hz to 100Khz, or 50 times higher!
> 
> By default the 27Mhz crystal will be enabled and any player that supports Digi+ should just work. To access the low noise clocks we make a few, small modifications to the sound driver in Linux and then we build the player SW on top of that modified Linux. We will submit our changes to the Linux codebase and then, when the player supplier builds their latest version our code will be in there. But that could take 3-6 months depending upon how often the player software is updated by the vendor. Until then you will need to either get the modified player from us, or the modified Linux driver and build the player yourself. That's why we're only looking at supporting Volumio, RUNE Audio and OSMC (OpenElec). But, as I said, once these changes are in the linux base, any player that is updated will get the changes.
> [Michael Kelly]

Can HATs be used with heatsinks attached to the raspberry pi? the type that come with the canakit bundles?

We use 18mm standoffs on our hats to insure clearance. We support both the Up-Board and the Odroid with some hats, and they have even bigger heatsinks.
[Michael Kelly]


YES! Thats what I'm talking about! Audiophile (or audiophool) version please! 110ohm AES and 75ohm BNC would be pretty cool.

The Wolfson WM8804, which is what is used on the Digi+ and we are using, does not support balanced outputs. The Cirrus (who happen own Wolfson now) CS8406 does. I can easily crate another hat that uses the Cirrus device along with the other enhancements we did. BTW, AES uses the XLR, which is a very large connector. What about using the mini-XLR? As for BNC, would that be 2 outputs to provide +/- or one for single ended?


I guess that'd mean custom cable, min-xlr to xlr, but you could also provide it for a fee. How would the CS8406 fare compared to the wolfson ?
According to the data sheet the WM8804 has 50ps RMS jitter while the CS8406 has 200ps RMS. Not as good as I would like. However, the TI DIT4192 does not use a PLL so jitter/noise is based on the input clock, which will be very high quality. Looks like a winner. The only downside is there is no existing hat with this chip, so we will have to modify the players as discussed before. Not Digi+ clone mode!  :(
And I think I understand the use of the BNC, it replaces the RCA, correct?

And yes, BNC would replace the RCA connection. I believe the reason for the preference is because BNC provides a true 75ohm connection whereas RCA does not. That being said, lots of older DACs do not offer BNC input so then an RCA to BNC adapter would have to be used. As much as I like BNC I think RCA would appeal to a wider audience.

You gotta love Google! Some quick searching turned up that I can drive the WM8804 output to a balanced XLR using a high speed RS422 driver. In fact, when you look at AKM's drivers they specifically state it is an RS422 driver. Did some more searching to make sure and found several sources backing it up, including the AES3 Wiki.
So now we'll have the same HW as 503SPD1 but with balanced XLR out. And because we are using a discrete buffer I can drive a BNC at the same time. Both with transformer coupling optional.
New board will be called 503SPD2.

3D PDF's for the SPEED ONE and SPEED TWO (how's that for fancy names) as well as schematics for you guys to take a look at. Go to http://www.pi2design.com/private-info.html

Adding BNC was easy and XLR simply required the differential driver. Both are transformer coupled. The SPEED TWO will require more testing since we have never done AES before. Once we're sure it's solid we'll need some of you guys to hook it into your equipment and evaluate the sound.

As for pricing, the total cost additional was less than $6 so even at 4x this board will be well south of $100.


Actually i need board with coax/aes and RCA same time, so if you going with this solution, i will need two boards with two RPis.
I understand if you switch output from RPi to i2s output, then you will get same signal on all the hat board outputs same time? I mean, if i want to play same music with two different dacs, one connected to RCA and one to COAX.

For these boards the I2S bus is driven from the WM8004. This is because the RPi does not put out a master clock and we need a PLL to recover it. This means the inaccurate BCLK from RPi is multiplied to get a master clock. These clock errors create real problems for the downstream digital devices, causing loss of lock at random times.
Because we are the master, a second board can not be added. There are XLR to RCA adapters that are reasonable priced. A quick search on amazon for "XLR RCA adapter" turned up quite a few choices.


We will be designing a case that will have a bottom half that is the Pi, then sides for each HAT with a top plate. We need this because if you add our 502SSD to the Pi plus any one of our DAC/AMP/TUBE/SPD boards you get a streaming server with SSD storage, Wifi and more! Sorry, shameless plug!


Actually having aes\bnc and rca\toslink in the same board would not be a bad idea at all. I guess all aes users would like to have a rca output just in case. If the price difference is not that much north of 50$ I'd prbably prefer a board with aes and bnc too. We all happen to change dac once in a while, ain't it?
The speed one could be the basic hat board with rca\toslink and the speed two could be a shield board with all the output one might need (rca\toslink\bnc\aes). 

When you wrote "Hat size is the official supported spec from the Raspberry Pi folks" what you mean by that? What is the downside of being out of the supported specs?


So right now most of you seem to prefer RCA and XLR, instead of XLR and BNC? But, BNC to RCA is under $1 for an adapter at Amazon. Heck, I'll include it! 
It seems the desire for BNC and RCA together was the odd one? Just to summarize: 503SPD1 has TOSLINK and RCA, while 503SPD2 has XLR (Balanced) and BNC. All have transformer isolation, though we may offer the SPD1 without. 
Are we good? I would like to send these off for fab this week. But I am kind of doing it for you folks, so your opinions are key!


The point stands as you said, still I see no reason to dismiss the toslink. It doesn't hurt the sound quality or the wallet and there is space.
The speed one is still for the "masses" and the speed two would be for a wider "advanced crowd".


Actually there is no room for the TOSlink on Speed Two, not int eh HAT format which I am loathe to break.


when will this be ready for purchase???

Forbidden, yet you ask anyway! Here is the process:

1) Design completion: Done
2) Design Review: Under way, completion date 5/6
3) PCB Fab submission: 5/9
4) PCB Fab complete and in hand: 5/20
5) PCB assembly and visual inspection: 5/22 - 5/24
6) PCB test: 5/25 - 5/27
7) Alpha Units to testers - 6/1

That's based on no big snafu's. Both the SPD1 and SPD2 will be done together so the schedule is the same. But we will need to figure our how to test the SPD2 since we currently have no equipment in house that has XLR digital inputs.


503SPD1 is TOSLINK in and out, and RCA Coax with isolation transformer. 503SPD2 is BNC out with isolation transformer, plus balanced XLR out also with isolation transformer.

![image](http://www.pi2design.com/uploads/4/8/5/3/48531975/6725978_orig.jpg)

![image](http://www.pi2design.com/uploads/4/8/5/3/48531975/7023075_orig.jpg)


The big, big, big issue with noise and Ethernet on the Pi is that the Ethernet transformer center taps are tied to the Raspberry Pi 3.3V plane. It has a ferrite, but that is to keep out noise in the MHz range and up, not in the audio range. In fact, the purpose of the center tap is to shunt common mode noise to the power plane! Although a solution is to use wireless, a better solution is to use a hat that does not use the Raspberry Pi 3.3V rail. The DIGI+ and DAC+ both use the Pi 3.3V for their digital side. On the 503SPD1 and 503SPD2 all 3.3V is generated on the hat using low noise LDO's with high PSRR (power supply rejection ratio) above 80db up to 100Khz. And we use separate LDO's for the digital interface and one for the PLL and Transmitter. Testing will tell for sure, but I am confident Ethernet will not have issues.

In fact, we posted a quick video of our tube hat playing and it is streaming over Ethernet and the noise floor is below 90db. And that's a basic PCM5102A with Analog Devices ADP150 LDO's with 60db PSRR. The SPD1 and SPD2 have the even superior LT3042 with 80db+.


Michael, if I use a USB3.0 to Gigabit ethernet adapter will this eliminate the noise you are referring to here? Perhaps this is why I think I prefer music using this adapter getting music from my wireless AC bridge versus connecting the Pi3 directly to my bridge with ethernet cable?

Yes. In that case the Ethernet is powered from the USB 5V via a 5V to 3.3V LDO and is no where near the Pi 3.3V.


isn't common mode noise supposed to be shunted to a ground plane?

For frequencies above a few Mhz or so, the 3.3V plane appears the same as the ground plane. High frequency signals/noise are shunted to the ground plane through the bypass caps. But below 1Mhz or so, and especially at audio frequency, the impedance from 3.3V to ground is very high, so the noise stays on that plane.

In fact we use a bypass technique for high speed digital routing. When a signal goes from one side of a 4-layer board to the other, it often switches the plane it is near from 3.3V to ground. To create proper return path we simply add a small cap connected from 3.3V to ground. At those frequencies it's a short. The designers of the Raspberry Pi were digital guys, and somewhat novices at that.



We currently have a board with the PCM5102A DAC and the WM8804. It only does SPDIF and RCA, and runs in slave I2S mode with the 27Mhz PLL, but it does use low noise LDO's and does not use the Pi 3.3V. Anyone willing to test it against the DIGI+? It's called the 503DAC1 and we also have a PI-Zero version, the 504DAC1.


There is no ground filter. We do split the ground plane and join them right at the GPIO header wehre th 5V from the Pi goes. That way any noise in the Pi side tends to be reduced. Grounding is a black art and my experience is limited to the types of systems I've designed and tested. Some of which have had noise issues that required re-configuring what seemed to be a proper ground plane.

That's why you test and try new things. I would be inclined to think splitting the feed might help as it would tend to force Pi noise back to the supply without going through the hat. But, in the case of the SPD1 and SPD2, that noise would not likely create problems anyway. Still, trying it out seems pretty easy and low risk.


THe 503DAC1 is the equivalent of the DIGI+ AND the DAC+. 


> Now that you mention the UP-Board. Your 503SPD1 DAC Hat board has REALLY caught my attention. I am dreaming of getting Roon Server running using this Pi2Media 503SPD1 DAC Hat & the UP board.
> 
> There is a Python library used on Raspberry Pi platforms to control GPIO pins.
> https://up-community.org/UpWiki/index.php/RPi.GPIO
> 
> In addition to GPIO control, it is also used by many other libraries to query the Raspberry Pi hardware version as header pin layouts differed between certain versions.
> 
> "As the UP board has a similar header pin layout to the Raspberry Pi 2, we have created a port of the RPi.GPIO library for UP. This allows many existing Python scripts developed for Raspberry Pi to be used on UP also."
> 
> As the UP board has x86 CPU it should be able to be used with Roon Labs Server software. Without an x86 processor you can only run Roon Bridge.
> https://roonlabs.com/downloads.html
> 
> The Up board appears to have the same form factor as the Rasberry Pi & the same 40 pin connector & pin definition GPIO header, and now with RPi.GPIO library for UP, maybe we might be closer to IS2 connected DAC with a reasonably fast CPU, RAM, storage etc...
> 
> I saw quite a few people in this thread talking about a 'cost no object' version, I would love to have aversion available like that that was compatible with the UP-Board.
> http://www.up-board.org/
> 
> ![image](https://raw.githubusercontent.com/rootscript/audio-dump/master/Pi-types/UP-board/01_UPBoardTopView02WithSpecs11.png)
> [Carlos]

Carlos I like your thinking! This Up Board would be great run Roon or Minimserver and other software tweaks like Jplay, Audiophile Optimizer, etc. This little guy could easily replace my current Atom D525 PC that has a fan which I am not happy with. Plus this will take up less space and require less power. I wonder if this has enough horsepower to run Server 
oe]> 

> Pi 2 Design, my company, already has a relationship with up-board. They are re-selling our 502SSD Storage Hat. The early versions of the up-board did not have the I2S bus enabled. Not sure why, but that's what they told us after we spent a few hours trying to get our 503DAC1 running. However, we are told the final rev will have it. As soon as we get one we'll test and all our hats will be tested on the ard.
> 
> As for ROON we are currently working with them to add support for our 503HTA Hybrid Tube amp, and will add support for all our audio hats, including 503SPD1 and 2. Of great excitement to us regarding Roon is getting support in place for our up-coming 35W/channel Class-D Amp w/HP out hat. Not Audiophile level, but great for dorm rooms, game rooms etc [Michael Kelly]

*Then came a very detailed/specific post from Abartels (that may have slipped through the long thread):*

> I have PI2 and Pi3 and using HifiBerry DAC+ Pro. I use I2S ONLY
> 
> VERY IMPORTANT:
> 
> I did mod one of my DAC+Pro's with NDK NZ2520SD clocks, but that sounded a lot LESS open than XpressO TCXO's !!!!
> Please use XpressO Ultra TCXO's, they are not that expensive.
> 
> I have my own wishlist, after testing and modifying a lot on DDC's I came to the conclusion that it is very important to:
> 
> 1- Isolate ground completely from PI
> 2- Isolate 5V completely from PI - Include 5V header
> 3- Isolete 3.3V completely from PI - Include 3.3V header
> 4- Isolate TCXO's 3.3V completely - include 3.3-5V header for TCXO's
> 5- Include I2S header on PCB !!!
> 6- Put TCXO'x in DIL14 header for future purposes, possibility to exchange TCXO's is a MUST HAVE
> 
> Point 4 is also VERY important because this way you have ability to use 5V OCXO's if you plan to use them,
> most of them need 5V, so if external power header for XO's exist, you can choose 3.3V or 5V.
> 
> Isolating power from XO's is very important, this gives a much bigger soundstage with a black background!
> 
> Hope you will consider my recommendations!
> [Abartels]


Alright! Now we are talking! Back to the audiophool/audiophile version I was talking about early on. I am in favor of keeping the design of the SPD boards the same but use higher quality components like clocks as mentioned by @Eugene du Toit. However. I have found in audio getting the best sound (highly subjective by the way) is less about having the absolute best technology but more about implementation, paying particular attention to noise, vibration, etc. 

I do admit my nerdy side loves the Fifo projects referenced by @Abartels . Lots of possibilities here to improve on the sound. Gotta remember its only been a few weeks since this project actually started! 

I've been thinking more about the UP Board and I think it could be a great solution for my server. I would run Windows 10 and Minimserver on this device plus OS optimizations Audiophile Optimizer, Fidelizer, and maybe Jplay. I would use a second UP as my renderer using the same OS and optimizations and of course a SPD hat. Or I could use my Pi3 with SPdlD hat, whichever gave the best sound. This setup would essentially mimic my current setup but at much lower cost and power consumption. Not to mention I could save a lot of space in my rack. Hmmmm...I am really liking the possibilities.

What will be really interesting is when I try HQPlayer and use the Pi3 or UP Board and SPD as the NAA. I am going to load up HQP on an ultra portable i3 laptop I have and compare that to my tweaked pc.


[link](http://www.superbestaudiofriends.org/index.php?threads/raspberry-pi-i2s-to-spdif-hat.1990/page-10)

---

#Pi2Media 503SPD2

503SPD2 is BNC out with isolation transformer, plus balanced XLR out also with isolation transformer.

![image](http://www.pi2design.com/uploads/4/8/5/3/48531975/7023075_orig.jpg)

---

#Pi2Design 503DAC1 [link](http://www.pi2design.com/store/p7/503DAC1_-_Digital-to-Analog_Converter.html)

---

#503HTA

Hybrid Tube Amp for the Raspberry Pi

---

#504DAC1

pi-Zero sized DAC, Almost the same as the 503DAC1





Michael Kelly
MOT: Pi 2 Design
mike@pi2design.com