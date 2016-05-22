### AC Filtering, Grounding Boxes, Linear PSU and Balanced Power. [link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/)

I am building an AC Filtering device which has one inlet, several outlets, each along a filter path. This should help prevent some of the noise re-injected into the mains by some of the switching-mode power supplies from affecting the other components.

The design is rather simple:

Inlet + Inlet filters -> Rails -> separate Filters for each outlet

On researching and building this, however, a lot more questions cropped up not just about the AC Filtering, but about alternate approaches or additional devices, and general use.

1. I could use duplex outlets, but if I were to plug two devices in one of these, would one device be well isolated from the second one?

2. I believe I'll benefit by plugging the iMac into it, but I think I would need to build a new, properly shielded power cable for it to keep the benefits of the filter box.

3. If I plug my amp in the filter box, then the line sees a 'pre-filter' before heading into my amp's power supply. I believe this could potentially be good, but it could also be detrimental to dynamics.

4. If I use that filter box, will I still derive cumulative benefits if I install Linear PSUs? I think this is a 'yes'.

5. If I use balanced power (like Equi=Tech or an isolation transformer), do I get cumulative benefits with the filter box? With the filter box and LPSUs? Or could the installation of balanced power replace some of this arrangement?

6. Currently, in the arrangement for stereo, only the iMac is grounded: 
External HDD -> iMac -> DAC -> Amp. Theoretically, this should be OK, but I do hear some high-frequency hash that diminishes timbral accuracy for cymbals and the like, and proves fatiguing in the long term.

During my recent readings, I was reminded of the importance of the Ground Plane in DIY Ham radio circuits. In equipment which has not been designed properly, this is not well implemented. Thus, we often find ourselves with a mix or properly and improperly designed equipment, each with their own grounding scheme, each with either a two-prong power cable or a 3-pronged one.

Could this be the explanation why some people report getting much better results using grounding boxes? Take for example two commercial products which are very expensive and out of my budget:

1. Tripoint Troy - Grounding box used for chassis grounding for all components of your playback chain. This connects through a Ground pin only to mains.

2. Entreq Tellus - Autonomous Grounding box initially reserved for grounding Signal returns (e.g. an RCA return from each of your components). This doesn't connect to any other ground or earth, it has its own internal ground.

Are our power lines, grounding schemes, power supply units are compromised in various ways and greatly spoiling our enjoyment of music?
[YashN]

---

Normal mains filters may not be as efficient as a specially designed heavy duty filters that also take into account SMPS rubbish coming back the other way ?
[sandyk]

Certainly, and I'm not trying to compete with commercial offerings here.
I'll definitely separate analog and digital and perhaps small power from big power.
Since each line in my filter box has its own filter, each component will have less opportunity of affecting the other components.
[YashN]

Now the thing is between the original Tripoint Troy vs the Entreq Trellus is that the Tripoint was geared towards chassis grounding only, whereas the Entreq was geared towards cleaning up Signal only.
The thing is, the theory tells up the closing of the loop looks for the least impeded pathway. But is our common implementation close to the idealised theoretical aspect?

