### 0.8uV DIYinHK kit - [link](http://www.head-fi.org/t/736294/gustard-u12-usb-interface-8-core-xmos-chip/1650#post_11633998)

> I've just finished building my ultra-low noise power supply based on the 0.8uV DIYinHK kit and I'd like to share what I've found about this kit.
>  
> First, some photos of the build:
> 
> ![image](http://cdn.head-fi.org/e/e0/900x900px-LL-e04a2f86_DSC_3748.jpeg)
> 
> ![image](http://cdn.head-fi.org/0/0c/900x900px-LL-0c40bd7f_DSC_3768.jpeg)
> 
> ![image](http://cdn.head-fi.org/e/ec/900x900px-LL-eccca360_DSC_3770.jpeg)
> 
> Since I need 1.6A supply for my NAD D1050 dac, I paralleled the two individual 5V outputs with some changes to the original circuit. Theoretically, paralleling the regulators will reduce the noise even further, to 0.57uV in my case. However, there is no way I can measure it with my humble multimeter. What I do know is that right now, it's working perfectly with my DAC. Actual output voltage: 5.06V. Current consumption is very steady at 1.4A, exactly 0.7A measured from each output, what a perfect balance of load! I am amazed at the performance of these nice LT3042 regulators.
>  
> After I put my new power supply into service, my wife immediately noticed improvement in the sound. She said that the sound was SWEETER, to which I fully agreed. Previously I always start to feel a little fatigue after listening to my system for more than one hour, now that fatigue is all gone. 
>  
> I am now very happy with the combination of my power supply, my dac and my U12, although I did encounter quite a few issues while building the power supply:
>  
> 1) Although DIYinHK claims that this kit is capable of supplying 1A x 2, I believe that the original design is only good for a maximum of 500mA x 2. The Murata hybrid EMI filters supplied in the kit are rated at 500mA only. In my initial tests, they got VERY hot at 500mA. Once the current went above 500mA, the filters got saturated and there were a huge voltage drop once the chokes were saturated. As a result, the output voltage plummeted to 3.7v from 5v upon saturation. This alone won't be too much of a problem if you only need 3.3V. The board can still output a steady 3.3v if you set its voltage jumper to 3.3v. But since I need 5V, the voltage drop was totally unacceptable to me. Eventually, I had to bypass the two nice-looking but useless filters to get a steady 5V output;
>  
> 2) The default heatsinks that come with the DIYinHK are too small for current output above 500mA. The transistors got burning hot when more current was drawn. I was so alarmed at this that I checked again on the DIYinHK website to see what could be wrong. This time, I noticed DIYinHK's warning to use larger heatsinks or a fan for cooling if more than 500 mA current is needed. To make matters worse, the PCB was specifically designed to allow only a small heatsink to be installed. There are capacitors right beside the transistors, leaving no room for larger heatsinks. Luckily, I've already replaced most of the WIMA film capacitors with tiny 22 uf surface-mounted Murata ceramic capacitors, so that I have space to mount larger heatsinks above my capacitors. This tames the heat nicely, although the board doesn't look as nice and neat as before;

Hi ! you have done a great job indeed. And the noise levels you have reached are really impressive.
How did you connect the new power supply to the U12 ?  with an umbilical ? do you have any pictures ?

[ginetto61]

>  
> 3) Regarding the choice of transformers, I originally ordered a R-core but decided to try an EI core first because of their alleged superiority in isolating high frequency noises. My EI-core does work. It has become particularly important after I had to bypass the Murata EMI filters,  but it does get hot and it HUMs when under full load. The humming is audible within a 2-foot range of the transformer. I haven't decided if I should replace the EI core with my R-core to get rid of the humming. But for now, I have learnt to use the humming as a cue to let me know whether the power supply is working under full load of not.

very very interesting.  If the problem is the transformer rating you can try a bigger EI maybe.  I can only see that in some very high end equipment they are used, like in the Schiit Audio dacs and Berkeley Audio dacs.
I have the feeling that EI transformers can even filter some kind of HF noise that passes through the regulators.   But a solution mains filter plus toroid could also work just fine.   And it should be even simpler to implement.  Just a simple mains RF filter is needed.
Or even a power cord with high capacitance can have a nice effect in suppressing HF noise in the mains.

[ginetto61]

