#Mac Mini DC-conversion/Linear Fan Controller Kit (MMK)

The Late 2014 Mac Mini model is MUCH easier to work on than the 2010-2012 units.

Get them with just the PCIe Flash Drive and not the HD or Fusion drive so as not to have any SATA bus drive active. In theory the PCIe Flash drive--being directly connected to the PCIe bus controller--should sound as good as the SD card, just monstrously faster. Though just like the RAM in a computer, there is a LOT of high-speed switching going on and the PCIe Flash Drive could have greater emissions.

I do think that avoiding the SATA bus is very much a part of what makes the SD card trick work so well for SQ. So the PCIe Flash should sound very good.

Network shared storage and a BlueJeans/Belden Cat6a cable is my recommendation for full music library storage and playback. Thus an optimal 2014 Mac mini would have just a PCIe Flash drive and the only attached cables would be a DC cable for power (got to ditch the SMPS and PWM fan pulses!), the USB cable to the DAC, and an Ethernet cable (bypass the EN switch or use a fiber optical LAN isolator).










##Links:
[link #664](http://www.computeraudiophile.com/f27-uptone-audio-sponsored/attention-current-mac-mini-users-boot-mavericks-sd-card-load-ramdisk-dismount-your-internal-sata-drives-and-pour-drink-musicians-walking-out-your-speakers-18159/index27.html#post513700)

[link](http://www.computeraudiophile.com/f27-uptone-audio-sponsored/uh-oh-i-beat-my-sd-card-trick%3B-bypass-your-ethernet-switch-and-make-your-external-drives-sound-close-ram-disk-using-apple-thunderbolt-ethernet-adaptor-and-second-network-connection-18475/)

[link #671](http://www.computeraudiophile.com/f27-uptone-audio-sponsored/attention-current-mac-mini-users-boot-mavericks-sd-card-load-ramdisk-dismount-your-internal-sata-drives-and-pour-drink-musicians-walking-out-your-speakers-18159/index27.html#post517362)

[link #129](http://www.computeraudiophile.com/f27-uptone-audio-sponsored/uh-oh-i-beat-my-sd-card-trick%3B-bypass-your-ethernet-switch-and-make-your-external-drives-sound-close-ram-disk-using-apple-thunderbolt-ethernet-adaptor-and-second-network-connection-18475/index6.html#post322458)



#Uptone JS-2 Linear Power Supply

Dual-output, choke-filtered linear power supply with four user-selectable DC output voltages.

Two independently adjustable, separately regulated outputs; Voltage choices are user set from the back panel: 5V, 7V, 9V, or 12V.  
Guaranteed current capability is 5 amps continuous from either output at any voltage setting.  
(Up to 6.8 amps split between outputs, depending upon DC voltage combination; Instantaneous capability of up to 10A).
User configurable for worldwide operation at 100/120/220/230/240 volts AC.
Dimensions: 9.0 inches wide x 9.1 inches deep x 3.3 inches tall (with feet).

**Includes:**

1 custom 5-foot DC cable. This special cable is a shielded, star-quad with 4 conductors of tinned, stranded 18AWG; paired at the connector that makes it about a heavy 15AWG.  Gold/copper/brass Oyaide (5.5mm x 2.5mm) DC barrel plugs from Japan at both ends. Upon request we can terminate one end with a 2.1mm version of the Oyaide connector in case you need that size at the device end.

[A second one of these in-demand custom cables can be ordered by JS-2 purchasers for $60; Specify length and device-end termination.  A nice factory-made, 1-meter, 16AWG coaxial DC cable with DC 5.5mm x 2.5mm jacks at both ends is offered by us for just $10 and is fine for many applications.]

2-meter, 16AWG, shielded AC power cord (USA mains plug, but you can cut and attached an appropriate local plug; it is a good heavy and shielded cord, so adapting it is worthwhile.)

1 SMA coax cable for optional activation of JS-2's unique Kelvin-sense voltage feedback circuit (currently supported only by the UpTone MMK).

The choice to use a costly, custom, electrostatically shielded 100VA R-core transformer is highly beneficial to the JS-2 design.

Just powering the computer, the difference—between the R-core and a toroidal transformer in the bass was shocking. And in comparisons powering a DAC or other audio-signal-handling component, the sonic benefits ranged top-to-bottom, cymbals and piano to deep bass.  Plus R-core transformers, due to the gapless construction of the core, are mechanically silent.

**John Swenson on the benefits of a choke-filtered linear power supply:**

The traditional cap only filter (transformer, diode bridge, big cap) produces raw DC with a sawtooth riding on top. That sawtooth produces lots of high frequency components that the regulator has to deal with. Traditional regulators do very well at low frequencies, but have lousy characteristics at high frequencies which means a fair amount of those high frequency components from the cap-only filter get through to the regulator. Fancy discrete regulators do well at blocking the high frequency components, but add cost and complexity to a PS. Our approach is to use a properly designed choke-based supply whose ripple is a perfect sine wave, no high frequency components, thus a traditional regulator works very well. The discrete regulator is not needed to deal with the high frequency components, since there aren't any.

All diode types except Schottkys emit a burst of ultrasonic noise as they turn off. This noise can go forward into the load circuit AND it can go back into the AC line, and it can also excite the transformer resonance. The "slow" diodes still have this ultrasonic noise. Schottkys are the only type which do not have this noise. Schottkys also usually have about half the voltage drop of other diode types and are usually faster. Which type to use depends a lot on what your supply looks like and what you are trying to optimize for. 
With a traditional low voltage design with a large cap right after a bridge you get large current spikes, these produce a large amount of high frequency noise which needs to be filtered by what comes after the cap. In this type of circuit the slow diodes can help cut down on the extent of the high frequencies generated by the sharp high current pulse. BUT they still generate the ultrasonic noise.

This is another reason why we like to use the choke-based design. With the choke there is no steep high current pulse, so no disadvantage to Schottky diodes. You get the advantage of no ultrasonic noise, lower voltage drop (so lower power consumption in the diode) and no big massive current pulses.

##Notes:
Last weekend I took a prototype over to SuperDad's place and we tried it out. This supply has two regulators, one normal and one with "Kelvin sense", this runs the regulators sense inputs to the load rather than the output of the regulator. It attempts to compensate for any effects of the cable in between the PS and the load.

First pass we were listening to a commercial lab supply, not the mini SMPS. This trip I never got to hear a comparison to the factory setup.

Then we connected the regular output(non Kelvin) to the Mac mini, the result was definitely improved sound, but not spectacular "WOW" type thing. We listened this way for quite sometime. Then we hooked up the Kelvin sense (it's a board that goes in the mini) and it's separate coax to the supply, now THAT was getting to the WOW factor. It significantly cleaned up the sound over the non-Kelvin version. What we were hearing was a much cleaner sound where subtleties of intonation were much more audible. 

Strange as it may seem the effects from the Kelvin sense were less than the "base supply", but they are what added the "WOW". 

This whole thing is a problem for me as an engineer, this was the COMPUTER, not a DAC or preamp. At this point I know it works, but no idea as to the exact mechanism. I spent a lot of effort on this design cutting down on the amount of noise sent back down the line, but the Kelvin sense is just cleaning up the power going to the load. (shaking head in disbelief)

This was just a listening trip, no measurements were taken so I have no clue what actual electrical differences occurred. ( didn't want to haul around several hundred pounds of test equipment)

This was pretty close to the final version, I have to make a few tweaks to get things to fit in the case Alex chose. 

John S.

[link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/#post287975)

**Q1:** That's interesting indeed! Are you using something like a 4-wire Kelvin clip? If so, is it possibly you are setting up some kind of RC filter in the connection, with the power supply side providing a bit of capacitance? Probably showing my ignorance there.  
-Paul

**A1:** Paul:
I'm sure John will answer with a more proper technical explanation (even if the mechanism for the actual sonic differences are not clear), but I can tell you a couple of things: 
After we wired the boards up (attaching regulators and diodes to temporary heatsinks, etc.) in my garage, we put a bank of load resistors on the supply to check the voltages and see how hot the devices would get (1/4" copper bar attached to an old Hovland RADIA heatsink worked great!). Without the pseudo-Kelvin sense line, the voltage at the load end of a 5 foot 18awg dropped about 0.8V (when we had the PS set for 12V as I recall; there are settings for 5,7,9,12V BTW). With the sense line connected, there was no droop at all.
In listening (and BTW, I can report like others that a linear versus the stock Mac mini SMPS offers much better bass!), what I heard with our supply without and with sense was that without it, transients and complexity seemed to tax the system. With it, there was a total evenness and nothing could fluster it. I'm not describing it very well, but it did seem to jive with the purpose of the sense line--to keep up with the load and instantaneous demand, even with the PS being at a distance. In a typical piece of audio gear, say a preamp or power amp, a designer would never want the power supply to attached by several feet of thin cord. I may make up a 12AWG cord and see of the sense line makes as much of a difference.

What's neat about it is that the board we will offer for the mini (with the correct SPoX connector allowing use of the stock internal motherboard>SMPS 9-wire cable--no cutting or soldering) will have the voltage-set resistors on it--and 2.5mmx5.5mm barrel jack and SMA jack for the sense. So installation is really easy (Mac mini surgery is actually much easier than the helpful pictures make it out to be), and one does not have to use the sense line. Any PS can hook up. Even if someone uses our supply, they can switch the sense circuit on an off (at the back of the PS) without moving any wires.

Maybe some pics will help:

![uptoneswenson-preprodpcb.jpg](http://www.computeraudiophile.com/attachments/f10-music-servers/9979d1389311448-why-linear-power-supply-uptoneswenson-preprodpcb.jpg)

This next one was just a short test version of the Mac mini PCB. We are still dimensioning for a board with both jacks at the end that will fit in the vacant holes.
![protominikelvin.jpg](http://www.computeraudiophile.com/attachments/f10-music-servers/9980d1389311759-why-linear-power-supply-protominikelvin.jpg)

A few people have PM'ed me for pictures of the chassis, so here you go:
![uptoneswensonps-chassis.jpg](http://www.computeraudiophile.com/attachments/f10-music-servers/9981d1389312343-why-linear-power-supply-uptoneswensonps-chassis.jpg)
Overall dimensions are 9 inches x 9 inches x 3.25 inches tall (including the height of these really beautiful feet I found). The fit and finish of this enclosure from Japan is far nicer than anything I could find from China (I looked for months!), though it does cost a bit more. I won't be able to calculate total cost or sale price until I can send CAD files for heatsink drilling and back panel machining/printing to the chassis supplier. We hope to be in production before mid-year.
Chris wants me to be careful about not doing commercial promotion in the forums, so I won't say much more about this. 

I will say that John and I had a lot of fun this past weekend. We listened to a lot of different things. I even played him an A/B of Ethernet cables from the machine across the room that shares the tracks with the dedicated music mini. So much fun to baffle even an open-minded, brilliant engineer!

Ciao,
Alex Crespi [link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/#post288005)

**Q2:** What is the projected cost of the board?

**A2:** If you mean just the little 0.75" x 3" conversion board for inside the mini, the answer is as little as we can have it made for plus a little to cover basic handling and transaction costs. But I don't feel comfortable guessing yet. Whatever it is, nobody is going to wince in pain at the price. I figure that people who use it might then be interested in hooking our power supply up to it and taking advantage of the Kelvin sense connector.

If you were referring to the cost for the PS boards themselves: It will be sold only as a complete supply in a chassis, not as a DIY. I am calculating for 50 and 100 unit runs, and even then the parts and labor add up. For this product I still think we will go direct (versus dealers/distributors), and when I officially announce I will be forthcoming about built cost, technical details, and performance. I want to test out for my business what is known as "radical transparency." I think it is a way to engender trust and an appreciation of value--and it fits with my personal ethics.
Whoa, how did I get off on that tangent?…

BTW, our plan is to also offer external Kelvin-sense modules (it's just a pair of resistors chosen for the particular voltage desired at the end of the cable) for use with other gear (DACs, CAPS, etc.). These will consist of a female SMA coax jack and female DC barrel jack on one side, and a male DC barrel plug (or later maybe product-specifc plugs) on the other. Think little 1-inch cubes.

Thanks all for the interest. I'll try to keep people posted--without stepping over the forum/commercial lines too often.

AJC

**Q3:** So it's not going to be this expensive?
Mac Mini Modifications : [Mac Mini Mod Kit Pre Assembled](http://www.yourfinalsystem.com/yfs-power-supplies/190-yfs-ps-512-mac-mini-power-supply)
Same idea though. Right? Will you have any objective data posted?


**A3:** Uh, yes and no. First off, our little board should be less than $100, not $450! Secondly, the stock internal MB>PS cable will plug directly to our board and the DC barrel and SMA jack (for Kelvin sense) will be mounted on the opposite end of the board--and will be what secures/supports the whole thing inside the mini. So I think installation will be easier.

Third and most importantly, John feels that putting a bunch of capacitors inside the mini, AFTER the regulated supply, either does little or does harm (depending upon the values and total ringing of the cap array). I'm sure he will jump in later to elaborate or correct me.

As for measured performance data: Yes, that is a goal of mine. John has explained a lot of good reasons for doing a choke-filtered, regulated supply versus all the fancy discrete super regulator methods that others employ. From a sales/marketing perspective, it will be great to have real scope shots showing just how well the supply rejects line noise, provides good regulation and low ripply, is quiet, and can handle transient loads. Much to do before we get there though.;-)

---

Hello Alex,

I have to agree that typical scope sensitivity is inadequate for investigating noise contributions from equipment whether analogue signal, digital signal of power supply especially.

To help me see what is happening on power supply lines I use one of my old preamp designs, that was originally specified to provide step up amplification for Moving Coil cartridges in Vinyl based systems, where extremely low signal levels need to be resolved. Input referred noise of the active gain stage was typically 0.2 nanovolts root Hz and the circuit has been adjusted to provide 40 dB (x100). This gives me a sensitivity of 10 nanovolts per division on my analogue scope and 20 nanovolts per division on my digital storage scope and this has made a big difference to the low level resolution of my test rig for noise assessment.

Regards
Paul

---

John has explained a lot of good reasons for doing a choke-filtered, regulated supply...
Ah, That's why I saw a EI 'transformer' right next to the toroidal, in one of your pictures !

Would the 'Kelvin Sense' setup also be available as an LPSU filter?
tranz, I don't think it is a 'filter' at all, but an extended regulator feedback line.

---

Yet I do see that your concerns are twofold: 
a) That we are not making measurements of the ANALOG result;
b) That talking about some things we heard in the design process--without it having been a "blind" test--makes some people uncomfortable.

I don't think "b)" needs any comment. 
As for "a)", can you show me where any hi-fi company has published measurements comparing their power supply's effect on the analog output--even the PS of a preamp or power amp, or of a DAC, let alone the analog effect for a computer PS? I am sure one can measure PS quality in the analog output of a big power amp, but for the rest of devices I am not so sure. Of course the quality of any internal or external PS can be quantified with many relevant measurements, and that is certainly part of John's design process.

And while it is not too hard to understand why a quiet and robust supply performs (measurably and audibly) better than a small SMPS built for a few bucks and sandwiched inside next to the motherboard, it is a bit harder for any of us to understand or quantify what we hear between a multi-purpose $90 linear supply and something more refined like this or a Paul Hynes or a Teddy Pardo. I'm not here to defend all the aspects of high-end audio which you are skeptical about. People can decide for themselves what they do/do-not hear and what their priorities are.


By the way, to those wondering about really good SMPS: They do exist, but are not particularly cheap. Some of the best ones John and I have ever found were the "ultra-low-noise" series from this company: Daitron AC/DC Power Supply - Daitron Incorporated The HFS150A series are $285 each in OEM 10 pc. quantity. Even at higher quantity they are still a bit pricy to built into a DAC or preamp. Part cost for a very well done linear would still be less--though not as compact.

---

If talking about this design is making people uncomfortable I can stop talking about it. My original post in this thread was a response to a direct question about it and was not meant as "advertising".

As to testing, I DO make measurements. I haven't done any yet since the prototype was assembled at Alex's place and as I mentioned I didn't want to bring any test equipment with me. Since I'm not a big company with a large budget most of my test equipment is 20 year old stuff off of ebay, most of which is big and heavy, so hauling it around is not something I like to do. 

Since he has the prototype I don't have anything to measure at this point. I haven't had time to build one up for myself. So it is going to be a little while before measurements happen. 

As to how I do measurements, I built a very low noise wideband differential amplifier that is powered off of batteries, and sits in a metal box. (I like 1/4" thick aluminum, why is a very long story) I usually plug this into a spectrum analyzer rather than a scope, it's usually very difficult to see what is happening with just a scope. (BTW I have a 2467B, off ebay of course) The spectrum analyzer is a behemoth HP, very good, but huge and heavy (off ebay of course)

I'm sure I will be able to measure differences in the actual supply rails, but measuring analog on the output of a DAC is a different matter. In order to do this well you have come up with a guess as to what the interaction is, figure out a test waveform for that, figure out the best way to measure what you think is happening, set it up, do the measurements, and repeat 50 times. It CAN be done but takes a LONG time. It's not so simple as play some music and look at it on a scope. The effects from these types of power supply differences are small and you really need to "zoom in" on what they are with specific test signals and measurement techniques. I have done this a few times and it usually takes 3 months or so to figure out what is really happening and figure out how to measure it.

John S.

John is particularly tickled with his recent acquisition of the 400MHz HP 2467B scope (to go with a fancy new set of 4 probes he got for Christmas). It is the only non-storage CRT scope ever made with a micro-channel plate CRT. It does extremely high speed writing, making one-shot pulses at nanosecond duration visible in normal room light. It is pretty unique and he says it will let him see much finer details than an ordinary scope. I understand that a comparable modern scopes would cost a lot more than what he paid.
![image](http://www.computeraudiophile.com/attachments/f10-music-servers/10005d1389400223-why-linear-power-supply-tek2467b.jpg)

John Swenson
Before you put it all together, did you draw a concept diagram of your PSU ? I imagine that quite a few would be interested to see how you used Kelvin Sensing to achieve such great results in voltage stability. I do realise that a few other well known PSUs do similar.
Alex

Really? Others that use a remote sense line for voltage feedback? Examples please.
Of course the principle and practice of Kelvin-sense circuits is not new, I am just unaware of any commercially available low-voltage DC power supplies that offer it. At least not in the voltage and current range of interest for audiophiles.

Alex C
I believe you will see a few examples discussed in DIY Audio, but they aren't commercial power supplies. I believe that a version of the Salas Regulator does this too, using remote sensing. I have never delved deeply into this area , which is why I asked John the question.
Perhaps I should have said well known to the DIY community ? 
Alex

---

Jtwrace: To answer your questions, the supply we will be offering has two separately regulated outputs, independently selectable for 5V,7V,9V,12V. 
Only one of the two includes the pseudo-Kelvin-sense circuit. There is a slide switch next to the SMA jack (see pics upthread). When you slide the switch towards the jack, the supply then ignores the output voltage setting (for that output) and gets its voltage set by the value of the pair of resistors at the far end of the thin coax cable (in the Mac mini example, it's 12V set by resistors on our internal adaptor board; we plan on offering little cube modules that can range anywhere between 5V and 12V).

The max current is limited by two factors: The 5 amp rating of the choke filter we use, and also the rating and thermal dissipation of the regulators (and heatsinks) we are using. We have not finished stress testing a unit (didn't want to blow up the first one before getting to enjoy it!), but I think we will be quoting around 5A@12V, on down to something less @5V. (Larger the drop, the more the heat.) And while yes, that will be total for the supply (only one set of diodes, one 5A inductor, and 66,000uF caps feeding both regulators), I think it will still be a robust unit capable of handling instantaneous loads. 

The idea is for a user to be able to power a pair of devices--say a Mac mini or CAPs, etc., and also a small DAC, hard drive, headphone amp, whatever. John's choke-based design (and careful balancing of cap values is part of that) is very clean, but it is a challenge to scale it into a higher-current arrangement. The chokes get very large, heavy, and expensive, and we would likely have to leave behind the regulators we like. So I think that overall we are sticking a useful balance as small computers really don't draw very much at all (so far the heatsinks and regs have not gotten hot).

Lastly, 120/240V operation is standard. We are using one of those nice Corcom combo power entry modules (IEC/switch/fuse) where you just flip over the fuse tray to go 240V or back.

---

**Q4:** Back to the LPS / Mac Mini issue -
As part of the LH Geek Pulse campaign, I purchased the LPS perk. Mainly I was hoping for the cleanest and most stable possible power for the Geek Pulse through the USB port, but also since it has a separate 12V outlet. 

Here is my question for the CA LPS and Mac Mini gurus - if I remove the internal switching PS from the Mac Mini, I assume that I can hook up the Mac Mini to the LPS from LH. In this case both the Pulse (through 5V USB power leg) and the Mac Mini would then be powered by the single LH LPS system.

Are there any problems with this that I am not currently seeing ?

**A4:** The 12V output of the Geek LPS is rated to only 0.8 amps. That is far too low a current capability to run any of the 12V Mac minis on--or most any computer music server. The LiteOn $35 internal switching supply from the 2010/2011/2012 Mac mini is rated at 7.1 amps, but that is much more than the machine needs for duty as a music server. It think Apple went that big because they could within the form factor and because the fastest quad-core i7 model running some heavy-duty graphics rendering might get the machine to draw a bit more during 100% CPU utilization and they want to err on the conservative side.

I just put an ammeter in line with the DC feed from our prototype linear PS (around 5A@12V) to my 2010 2.4GHz Core 2 Duo Mac mini. At idle it draws just over 0.5 amps, while during start-up and operations such as Audirvana Plus upsampling CD tracks to 176.4KHz it draws a little over 2 amps (after A+ finishes converting and loading the track, demand drops down to about 0.8A.

So while a 2 amp supply technically could take care of running a mini (and the Geek LPS is much smaller than that), units that small usually don't have very ample storage capacitance for instantaneous demand and can result in a somewhat lightweight sound--usually with with a DAC or preamp, but oddly robustness seems to impact the computer a bit as well.

Hope the above info is helpful.

Best,
ALEX C.

Forgive me if this sounds a little trite, especially from a newbie to electronics, but I thought a load-sensing regulator is very much "standard fare" in the super regulator game. Jan Didden and Walt Jung et al have made their designs public and their regulator boards are available on DIYAudio. Am I missing something in relation to the design element that's being introduced here?

There's a very good thread on DIYAudio discussing snubber strategies and transformer ringing, snubbers across the transformer secondaries (preferred) versus across diodes (not preferred), what actually does the snubbing (the resistor and not the capacitor) and how to dial in the right amount of resistance. Look for the Quasimodo thread.

**Q5:** Regulator board with load sensing. Not enough current capability for a server but the articles relating to its design are interesting.
Are we talking the same thing here sensing-wise?

**A5:** I'll let John speak to the differences more specifically. But of course current sensing is nothing new. We are just putting the sense/voltage-set resistors at the end of the DC cable to include it's resistance in the loop, thereby insuring the right voltage. I am not sure how it works on a dynamic basis. Again, I'll ask John to jump in tonight.

**Q6:** There you can see the impact of taking the resistance down from under-damped to a critical level of damping and further down to an over-damped level.

**A6:** Well yeah, but who is going to use a 24 ohm resistor for their snubber RC? That's what it took for Mark Johnson to badly overdamp the transformer. It is cool that people go to radical lengths to critically damp their transformers (too many commercial high-end audio products don't attempt to damp their transformers at all!), but a little over or under will be awfully hard to hear. What John said was that he measured a whole bunch of transformers--large and small--and kept ending up with critical or slightly over-damping with the same value resistor. Funny thing is, reading through several threads on snubbers at diyAudio (the one you linked and a two others), almost everyone using the Quasimodo test rig also ended up with around the same resistor value as Swenson did.
Like I said, it is neat that people are aware and tuning snubbers. Having one is very important. But from what I have been taught, I just don't think this particular element of a PS design is the most critical one to get exact.

---

Let's not get defensive. The selected charts in that post were endeavouring to suggest a point not suggest that anyone would use a 24 Ohm resistor. They are very informative for someone who might otherwise have been thinking of just placing caps across the diodes. 

There are lots of things to get right in a power supply and if you are diving into load sensing then already likely over-reaching in terms of what's needed and may as well optimise the other bits as well. I was providing links to information the poster above may find interesting, not trying to dictate the outcome. 

Let's have an open mind and open discussion about techniques and how and why they work or why some are better than others etc. I think a lot of people here would like to learn more about what they can do to power their audio servers. Product promotion can go elsewhere but I for one don't mind if someone is saying words to the effect of "here's what we're working on and why we think this approach is useful..." if it helps inform people about power supply and audio server design. 

I am intrigued by what you said about 110v vs 240v mains support. You are deploying a component which by simply reversing the fuse socket it alters series versus parallel wiring of the transformer?

EDIT: I just reread your reference to Corcom. Are these the L or LA Series "dual configuration power entry models"? So you wire the transformer for 110V input and if the user has 240V the power entry module takes care of 240->110V? How good are these versus rewiring the transformer?

---

"There are lots of things to get right in a power supply and if you are diving into load sensing then already likely over-reaching in terms of what's needed and may as well optimise the other bits as well."

Not sure why you think extend the voltage sense out to a small cap at the end of the cable right at the load is over-reaching. It is a good idea that measurably and audibly makes a nice difference. And I assure you, the snubber values selected are optimal for the transformer we are using. More unique in the supply is choke-filtering and the particular LDO regulators we chose.


"I am intrigued by what you said about 110v vs 240v mains support. You are deploying a component which by simply reversing the fuse socket it alters series versus parallel wiring of the transformer?"

EDIT: I just reread your reference to Corcom. Are these the L or LA Series "dual configuration power entry models"? So you wire the transformer for 110V input and if the user has 240V the power entry module takes care of 240->110V? How good are these versus rewiring the transformer?
Nothing new here. We are using a dual-primary transformer, and the IEC/switch/fuseholder (a 10amp "P" series model with no filter) simply connects the primaries in series for 240V and in parallel for 120V--depending upon which way the fuse holder drawer is facing A little window even tells you what it is set for, and the fuse holder works with both American and European length fuses. The module costs $18, but it will save a lot of labor in production.

---

I would have thought it a direct product of an external PSU with a long umbilical cord. Place the regulator closer to the load and the benefits of load sensing presumably diminish significantly with a decent linear PSU. I'd be interested to hear more from John on this. What regulators are you using? Since we're discussing power supply techniques rather than marketing a product it would be useful to the discussion for you to post a schematic of the PSU design. 

---

**Q7:** How different is the CLC filter from the one John posted here:
![image](https://web.archive.org/web/20120229202628/http://johnswenson1.home.comcast.net/~johnswenson1/stereo/SB_5V.GIF)

**A7:** The filter is the same basic concept but the values are different. Every time I do a new design I come up with new values to meet the requirement of that design. The constraints are:

* 1) as close to choke input as possible. This usually means a fairly small first cap.
* 2) overall critically damped response
* 3) fast recovery time, aim for less than 20ms
* 4) high load regulation
* 5) low ripple

Then you can throw in size and cost limitations sometimes as well. In this case we had some size limitations, the ideal components wouldn't fit in the case Alex wanted to use, so some slight compromises had to be made.

*Only compromise (though it's highly unlikely to have any impact on performance) is that we went with two 33,000uF caps post-choke instead of the single 4-inch tall(!) 68,000uF monster John originally spec'd.*

It's a difficult optimization task. 

The regulator is from Micrel, I don't remember the model number off the top of my head. As with everything else it was a compromise, high enough current capability, high enough power handling capability, high input voltage so it won't fry when the load is small, wide bandwidth, reasonably low noise. It's not the best at any one parameter but is reasonably good at everything. Oh yeah, cost is in there too.

The overall goal was to produce a design that has extremely low noise being fed back into the AC main, fairly high isolation from AC main to output, high attenuation of line frequency harmonics to the output and very low level of ultrasonic noise. Ultra low broadband noise was NOT a primary goal. 

The Kelvin sense stuff was an experiment. I'm calling this a "psuedo Kelvin sense", the architecture of the regulator allowed the voltage set resistor network to be located remotely, with the ground connection and feedback pin of the regulator being run through a separate cable to the load. This does allow the regulator to compensate for the intervening wiring to some degree. I have not had time to actually measure this, but there is an appnote from Micrel that shows a similar configuration working quite well. 

I have done many similar designs before so I have a pretty good idea how this will perform, but I have not had time to actually run a battery of tests to get the actual performance. Right now I CAN'T because Alex has the only prototype so far. I need to spend some time to build one up for myself, but other things seem to get in the way (such as shower doors shattering into a gazillion pieces, light fixtures flashing on and off and other household tasks that need to get done right away)

The PS is far too big to actually fit inside a Mac-Mini, so there will HAVE to be some form of cable between the box and the computer, the Kelvin sense is an attempt at minimizing the impact of the cable. It was actually easy to do so I put it in there. 

John S.

---

**Q8:** Can anyone explain the difference between a regulated power supply and a linear power supply?

**A8:** There is no difference really. A linear power supply refers to one which is not based on switching technology. A linear supply can be regulated, or not.
An unregulated linear power supply will vary in its output voltage, both with AC line variances and with load (current draw) variances.
A regulated linear power supply will include active circuitry which holds the output voltage stabile regardless of load or line conditions (ideally, how well it can do this is limited to some extent).
Additionally, while most switching power supplies are regulated, they do not have to be, so there are also both regulated and unregulated switching supplies.

Power supply design is a complicated business. For audio components, you are really listening to the power supply, so the better the power supply, the better the sound. This means you want a no noise, no output impedance supply, ideally, with absolutely stable voltage regardless of load. The demands which high end audio components place on a power supply are beyond all other uses, besides high precision measurement instrumentation, some military hardware (like highly sensitive sonar and radar applications) and some medical tech.
I would not expect any off the shelf industrial power supply to be even adequate for high end audio purposes. When something says "low ripple" but does not specify what that ripple actually is, it is pretty accurate to assume that the ripple is not really that impressive by audio standards. [link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/index6.html#post292805)

---

**Q9:** On another note, John I'm interested in your views on the impact of using choke filters in power supplies on the response of the power supply. I had a super regulator and audio designer comment to me today that he doesn't like using them because they raise the impedance of the supply and slow down its responsiveness.

**A9:** The traditional cap only filter (transformer, diode bridge, big cap) produces raw DC with a sawtooth riding on top. That sawtooth produces lots of high frequency components that the regulator has to deal with. 

Traditional regulators do very well at low frequencies, but have lousy characteristics at high frequencies which means a fair amount of those high frequency components from the cap only filter get through the regulator. Those discrete regulators do well at blocking the high frequency components, but add cost and complexity to the PS.

My approach is to use a properly designed choke based supply whose ripple is a perfect sine wave, no high frequency components, thus a traditional regulator works very well. The discrete regulator is not needed to deal with the high frequency components, since there aren't any. 

The filters I design also have very fast recovery time. A traditional C only filter has a fairly slow recovery time. With the C only if the load presents a large current change (lets say your computer starts taking 3A instead of 1A, then goes back to 1A after a short time). With the C only filter the voltage across the cap goes down quickly and takes a long time to get back up to the original level. With the choke based supply charge can come from both the cap AND the magnetic field stored in the choke. The result is that the voltage drop is less AND it recovers to the original level 10 - 20 times faster than the C only filter. In my designs I carefully tune the filter to provide a considerably lower drop and the much faster recovery time.

The result is that the raw voltage presented to the regulator is much easier to work with for the regulator. But shouldn't the regulator make that irrelevant? The problem with the slow response time is that frequently that 2A current spike is not a lone event, there might be a bunch of them in a row. With the slow response the cap can get into a situation where it doesn't recover in time for the next event, and the raw voltage descends rapidly to the point that the regulator temporarily goes out of regulation. With the fast recovery time that is much less likely to happen. 

This actually very important for low voltage high current supplies. With any regulated supply the higher the raw voltage is above the regulated voltage the more heat you have to dissipate in the heatsinks. So the tendency is to run the raw voltage fairly close to the output voltage, which means margin for these sorts of short term current spikes is fairly small. 

The choke based filter also has another big advantage, essentially zero noise is injected back into the AC mains, the traditional C only filter can put a lot of noise back down the power cord. 

So from my analysis it is much better to use the choke based filter.

John S.

Thanks John. I was reading an interesting article by Charles Hansen re choke-input filters (ahead of the input caps) last night. (He was at pains to distinguish this from a smaller choke filter post these caps.) I guess, in large part it, depends on how good the regulator is. With a fast-response, high-quality regulator a current spike can draw on the output cap and through the regulator from the input caps. And the more low-ESR capacitance the better (apart from cost). I suspect a choke immediately after the rectifier diodes can't be a bad thing but I'm still trying to get my head around the comment that it raises the impedance of the PSU. (Nose back in Horowitz's impeccable textbook...) 
Oh, in the schematic of yours that I linked to a couple of pages back, what's the purpose of C2 120uF electrolytic ahead of the choke?
PS: my raw AC is a little over 16VAC, 22ish DC post rectification (no load, I need to check again) for input into a 12V super-regulator (with 4V drop) and so good "headroom". The side of my enclosure (the awful Streamcom) is the heatsink.

BTW, Silicon Chip magazine had a problem with some toroidal transformers humming with one of their amplifier designs. (20W Class A)
Their fix was to use a low value choke (100uH? ) after the rectifier diodes. A minor problem though was slightly reduced supply rail voltages, and loss of a couple of watts power.
Regards
Alex

To answer your question as I understand it, and greatly over simplified:The choke would raise the Z between the transformer and c3, a good thing, not between c3 and out, a bad thing. You need c2 between diodes and L1 or you change the filter characteristics from a pi to an LC.
Just google pi vs LC input filters.
-4est

I may just pop in this Coilcraft CMT4 26mH 6A 0.115Ohm choke when I drop in the CRC snubber and see what happens.
-JJJ

Uh, I'm sure you know this, but that Coilcraft is a common-mode choke. We are using a DC filter choke in John's design.

And I think 4est is correct, Swenson's C2 is about knocking down the diode spikes before the choke. John has a whole process for arriving at the particular C2 and C3 values. They are not arbitrary at all, and C2 needs to stay relatively small. I could copy/paste from what he has previously written, but I'll wait for him to chime in instead.

---

[link to bypassing PDF (Power Supply Noise Reduction)](http://www.designers-guide.org/Design/bypassing.pdf)

I suggested the article as worthwhile reading because it covers specifically the topic of tuning a CLC network. Any pre-regulator capacitance filter, RC filter, LC filter or CLC filter is, of course, merely trying to lighten the load on, and thereby improve the performance post, the regulator. The goal is still a low-impedance power supply with extremely stable voltage.

To quote Horowitz and Hill "Power-supply filtering is really a form of bypassing."

---

Boy a lot of different things to respond to. 

I don't have time right now to make an official treatise on the subject, so this is going to be a little scattered. 

The first thing to note is that a CLC or LC behaves very differently depending on the values of the parts used and the load. Thus statements of the form "an XYZ behaves like this" is not always the case, it depends on the values and the load. 

As I stated in my previous post on the topic, my designs are very carefully designed to work in a specific way, which is frequently quite a bit different than other LC or CLC designs. 

The choke design provides two primary advantages over a single large C filter:
1) the remaining ripple is pure sine wave, which makes the regulators job MUCH easier.

2) It radically cuts down on the current spikes from the transformer, significantly cutting down on noise put back into the AC line.

In my previous post I did mention that from the load's standpoint a single large C filter and a very good discrete regulator design can achieve similar results. JJJ your friend is right in that aspect. I did mention that that is one of the engineering tradeoffs involved, Do the choke filter, and simple regulator, or just C filter and complex regulator.

BUT if you go with the large C only supply the diodes and transformer WILL be seeing LARGE current spikes. This WILL propagate significant harmonics of the 120 Hz (or 100Hz) back down the power cord. And in addition if the transformer is not damped it WILL excite the ultrasonic ringing of the transformer. This will happen no matter how good the regulator is. 

An example. Lets say you have a single large filter with a 60,000uF single cap filter, and the load is pulling 2A. The current spikes through the diodes and the transformer are about 15A.

In the link others were pointing the characteristics of an LC filter were described. A few pertinent aspects of an LC, for a given C the ripple will be much lower , this isn't that big of an advantage with the very large low voltage caps you can get today, so we don't really need it. IF the choke value is chosen correctly for the load current (the so called "critical inductance") AND the DCR of the winding is kept low, the output impedance actually goes down. (voltage drops less for a current increase than it would for the C only version) BUT if the inductance is too low or the DCR is too high, this doesn't happen and you DO wind up with a higher output impedance. So your friend is right IF the wrong choke is used. Getting the RIGHT choke is not always easy, there are only two companies that make these types of chokes so you are stuck using one of their models. It almost always turns out that the RIGHT choke is big, heavy and expensive. 

Some more aspects of LC are: once you achieve critical inductance the diodes and transformer do not see any current spikes, they are continuously providing current to the choke. To my mind this is a very big deal. There is one not good deal about an LC filter, that impedance of the choke causes the C to charge up slowly, thus it will recover slowly when a large current demand hits the output. This is not good.

This slow recovery is what the first C is all about. It is carefully chosen to create a tuned circuit with the choke such that it squirts an extra bit of charge into the choke at just the right time such that this long recovery time is drastically diminished. For example a common LC filter might have a recovery time of 250ms, with the right first cap I have been able to get it down to 8ms, a pretty big improvement. Fortunately this effect can be achieved with fairly small caps, which cause only very small current spikes. For example a 2A load (which had 15A spikes with just C) will have about 2.6A max current with the proper CLC. So the current through the diodes and transformer is not quite as good as a critical inductance LC, but the decrease in response time I consider a very good tradeoff. 

So if it is done right the output impedance is NOT increased, the ripple is lower and is a pure sine wave, and there is a DRASTICALLY reduced amount of noise injected into the power cord. To me this is worth the extra expense of the big, heavy and expensive choke. 

I hope this gives some insight into the design.

John S.[link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/index8.html#post295127)

One important thing I forgot to put in the big post, for most PI designs that have been done over the years, the first cap has a different purpose. 

One of the critical parameters of a choke is how much AC voltage there can be across the choke. If the AC voltage is too much the choke saturates and it doesn't work right any more (and gets hot and starts buzzing loudly). A choke that can handle the full AC voltage of the supply (which is what happens with an LC filter) is generally very expensive. The first cap partially filters the raw signal so there is less AC voltage across the choke which lets you use a cheaper choke. But the bigger the first cap, the larger the current spikes. It's very much a tradeoff the designer has to make. 

What I use the first cap for is very different.

I also want to talk about what the current spikes look like for the different configurations. For the single large C filter the current spike is very short it goes up high very fast and almost as fast goes down. Its a high current very short spike. Most of the time there is no current flowing.

With my CLC design there is current flowing almost all the time. There is a very small amount of time when none of the diodes are conducting and when one does start conducting there is a small peak (essentially a small overshoot) that is just slightly higher than the average current. It is a MUCH more benign waveform than the short full current spike of the C only filter.

John S. [link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/index9.html#post295133)

---

**Q10:** So all this talk and its future prospects are about a mac mini? This is not a design for CAPS servers?.

**A10:** Oh gosh, that's not it at all Jakov. We want this supply to be as flexible as possible so it can be used with a wide range of gear (or at least with gear only needing a positive DC voltage since we are not doing a bipolar, +/- supply). This is a supply that will sound great with CAPS, small DACs, hard drives/SSDs, headphone amps, etc.

The UpTone Audio JS-2 (temporary name?) has two separately regulated DC output jacks (on heavy-duty but standard 5.5mm x 2.5mm barrel sockets), and next to each one is a 4-position voltage-selection switch. Choices are 5V, 7V, 9V, or 12V. John is doing stress testing now, but we expect max current ratings to run from around 3.5A to 5.5A (on each output), depending upon selected voltage. In addition, there is a slide switch to put one of the outputs into a pseudo-Kelvin-sense mode, whereby the rotary voltage selection is ignored and the voltage is determined by a pair of resistors at the far end of a thin coax cable (see posts #9 & #15 in this thread for more detail). With the right resistors, the output on that side of the supply can be anything from about 1.5V up to 12V (maybe a little beyond, I have to check).

The only thing that is Mac mini-specific, is that concurrent with the launch I will be offering (probably just throwing in free for the people who intend to use a mini with it) a small DC-conversion-kit board that makes for an easy soldering-less conversion and supports the Kelvin-sense line as well. During the lead time for chassis production we will turn our attention to little "Sense Cubes" for those who want to utilize the voltage-feedback sense line with other gear. These would have both female DC barrel and SMA jacks on one side, and a male DC plug on the other.

Admittedly, our new supply is not a full-blown, multi-rail ATX supply with timed turn-on sequences, etc. People who use it with a CAPS are likely to use a PicoPS fed by the 12V, perhaps using the JS-2's second output to isolate some 5V or 12V portion of their server.

Also, for some 5V DAC users, I'd like to find a source for something like this cable:
![](http://www.computeraudiophile.com/attachments/f10-music-servers/10590d1391374161-why-linear-power-supply-usb-dc-adapter.jpg)

It passes through the data yet interrupts the computer's 5V to feed from cable "T"ed into it. Does anyone know where to get these cheaply?

Hope this answers some of your questions.
Regards,

**Q11:** Thanks John for taking the time to respond. I'll have to chew on your responses for a bit. I'm also looking at Pi filters versus RC filters in the context of an unregulated power supply for a power amp. One commentator made the following point: while Pi (CLC) filters present a number of advantages over RC filters they suffer a significant disadvantage - when current draw goes low, voltage rises dramatically (upwards of 50%). I'm still trying to get my head around this in the context of a digital computer as the load with its sharply varying current needs...

**A11:** Yes this is a problem. Remember when I talked about critical inductance, for a given current the raw output voltage will be 0.9 of the AC if the inductance is above critical inductance. If it's below you get the traditional C only output voltage of 1.4 times AC. 

You can think about it the other way and think of a critical current for a given choke, if above you get 0.9 if below you get 1.4. Of course there is a range in between, it's not a super steep curve. 

So when doing such a design you have to take it into account. There are two ways to do this:
1) choose your voltage regulators so they can take the higher voltage. Since it only happens at the lower current draw you won't be burning them up, but you need to make sure they can withstand the higher input voltage.

2) put a big monster resistor across the raw supply that will make sure there is always enough current to keep it above the critical current. 

Or do both! For example the supply I'm doing with Alex has a maximum current of 5A and a critical current of about .7A. When the load current is above .7A the voltage is around 14v, when it is very small it is about 23V. The voltage regulator is good to 36V, so that is not a problem, but the big caps are 25V, that 23V is too close for comfort, so I put a big resistor on the raw supply to always pull .2A which lowers the no external load voltage down to 18V, I'm much more comfortable with that on the 25V caps. But I have to live with the extra heat dissipation of that resistor. 

John S. [link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/index9.html#post295531)

---

I think you would be very surprised as to what resistor is required to dampen transformer ringing. The "optimal" resistor for my transformer (160VA, series for primaries 230VAC, secondaries in parallel for 15VAC) is around 15-16 Ohms. Much above that is a waste of time.
-JJJ

Wow, 15 ohms, I have never found a transformer that needed that low a value to damp. What type of transformer is it? (EI, torroidal, R-core etc.) That would have to have some unusual parasitics to require 15 ohms. Have you measured what the resonant frequency is? 
John S.

---

My Hovland RADIA-i power amp has been on continuously for 3 years (excepting vacations and the odd power outage). And my circa 1985 Hovland Model 1 high-gain, discrete phono preamp has been powered on for over 10 years a stretch. Never any trouble.
Hi Alex C.,

Are you using Duelund® caps?
Hi Alex, nothing lasts forever. Electrolytic caps will dry out, even while they are not in use. Hence I would advise folks to use fresh parts, and especially avoid "NOS" electrolytic capacitors, like Blackgates, which have been out of production for quite some time now. Usually domed tops happen to a cap which is either defective, or has been subject to over temp and/or over voltage conditions. Good quality, fresh, electrolytic caps, operated well within their voltage and temperature tolerances, can be expected to last around ten years, or more, powered up all the time. Any part can be defective though... but keeping things powered up will not prematurely wreck an electrolytic cap, unless the component is poorly designed and uses the caps too near their voltage or temperature rating.
I have seen some companies spec caps with a voltage rating equal to the nominal voltage seen in the circuit! This will result in premature failure.

Film caps (like Duelunds) are an entirely different story, unless they are subject to gross over voltage, or some kind of highly unusual environmental condition, they will last forever, and for sure they sound better when they are kept with some voltage across them to keep the dialectric biased.

---

Yikes - let me first state that I am a newbie to this stuff. I've just been learning as I go along. So re rectification diodes I understand that one desires something that switches fast or ultrafast but, importantly, which has soft recovery to minimise transformer ringing. So you get people seeking the benefits of HEXFRED and other diodes. I had asked a very knowledgeable guy on DIYAudio what he thought of CREE C3D08060A silicon carbide Schottky diodes which Alex here and recommended. He responded in a sensible manner:

"I myself certainly would not select or pay for Cree's Silicon Carbide diodes; instead I'd probably choose something like the Fairchild FFPF30UP20S. It's rated for 30 amps, 200 volts, and most importantly, it's an honest to goodness soft recovery diode with the softness parameters (ta, tb) measured and specified on the datasheet. Non repetitive peak surge current is 300 amps. It's way cheaper than the Cree diode too."

So I think this is an area where different people have different opinions. Also, I've come to the conclusion that a CRC snubber across the transformer secondaries is also very important.

John Swenson expressed views on rectifier diodes in this other thread (posts [302](http://www.computeraudiophile.com/f10-music-servers/good-linear-power-supply-unit-s-computer-audiophile-pocket-server-music-player-wont-break-bank-17336/index13.html#post280723) and 304)

As to the question of diode type there are 4 things to consider, switching time, ultrasonic switching noise, voltage drop and average/peak current capability. 

All diode types except Schottkys emit a burst of ultrasonic noise as they turn off. This noise can go forward into the load circuit AND it can go back into the AC line, and it can also excite the transformer resonance. 

The "slow" diodes still have this ultrasonic noise. Schottkys are the only type that do not have this noise. 

Schottkys also usually have about half the voltage drop of other diode types and are usually faster. 

Which type to use depends a lot on what your supply looks like and what you are trying to optimize for. 

With a traditional low voltage design with a large cap right after a bridge you get large current spikes, these produce a large amount of high frequency noise which needs to be filtered by what comes after the cap. In this type of circuit the slow diodes can help cut down on the extent of the high frequencies generated by the sharp high current pulse. BUT they still generate the ultrasonic noise.

This is why I like to use the choke based design (as in that schematic posted earlier in this thread). With the choke there is no steep high current pulse, so no disadvantage to Schottky diodes. You get the advantage of no ultrasonic noise, lower voltage drop (so lower power consumption in the diode) and no big massive current pulses. 

When choosing diodes it's important to calculate the power dissipation of the diode and make sure they will not be overheating. In higher current designs (such as for driving a computer or power amp) this dissipation can take you by surprise. For example many non Schottky diodes can run .8 to .9 V drop when dealing with 5 amps, divide by two and you get over 2 watts. Many diodes are only good for up to 1.5 watts if not heatsinked. A Schottky diode with a drop that is usually 40% less than a non-Schottky diode can make the difference between needing to heatsink or not. 
John S.

Hi John
Do you have any experience with the Cree C3D08060A–Silicon Carbide Schottky Diodes ?
A friend of mine reported an audible improvement in a Class A amps dual PSUs after replacing MUR devices with these.
Regards
Alex

I use them for high voltage tube supplies, but not for low voltage supplies. The SiC (Silicon carbide) diodes have a much higher voltage drop than "regular" Schottkys. You can get regular Schottkys up to 100V rating, the only reason i would go with the Crees is if you need more than 100V.
John S.

**Q12:** Do you have ripple measurements for both rails in use of the new baby? Will both rails be completely isolated?
Cheers

**A12:** Not yet. Ripple will be suitably low, but the key thing is that it will be a very quiet supply with none of the high megahertz noise that other supplies (standard cap/regulator style) let through. The inductor and John's careful choice of pre and post-choke caps are the key to making this an exceptional unit. Specs will be published I promise.

As to the rail isolation: There are two LDO regulators, but behind them there is only one set of everything (caps, inductor, transformer). To do a true, fully isolated 2-rail supply would require a second big inductor, a second set of caps and resistors, and a custom, muti-secondary power transformer. That's not going to happen in my little 9" x 9" x 3" case. But I will ask John to do some measurements regarding rail isolation.

I've simultaneously powered both a computer (my Mac mini) and a DAC at the same time and it sounded great. Mostly I am using the second rail for an external hard drive.

---

I just found this thread and what is so interesting is that I've already got the PCB made and the circuit is an improved version of John's power supply. It has two independent 5v outputs, each powered by an ultra low noise super regulator (4uV RMS). I have another version that is using a R-core transformer, and it does sound significantly better than the Triad transformer John has specified (much richer and deeper low bass). Here are some pics of my supply:

![image](http://www.computeraudiophile.com/attachments/f10-music-servers/11605d1396197635-why-linear-power-supply-xe2f3041.jpg)

![image](http://www.computeraudiophile.com/attachments/f10-music-servers/11606d1396197661-why-linear-power-supply-xe2f3042.jpg)

It is the same circuit as the John Swenson LPS. Regulator is the Belleson SPJ (new generation with lower noise output and san SMD ceramic caps - i.e.: no microphonic effects).

[link](http://www.computeraudiophile.com/f10-music-servers/why-linear-power-supply-18929/index10.html#post310271)

Hi Alex,
I'd avoid having the choke being so close to the toroidal transformer. The "belly" portion of a toroidal transformer emits the most magnetic flux. In my supply, I put the transformer and the choke far away as possible.
I have done tests by putting my supply on top of a 1000va toroidal transformer and can hear the negative effect to the supply. The sound becomes more harsh and mechanical.

In this implementation the choke is on its side, this significantly cuts down on coupling between the choke and the transformer. 
John S.

![image](http://www.computeraudiophile.com/attachments/f10-music-servers/11655-why-linear-power-supply-mac-lps-top-and-section-review.jpg)

The R-core in the JS-2 really makes so magic. Not only was the difference between a good toroid and the R-core obvious in the bass with a computer, but when powering a DAC the difference was top to bottom. I really hope that people will use our supply for things other than just the computer and peripherals.