Secondly, note that the Tripoint does connect a ground pin to an outlet ground (it does have the two other pins to but these aren't connected inside the device, they are just there for mechanical stability at the outlet).

The Entreq, on the other hand, has no such connection back to an outlet... it's autonomous in that way. Still trying to figure out how this works.
at first I was concerned only with my AC filter, but the more I read and researched, the more I think all this is inter-related.

Some people have even reported great results using both products, i.e. the Tripoint Troy for chassis grounding, together with the Entreq for signal clean-up (grounding might be a misnomer here).

the Tripoint Troy is meant for connecting each of your components' chassis to it. The device also connects to mains Earth.

The difference is that **the Entreq wasn't planned for chassis grounding at all, just signal clean-up. 
Moreover, the box doesn't connect to mains Earth**. In this respect, it's more intriguing than the Tripoint.
[YashN]

Any thoughts on what secret method they use for this signal clean-up?
[Speedskater]

for Entreq, the box specifically is said by the manufacturer to deal with 'stray currents which are low voltage but high-frequencies', not low frequency.  Apparently it only connects in such a way as to clean up the signal (they use a free RCA or XLR, and purportedly only connect the ground in these).
[YashN]

	The return current takes the lowest impedance path. At low frequencies (good old 60/50Hz) the dominating factor is usually the DC resistance of metals, so silver would be better than copper, IF you had the cross sectional area of both metals. But making the copper wire a little thicker does the same thing for a much lower cost. 

	As the frequency increases the inductance of the path starts becoming more important than the DC resistance, this transition happens at fairly low frequencies, it starts at about 1KHz and by 15KHz inductance is significantly more important than DC resistance. From 15KHz up to several MHz the cross section of the metal and dielectric are important in the inductance. Getting above that skin effect comes into play and the geometry of the outer surface and dielectric become of prime importance. 

	So things like buss bars and thick wires may be important for noise issues with low frequency c
	[JohnSwenson]
[link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index3.html#post441270)

Some nits to pick:

*The return current takes the lowest impedance path.*
The return takes all available paths! In inverse proportion to their impedance. And therein lays the ground-loop problem.
So let's make it:
Most of the return current takes the lowest impedance path.

*so silver would be better than copper*
But it would be a poor engineering decision to do so.

*the geometry of the outer surface and dielectric become of prime importance.*
Yes, flat, wide, thin copper strips (or maybe braid) are good choices.

*So things like buss bars and thick wires may be important for noise issues with low frequency components, they are not that important for higher frequency components.*
True about the thick wires, but bus bars are an ideal choice at higher frequencies.
thoughts

	"The Entreq Silver Tellus is a wooden box, the size and weight of a small power amp. It contains inert minerals and a grounding plate."








Get some copper plates, Rochelle salts and Silica gel -- mix the salts evenly with the gel (beads) and place between the copper plates. Seal the arrangement. connect it however you think. Let us know how it sounds

With a high quality amplifier and sufficiently efficient speakers (>100 db) you can often hear a very faint hum -- you may need to use headphones -- and be very sure to use grounding plugs on the inputs or else you will blow your headphones apart. (Connect the headphones to the amp output with adapter cables) You may be able to hear the background noise level. If you can, you can use this setup to easily test noise levels.
[link](#521)

Method and product for reducing distortion in an audio or home theater cable
[link](http://www.google.com/patents/US6545213)

---

This looks a little more like what Sam Lord was describing:

Ferroelectric field coupling device for improved noise reduction in AC power lines
[link](http://www.google.com/patents/US8658892)

*A couple of questions come to mind here: how would the massive increases in instantaneous current be brought about? Quite intriguing. Secondly, to prevent the piezo effect in the other direction, one would need to isolate from vibrations quite well, isn't it?*
[YashN]

Yes a piezoelectric material can send and receive. But having a large quantity of it around a conductor will act as a sink. The different sizes and masses of each piece, along with noncrystalline distribution, mean that lots of RF radiation is converted to kinetic energy then dissipated in the mix as heat. But some through various means gets reflected back to the conductor, I'm not sure in what proportion (I assume tiny). Hysol potting compound is mechanically quite lossy so that works well, but for an adequately flexible cable filled with loose FeSi pellets, the friction and piezoelectric absorption between the pellets dies a good job. I don't know whether current Shunyata NICs are potted or have loose pellets.
[Sam Lord]

*I just read that he incorporated a new design in his Denali products, stemming from the very good results he had in the medical industry.*
[YashN]

Wow, I didn't see that line, brand new. Denali was the last speaker ($65k/pair) we used when we showed with Shunyata at CES 2002. I haven't spoken with my former partner Dale Pitcher in many years, so I don't know if Caelin just liked the name or what. Anyone remember the million-dollar-system room? Speakers were Wisdom Audio, dunno about electronics, and Ted Denny of Synergistic was in charge. Some of their team, I don't know who, heard the effect of the Shunyata Hydras (6-outlet AC power units), so Caelin let them use some number in the room. Denny went ballistic when he saw them, and ordered people to hide the damn things as they weren't his creations. They did a job, but I was told by many that the system sucked anyway.
[Sam Lord]

*Yes, from what I read, the material is as you described.
As for Quantum effects, at very small-scales we can't ever get away from these, but here again, just as saying 'stardust', mentioning them for a product can conjure aromas of marketing rather than substance.*
[YashN]

My thought about stardust had nothing to do with quantum mechanics, it was simply a marketing idea. You can hear and feel FeSi in the Shunyata power cords that use it, so I thought it would be useful to note that the stuff is an important part of the product. It is not expensive, we bought barrels of it: looks like a sea of tiny pearls. For the Hydras we potted the FeSi with Hysol, I don't remember which one. I mention this now because the FeSi information has been public for quite a while now.
[Sam Lord]

*Funny, I have this exact Shunyata balanced cable connecting my DAC to Amp. I always wondered what was in the hoses. Thanks!*
[lmitche]

No, FeSi is only used in or near power products, it will change (degrade) the performance of an audio circuit in close proximity.
[Sam Lord]
[link](#532)

*Sam, the first Caelin patent that Jud posted shows an interconnect cable surrounded by two concentric tubes with FeSi material in the outer ring. I have a pair of Shunyata Antares cables constructed in the same fashion. 
Perhaps the material degrades the signal, but they sound pretty good to me.*
[lmitche]

Hi Imitche,

I'm trying to find which patent. Descriptions of Antares don't mention the FeSi shields but everything else....could you show it to me? Please accept that I'm not saying this to doubt you, because there are lots of variables involved. There are many sizes if FeSi crystals with piezoelectric action at selectable frequency ranges, so the idea isn't crazy, it's just that I never saw it. But Antares was developed long after Shunyata parted ways with Essence/Intuitive Audio. Only Caelin warned us not to use certain FeSi close to our audio circuits. And none of the early interconnects or speaker cables used it. Do you hear the sound of sand as you move it?

Ah, now I found it here, thanks Imitche. Those are the same pellets we used in the Hydras, 1-3mm diameter:

"The silica gel beads 28 are a colloidal form of silica, synthetically manufactured from sodium silicate. The silica gel beads 28 are glassy, hard, and somewhat irregularly shaped generally spherical granules that are clear to milky in color. They have an amorphous microporous structure providing a large surface area and a large number of micro-crystalline structures and edge boundaries that provide improved performance. This is because the edge boundaries are believed to cause the radiated electromagnetic field to be diffracted, refracted, and reflected within the structures which aids in disrupting and dispersing the high frequency noise components.

Depending upon the application, either the rochelle salt 29 or the silica gel beads 28 are used (by themselves) to form the ferro-electric substance 26. For other applications, they may be combined together in any preferred ratio.

The formulation that is used affects the audio performance of the audio cable 10. The silica gel beads 28 end to improve the lower and mid audio frequencies (below 1 Khz) while the rochelle salts 29 are especially effective at the higher audio frequencies (above 1 Khz).

The diameter of the silica gel beads 28 that are used varies depending upon the size of the audio cable 10. Their size is commonly referred to as a “mesh” grade. A 1-3 mesh is often preferred and it includes the silica gel beads 28 having a diameter from 1-3 mm. For small interconnect cables a custom made size, of 16 mesh is preferred and it includes the silica gel beads 28 with a diameter that is less than 1 mm."

Well that corresponds well to my recollection. It looks like Antares was not continued. I asked Caelin about trying FeSi shields around audio cables, but he was convinced back then that they wouldn't work.

That was a pattern. Right from the start of designing the Hydra, I said that the pellets must be piezoelectric material to covert electric field noise into kinetic energy and from there, heat. But they said no, don't talk about this, there's more to it, etc. Well there was a bit more, I didn't know nearly as much about B fields then, but I had the basic idea. The purity of copper was an intense concentration, it cots a lot. My suspicion is that any magnetic impurities like iron must have a compounding effect, not exactly predicted by simulation, on overall transfer function of the devices...it's not an obsession, but rather observation from his earlier work. 

Current descriptions of Antares don't mention any ferroelectric materials, but do mention the patent, so that's it. Interesting that Shunyata didn't trumpet the feature. I don't think they are found in any current audio cables. Now, the new Ztron patent copy describes the use of shields surrounding each conductor and connected to an inverted voltage, AFAIK, supposedly to stabilize the behavior of the dielectric. A very elaborate type of balanced cable, as if on steroids, clever. I imagine this would work best with very-low-Z sources. Anyway people like it. 

Thanks for the correction.
[Sam Lord][link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index22.html#post528547)

*...Thanks for the additional info, it does look like in the patent he focuses on the electrical field and how losses are induced from there... ...I was also thinking of the magnetic field component and the impedance to high frequency content. Maybe the missing explanation can be found there.*
[YashN]

Well, the action of the bulk FeSi made sense for both the electrical and magnetic fields, but the behavior of the plates was the challenge. Just very pure, thick, polished copper of a certain shape was necessary, but it exceeded expectations.
[Sam Lord]

*If the effect is real, which it certainly might be, I've suggested a way that you could measure. Piezoelectric effects are eminently measurable, as is background noise. This is all conventional electronics... ...I have suggested a measurement that might demonstrate any real effect. So?*
[jabbr]


So have I, and one of my failures at Essence was not to heed Caelin's request to use our very good equipment to work to characterize the action of Hydra power distributors. A series of null tests would have given us useful numbers. But other duties had precedence, and I knew he would deal with it when necessary. While the transfer function of a Hydra was not anything you could easily approximate analytically, it was quite drastic. It brought up perceived level by around 2dB and often caused walls to newly shake with no change in the level set. This from a passive device with almost negligible reactance.
[Sam Lord]
[link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index22.html#post528838)

	No prob., Sam. Hope this is all cleared up between you two so that we can go on to the non-personal and interesting stuff.

	Speaking of plates, here was my thinking initially for my AC Filter box:

	I would have one single copper plate for the common ground underneath the filter lines as this would be a proper ground plane versus wires connected to a rail.

	This ground plane would also be used to connect to a set of chassis grounding binding posts in the same box.

	Now, I was also thinking of integrating the Signal 'grounding' technology in the Entreq within the same box instead of making two boxes. And since the Entreq uses a plate, I was then thinking of using two such plates.

	Thing is, if I use the two plates in close proximity, there may be some unwanted interaction (or at least that's how I view it) which I would like to avoid, so here I thought that perhaps using sufficiently large distance between these two plates could be helpful.

	An alternative would be to set up two cylindrical chambers, one for each, and isolate these.

	In this configuration, I lose the traditional ground planes, so perhaps if I implement them this way, I need to think of a good way to make a hierarchical and symmetrical star-grounding scheme. [On second thought this needs some more thinking as I certainly don't want to make a ground loop available here].

	What do you think, are these good ideas?
	[YashN]
[link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index22.html#post528975)

And as I have mentioned previously, not necessarily Maxwell, but there could be explanations in the micromagnetics domain too. And perhaps closer to the macro domain, any losses related to the magnetic field and a radical increase in impedance there and not just the electric field as mentioned in the patent. Not many people know about this effect as it's quite new, and personally, I can visualise it within the context of a DC field and a single alloy connector, but so far find it hard to visualise clearly within the context of the NIC.

What exists in the patent is the following:

- the chamber, 
- the parallel connection, 
- the material,
- the induced fields therein,
- the E appears to be catered for in terms of explanation 

but no details about the B given.

If the explanation can then inform a design, then that would be awesome. I'm not too concerned about it though because in this thread and quite early, I did a very, very rudimentary form of signal 'grounding' which added to the other enhancements (AC Filter box + Chassis Grounding) gave us the very best sound we ever have heard here.

So, in the end, I'd sooner just build a couple of NICs or just two grounding planes (or any combination thereof) rather than forever try to find explanations and measure them (I have no reason to doubt the 'massive increase in instantaneous current' nor will I let any measurement here distract me) because if I got results with my very rudimentary solution, then it means that just the impedance matching or 'external grounding' was a worthy goal at least in my modest system (YYMV).

For info (already somewhere in a past post in this thread), the rudimentary solution was just using flat braided cables to a small hollow copper tube: I had the plan of building a proper NIC with it, but this time all I did as a first test was just connect the braided cables (one to my amp, one to my DAC).

Now, you can imagine just what a proper Shunyata (or similar) solution or a proper NIC or two could do (here again in my system).

In other words, I view this arrangement as the following:
[Impedance Matching] + [Cleanup due to E field] + [Cleanup due to B field, potentially]

with each adding incremental (but not necessarily small) gains.
[YashN]
[link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index23.html#post529813)

*... in any case if we describe a grounding box as a type of capacitor in parallel with the ground ... with low internal impedance ... and with a particular type of dielectric then I can better understand what is being talked about.*
[jabbr]

	As the thread is packed with info (still worthwhile to read through, taking care to avoid the crap posted by Daudio and One and a Half, and side-stepping some of the less helpful posts by Speedskater and sticking to his other very helpful resources), here's a quick summary:

	- Probably Post #1 is good to read as starting point, namely I was looking to just build an AC Filter box, but then along the way, many more questions arose spanning the audio system view.

	- I started with a Jon Risch Filter design, which is quite simple and using ferrite rods

	- Then I read about some of Lukasz Ficus's iterations

	- My own circuit is similar to Lukasz's but I avoid a couple of things he integrated in his

	- There's also a parallel circuit by Thorsten Loesch in the thread

	- My own Filter box continuously wants to grow

	- Researching the matter brought us to discuss Grounding/Chassis Grounding and signal 'grounding', especially in the Tripoint and Entreq devices, as well as Balanced Power, Isolation Transformers, Balanced Interconnects, etc...

	- I wanted to inform the design of my AC Filter box on a pure Engineering/Science perspective (i.e. no consideration for budget/business/marketing side issues)

	- Other designs that I looked into: the Steve McCormack device, and Caelin's devices

	- I want to integrate the Chassis grounding in my AC Filter box (easy), as well as the signal 'grounding' (easy to do but not easy to integrate IMO). Imagine for simplification that we are mainly externalising the ground plane and the signal ground plane of our equipment into that single box: the question becomes how to integrate these two plates in my design geometrically, mechanically and electro-magnetically for the best results.

	- As for Balanced Power and Isolation Transformers, our friends Zilch0md and lmitche have done a lot of experiments and are far ahead of me in experimenting with them.
	[YashN]

[link](http://www.computeraudiophile.com/f8-general-forum/ac-filtering-grounding-boxes-linear-power-supply-unit-and-balanced-power-24916/index23.html#post530208)

Here's Lukasz's schematics for his Silk AC Filter:

![image](http://lampizator.eu/AC%20FILTER/SILK/silk220.JPG)

*C1 = any size from 0,1 to 0,22 uF / 250 V x rated or 630 V non-x rated. Soldered directly to IEC socket. 
L4 - finger type ferrite rod, 10 wire turns. 2,5 mm solid copper wire (green/yellow stripes). Tinted copper ends. 
L1 - ferrite ring, preferrably 3001 material. From C1 to L1 - wires tightly twisted (2,5 mm solid core). 
L1 Winding: two wires wound tightly around core together 3 1/2 times) (not like on the drawing, but both wires side by side). 
L2 and L3 - finger sized ferrite rods - 3 turns of each wire. OMIT (skip) these for amplifier outlets. 
C3, C4 - 0,01 uF (10nF) X or Y rated foil caps (wima is very good). or 630 V non x rated. 
MOV - 275 or better 300 V DC, biggest energy you can find. (big and thick look is a good sign). MOV directly on the AC outlet. 
Earth continuity switch: put in on all outlets except one, which must be allways in use (be it an amp or mono amp). 
Everywhere possible the N-L wires should be twisted.
	If making more than 1 outlet, the C1 and L4 are common. Everything else duplicate. 
remember to solder-tin all copper ends to prevent corrosion. Use tons of hot melt glue to secure everything.
	I recommend at least 24 hr burn in and break in under real (or much bigger) load before critical evaluation.*
	[link](http://www.lampizator.eu/AC%20FILTER/SILK/SILK.HTML)

On this one, there is an inductor on the Ground lead, and coming from the inlet, the caps between Ground and L and N are after the inductor.

Additionally, the L2 and L3 ferrite rods are omitted for the amp outlet.

Lukasz mentioned on AA around 2000 that he had some great feedback on his latest filter incarnation. Whether this is the same as the 'last design' above isn't known, but his filter appears better than what I am doing currently, which seems a hybrid closer to Jon's design.

He also added some switches to selectively disconnect GND from some of the outlets for certain devices:

![image](http://lampizator.eu/AC%20FILTER/SILK/filter30.jpg)

My circuit is similar to his, but has no inductor on the common ground line, and has no switches on the individual Ground to socket connections.

The rest of my design have parallels in the Shunyata and Steve McCormack designs.

Considering the audio system, where great benefits can be derived from using a dedicated line (done), balanced power (not yet explored), isolation transformers or other AC filtering, proper grounding, better power supplies and better amps, it sounds like it is a very daft thing to lose all that ability in a common weak link.

More and more, in my system, this weak link is nagging at my mind (as these things usually do) and it's the RCA and non balanced interconnect there.

Now, I just built my Single-Ended Tube Amp, so I am going to listen to this for a while, so buying a new DAC and a new Amp is not of the order of the day, because that's indeed what I would have to do to get a pure Balanced connection between these two and that would be a hefty price.

So, instead, what I thought about is make a pseudo-balanced connection. For this, I would have to put the DAC circuit in a larger chassis, and then use XLR connectors on it and the AMP. Thus the shield of the new balanced cable would actually be a shield, and the small signal return will then be inside that. We'll avoid the Pin 1 problem by architecting this properly as well.

Those small signals can be affected very easily (the proportion being big since the signals themselves are small) in the normal and flawed return-as-shield interconnects, as well as having the metal of the RCA connectors exposed to any RFI/EMI. Then we are amplifying these, together with the noise profile.
[YashN]