>  
> I originally was thinking about building the same linear power supply for my Gustard U12 too, but after I modded my U12 to be fully isolated from USB power, it has become so quite that I don't think an external power supply is needed any more. Now, my U12 and NAD D1050 powered by 0.57uV hand-made power suppy work perfectly. I hear pure, relaxed, sweet and musical sound. This further confirms that an external power supply for U12 is unnecessary, though doable.

My feeling is that the U12 is not very well isolated from noise in the mains.   A toroid transformer without any filter upstream.  A toroid is not a good filter.  EI is.
Of course USB isolation is mandatory.  Pc power is weak and dirty.  Only data should be taken out from the pc (someone says that also data are dirty ... but to clean data is more complicated.  Someone is seriously thinking about this anyway)

[ginetto61]

>  
> Regarding the use of USB isolators, I don't think they will be good for U12 once it has already been modded and isolated from USB power. External isolators can introduce jitter and distortion. I haven't tried them but I am not motivated to try them either, at least not until I am otherwise convinced.
>  
> Hope my little report helps.

[pakultra]

> I guess you are right about usb isolator based on chip.  I have the same feeling. The sound is more grainy and less developed.
> I would use only usb power isolator like the Teradak U9 i am actually using.   It just interrupts the power lines and provides external power.   And it works fine.
> I have instead an isolator like this one here ...
>  
> https://www.circuitsathome.com/wp/wp-content/uploads/2012/02/USB_isolator_built.jpg
>  
> and i do not like the resulting sound.   Maybe it adds some jitter as you say.
> It was just a try ... not very successful unfortunately ...
> Congratulations again for your excellent project
> Regards, gino

[ginetto61]

> Hi pakultra,
>  
> Thanks for sharing this with us. I didn't take the time to look at the specs of Murata 1430R5, they indeed are 500mA only, i did report at DIYINHK and got an answer to remove them if they get too hot,,, hmm, not the answer I was looking for,,,,
> About the LT3042, it can deliver 1A when expanding schematics with external NPN, and that is what the people at DIYINHK did. Off course you can parallel more LT3042 to get higher output if needed.
>  
> For me higher output power is of no importance since I will use them only to power the NDK's, one psu for each NDK. Since the NDK's only draw 6mA it will be no problem at all.
>  
> I suppose those psu's are designed for the isolated I2S kit they sell, so design is not for high-power appliances.
> 
> Regards and keep up the good work :beerchug:
>  
> Alex

[abartels]

> Hi ginetto61, thank you very much for your encouragement:smile:
>  
> I didn't connect my power supply to U12. I connected it to my NAD D1050 dac in place of its factory default external 5V switching mode power supply. I just built a DC to DC cable out of Mogami 2549 and plugged it into my NAD D1050 5V DC power socket.
>  
> U12 doesn't need this much power. 1A is enough for U12. To connect to U12, there are a few ways to achieve this. Here is what I'd suggest doing:
>  
> 1) disconnect pin 1 (Adjust)  and pin 3 (Vin) of the LM317 regulator. Pin 1 and Pin 3 are the two pins at the sides. These pins can be easily desoldered or just cut. Pin 2 (Vout) is in the center and it can be left as it is. Disconnecting pin 3 effectively disconnect everything U12 uses to generate its internal 5V power, including the Toroid transformer, the diodes and the two 2200 uf capacitors;
>  
> 2) connect the positive of your external 5V power to Pin 2 of LM317, or to Pin 3 (Vin) of LM1117, or to the 5V onboard via that is marked as 5V if you'd like to make connections at the bottom of the pcb;
>  
> 3) connect the negative of your external 5V power to Pin 1 (Adjust) of LM1117, or to Pin 1 of any of the two PE-65612 transformers if you'd like to work from the bottom of the pcb.
>  
> Regarding transformers, you are right about picking a higher rating EI core. The one I used is rated at 8V x 1.25A x 2. Theoretically this is sufficient for what I need. I had thought about using its large brother that would be able to provide twice as much power, but eventually I picked the smaller one in favor of its smaller size. Next time I will definitely pick a bigger one.
>  
> My whole system including the U12 is sitting behind a dedicated mains filter, that's probably why I haven't noticed any RF problems so far. By the way, I've also had Stetzerizer filters installed and have measured the RF noise level of my power sockets with a Stetzerizer Microsurge Meter. According to the meter readings, my mains' RF noise level is better than ideal.
>  
> Regarding the USB isolator, I think the key is to have data reclocked after the isolation. Since you've already had an isolator at hand, I'd suggest that you try connecting a bus powered good usb hub between your isolator and your U12. Only connect the data lines from the hub to your U12 and keep using your Teradak U9 to supply power to U12's USB socket. The usb hub can function as a regenerator to smooth out the jitter. I don't know if this will work for you but I think it is worth trying it.

[pakultra]

> Hi Alex,
>  
> Many thanks for your encouragement:smile:
>  
> It's a good idea to use these regulators to power each of your NDKs separately. The original DIYinHK design will be ideal for this without any problems of overheating or voltage drops at all. I might try this myself in my next project.

[pakultra]

---

Quote:
> Originally Posted by pakultra View Post
> I didn't connect my power supply to U12. I connected it to my NAD D1050 dac in place of its factory default external 5V switching mode power supply. I just built a DC to DC cable out of Mogami 2549 and plugged it into my NAD D1050 5V DC power socket.
> U12 doesn't need this much power. 1A is enough for U12. To connect to U12, there are a few ways to achieve this. Here is what I'd suggest doing:
> 1) disconnect pin 1 (Adjust)  and pin 3 (Vin) of the LM317 regulator. Pin 1 and Pin 3 are the two pins at the sides. These pins can be easily desoldered or just cut. Pin 2 (Vout) is in the center and it can be left as it is. Disconnecting pin 3 effectively disconnect everything U12 uses to generate its internal 5V power, including the Toroid transformer, the diodes and the two 2200 uf capacitors;
> 2) connect the positive of your external 5V power to Pin 2 of LM317, or to Pin 3 (Vin) of LM1117, or to the 5V onboard via that is marked as 5V if you'd like to make connections at the bottom of the pcb;
> 3) connect the negative of your external 5V power to Pin 1 (Adjust) of LM1117, or to Pin 1 of any of the two PE-65612 transformers if you'd like to work from the bottom of the pcb. 
 
Hi Pakultra,   the mods your propose are too difficult to me.  I understand now that there are two regulators on board and this adds difficulties ( i thought there was just one).
My idea is much more basic.   I would like to keep the board as it is.  I just want to bypass the power supply on board to use an external  DC power supply of decent quality (maybe a 12VDC power supply ? anyway the one i have can be set from 5 to 30 VDC)
So i will arrive with this DC on the board directly feeding the big caps before the regulators.  Just to explain it would be like extracting transformer and diode bridges and use the external DC power supply to power the unit. 
I will have for sure a better filtering of the mains noise and less noise because i will feed an already regulated DC to the board.  The regulators will still be working as normal. No mods to the pcb at all in this first attempt.   If the result will not be satisfactory i will think of something more drastic.
In the first approach no mods to the pcb.  Just soldering the two wires carrying the DC power from the external PS.

> Quote:
> Regarding transformers, you are right about picking a higher rating EI core. The one I used is rated at 8V x 1.25A x 2. Theoretically this is sufficient for what I need. I had thought about using its large brother that would be able to provide twice as much power, but eventually I picked the smaller one in favor of its smaller size. Next time I will definitely pick a bigger one

If you look at many units you will see that the transformer is located quite far from the circuit.  Or shielded. 
The voltage transformers usually vibrate and generate EMI. For this i think that a separate metallic box would be very beneficial. 
I would never use a toroid with digital.  For analog are ok but never for digital.  
 
> My whole system including the U12 is sitting behind a dedicated mains filter, that's probably why I haven't noticed any RF problems so far. By the way, I've also had Stetzerizer filters installed and have measured the RF noise level of my power sockets with a Stetzerizer Microsurge Meter. According to the meter readings, my mains' RF noise level is better than ideal. 
 
I think that this is a key point. I think that a good mains filter will have the same effect (or better) of an EI/R-core transformer in suppressing HF/RF noise from the mains. 
And also the filters that you mention.  As i am sure i have RF issues in my mains. 
I have this lab supply that inside has a EI transformer, i am absolute sure that it will have a much better isolation and RF filtering effect. I am sure of that.  But i have to listen also to be very sure :D
 
Quote:
> Regarding the USB isolator, I think the key is to have data reclocked after the isolation. Since you've already had an isolator at hand, I'd suggest that you try connecting a bus powered good usb hub between your isolator and your U12. Only connect the data lines from the hub to your U12 and keep using your Teradak U9 to supply power to U12's USB socket. The usb hub can function as a regenerator to smooth out the jitter. I don't know if this will work for you but I think it is worth trying it.  Regards  pakultra
 
Maybe i am confusing things but without a quartz there cannot be any reclocking i guess.  If there are no quartz there is no reclocking.   All the isolators i have at hand and i have bought do not have a quartz on board and therefore they do not reclock the usb signal.
And i guess they introduce some kind of additional noise/jitter.
Does the hub you mention have a quartz on-board ?
 
However actually there is now on the market a isolator and regenerator very well reviewed ... the Uptone USB Regen
 
http://uptoneaudio.com/products/usb-regen
 
![image](http://cdn.head-fi.org/e/e6/900x900px-LL-e6ac73b9_P1080659_1024x1024.jpeg)
 
this device placed in between the pc and a usb dac or converter both will isolate the dac and also reclock the usb signal.
Clearly the final and master reclocking will be inside the dac/converter but this device providing a regenerated (i.e. cleaner and stronger, less jittery)  usb signal will make the work for the XMOS usb receiver inside the dac easier (they say).
They say it works quite ok. It is the last fashion .... there is a thread going on on Computer Audiophile. 
Thanks again,  gino   

[ginetto61]

---

USB as a transfer protocol  has more error detection and correction than SPDIF, I think the best way if you are connecting a computer to a DAC is to leave USB out of the picture completely and use Ethernet.
 
Unlike USB, galvanic isolation is required by the Ethernet standard, running an error correcting protocol like TCP/IP over Ethenret guarantees error free transmission.
 
Here is a barebones version of one of my USB free setups. (This a very compact audio receiver/streamer, so it is very different cmpared to the computer sending out audio over usb which uses the DAC like a soundcard.)
![image](http://cdn.head-fi.org/c/c7/900x900px-LL-c714f298_DSCN0503.jpeg)

The system is basically 3 parts:

1. Audio mediaserver aka Logitech Media Server (install this on the PC)
2. Audio player control app for example Softsqueeze for the PC, iPeng for the iPad, Orange Squeeze for the Android Things
3. Audio player this runs on the RPI
 
This gets the PC out of the audio transmission completely, the player app instructs the RPI to grab audio as a datastream from the server also installed on the PC.
 
When it is running I can disconnect the Ethernet for 1-2 seconds and reconnect it and the RPI will not miss a beat, the audio buffers are several megabytes in size.

Total cost of the above including power supplies is a couple dollars less than the Melodious MXU8, about $300 with a decent metal case.
 
The little board is the Raspberry Pi2 (RPi2), it is connected to the bigger board which is the Soekris DAM1021 R2R ladder DAC.
Interconnect is plain-jane I2S.
 
The I2S connection is galvanically isolated and the DAC reclocks the data to remove jitter much like the Tanly but at a much lower cost.
Galvanic isolation breaks the signal and ground connection and gets rid of the the RF noise headaches.
 
The setup is isolated twice, network-RPi2 followed by RPI2-DAC
 
Software on the RPi2 is squeezelite which means this is a Logitech Squeezebox type device.
 
The silver cable at the bottom of the picture is a USB to serial that I use to load a custom DSP filter profile into the DAC, there are about 10 or so useful filter options.
 
The USB ports on the RPi2 can be used to connect to a USB dac.
Over USB, DSD over PCM (DoP) is supported and PCM sample rates up to 384kHz.
[b0bb] [link](http://www.head-fi.org/t/736294/gustard-u12-usb-interface-8-core-xmos-chip/1665#post_11638700)

You can also use the same ethernet connection if there is one existing on your PC, a dedicated connection to the RPI is not needed.
This means plug the ethernet cable from the RPI into the switch where your PC is connected.
 
Multiple ethernet interfaces on the same PC (multihoming) can sometime cause Windows to tie itself into a knot if they are on the same IP subnet.
[b0bb]

---

> ##U12 mod final update: [link](http://www.head-fi.org/t/736294/gustard-u12-usb-interface-8-core-xmos-chip/1695#post_11639950)
> 
> Hi my friends, I've just replaced the default TCXOs with 2 NDK NZ2520SD crystals thanks to Alex's advice. The new crystals have been running for only 10 hours but I am happy with the results already. So far, I can't say the improvement is like night and day, but there are clear differences if you know what to check for. Overall, the sound is more natural and more enjoyable with the NDKs. This is particularly evident with some of my favorite test passages of songs/music that are usually difficult to do right.  
>  
> Here are the NDKs that arrived in mail yesterday. They are so tiny I had to use my modded Microsoft Live Studio magnifier to see what's printed on them.
> ![image](http://cdn.head-fi.org/5/52/900x900px-LL-5249fa4d_NDKssourcedfromDIYinHK.jpeg)
> Here is how I put the NDKs into my U12:
>  
> 1) Took out the TCXO's and soldered two Mill-Max 110-43-314-10-001000 gold dip14 (4 out) sockets in their place. These sockets have full 0.76µm gold contacts. The best available. These sockets will make rolling different crystals as easy as plug-and-play.
> ![image](http://cdn.head-fi.org/8/8a/900x900px-LL-8ad356ef_dipgoldsocket.jpeg)
> 
> ![image](http://media.digikey.com/photos/Mill-Max%20Mfg%20Photos/110-43-314-10-001000.JPG)
> 2) built pcb adapters for NDK crystals with Mill-Max 3320-0-00-15-00-00-03-0 gold pins: 
> ![image](http://cdn.head-fi.org/e/e3/900x900px-LL-e34b97bf_Goldpins.jpeg)
> ![image](http://cdn.head-fi.org/f/f6/900x900px-LL-f673f59e_handmadeadapter.jpeg)
> 3) soldered Murata GRM2195C1H103FA01D smd 0.01 uf caps to the adapters. 
> Capacitance	10000pF
> Tolerance	±1%
> Voltage - Rated	50V
> Temperature Coefficient	C0G, NP0
>  
> These capacitors are ultra accurate, have No voltage drift, negligible temperature drift and do NOT age.
> ![image](http://cdn.head-fi.org/2/2e/900x900px-LL-2edd212a_0.01ufmuratorcaps.jpeg)
> 4) All soldering work was done with Wonder Solder (197 degree melting point) or Chip-Quik 137 degree low temperature solder paste. This prevented NDK' performance from being degraded by possible overheating during soldering process. The blue hookup wire used is Neotech UPOCC 20 AWG Cryo Treated mono-crystal pure copper wire. 
> ![image](http://cdn.head-fi.org/8/82/900x900px-LL-8290f8b9_soldered.jpeg)
> ![image](http://cdn.head-fi.org/6/6a/900x900px-LL-6a4c68cf_U12working.jpeg)
> With NDKs added on top of my previous mods, I would consider my Gustard U12 modding project a full success and I am ready to move on.
>  
> Here is a full list of mods I've completed for my U12:
>  
> 1) Grounded to IEC with Neotech UPOCC 20 AWG Cryo Treated 20 awg mono-crystal copper wire sourced from takefiveaudio.
>  
> 2) Relay switch removed from board to stop possible power pollution of 80 mA current flowing through the board as well as to save 0.5w per hour power consumption;
>  
> 3) Relay bypassed with the same Neotech UPOCC 20 awg cryo treated mono-crystal copper wire;
>  
> 4) Onboard 5+ supplied to XMOS USB Vcc detection pin via a 470k pullup resistor to trick U12 into believing that it has seen USB power so that it will start communicating over USB; this mod is a must so that U12 does NOT use usb power anymore;
>  
> 5) USB B socket's Vcc and Ground output pins de-soldered from board, flush-cut and insulated. This is a must so that U12 is completely and safely isolated from any USB power. It is safe to use regular USB cables with my modded U12, although data-only cable are recommended for best possible sound;
>  
> 6) Coaxial transformer replaced with Murata DA101C sourced from digikey.ca;
>  
> 7) Two 2200 uf capacitors replaced with ultralow impedance 2200 uf Nichicon HW UHW1E222MHD6 (14 mohm impedance) sourced from digikey.ca. These caps are better the Panasonic caps.
>  
> 8) Took out TXCO's and soldered 14dip (4 out) gold sockets in its place;
>  
> 9) NDKs fitted to handmade adapters and seated securely in the gold sockets;
>  
> I'd like to thank all forum members who have helped to make the mods possible. Special thanks go to hgpsemaj and Alex.
 
[pakultra]