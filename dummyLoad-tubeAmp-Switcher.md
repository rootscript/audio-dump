##Tube amplifier switcher (with dummy load)

The first order of business was to get the speakers off-line during power up. I set up the transformer outputs on relays and dummy loads. The relays are manually actuated with a switch, but it would be a simple thing to do to set them up on the control system to come on when the High voltage stabilizes. The picture shows not very well at all how I jammed them in there.

![image](https://www.sparkfun.com/images/tutorials/Amp/Amp-3.jpg)

The two orange guys are the relays, and the big fuzzy gold-looking resistors to the left and right are the dummy loads. It?s a bad thing to run a tube amp without a load. And while it?s unlikely that any audio will be going through the thing during power up, you never know. Better to be safe.

[link](https://www.sparkfun.com/tutorials/89)

---
Q:
Why is speaker load needed on a Tube Amp?
Can anyone tell me why it is said with tube amps "do not power up amplifier without any speakers connected"

A1:
The output transformers are "transforming" the load found on the secondary to the primary. As the 
transformers are close to lossfree, an open secondary will be mirrored as a very open primary ( from AC ),
it will become a coil ( choke).
Any current changes in the tubes will cause a huge voltage ( breaking a current in a coil will 
cause the collapsing magnetic field generate a huge voltage. Just like a ignition coil)
Some amps will stay stable, some won't. And even the ones that seems to be stable will
generate huge voltages when a signal or a "pop" from mains is amplified in the amp.

The short summary : Always have a load on a transformer equipped amplifier. This goes also
for the small numbers of transistorized amps using an output transformer.

A2:
Note that a 100 resistor ( 5w ) connected on the 4ohm taps will protect an amp, causing 
negligible loss of power. Some amps has this from factory, some uses a "zobel" ( see wikipedia) that
does the same service.

[link](http://audiokarma.org/forums/index.php?threads/why-is-speaker-load-needed-on-a-tube-amp.702686/)

---

A1:
The problem is that transformers are a big tank of magnetic field driven by active devices. The secondary side of an OT is low voltage/high current by design, and is on the outgoing side of the tank. The primary is high voltage and low current, and is driven by devices that can go into oscillation, and is isolated from the transformer's M-field by leakage inductances which can both store M-field, and which prevent the active devices from having high frequency control of the M-field. The danger from open secondaries is from high voltage punch through by a couple of different syndromes, and the energy involved in a punch through doesn't have to be very big to start the chain of failures. It just has to make one hole at a weak spot. The next few thousand stresses enlarge the hole. 

It is FAR safer in switching speakers to tube amps to SHORT the speaker outputs, or even better to parallel up a dummy resistor load before the switch happens. This completely avoids the issue of starting a punch through or making it worse. Tube amps will be fine when shorted for short periods. Solid state amps may go nuts, so using a dummy resistor is the best design choice because someone, someday will hook up the speaker switcher to solid state amps. 

So a speaker switcher ought to (1) add on dummy resistors to the amp output, (2) make the switch of the hot amp output to the new speaker load and finally (3) release the dummy load on the amp. It takes some timing and some careful reading about relay switching times, but as you noted, you can speed things up a bit by using an SSR to connect up a dummy load resistor in the interval until the mechanical stuff has time to move.

A2:
This may be a good place to use a TrensZorb element which is a zener diode (back to back internal connection for AC) which limits the overhoot but does nothing until the voltage gets high enough.  That way, you don't have a continuous load from a resistor.  The capacitance may be an issue but antiparallel diodes in series would keep that to a negligible level.

There are also some make-before-break relays that could solve the problem with a momentary state of half the regular impedance.  Not good for solid state but not a problem for a tube amp.  There used to be a huge number of relay variations but these have disappeared over the years.  You might be able to bend a relay contact into a make-before-break on a standard relay.

[link](http://www.diystompboxes.com/smfforum/index.php?topic=109202.5;wap2)

---

###Other links:

http://forums.parallax.com/discussion/90907/any-tube-amp-experts

http://www.tonebone.com/headbone.php

---

Guitar industry solutions:

The **Palmer Triline** basically routes guitar signals to different amplifiers and functions as an active A/B/Y box. The Triline's universal design makes it possible to utilize various options:

1. A single guitar can be routed to either amplifier A or B or to both.
2. Two guitars can be routed to different systems, e.g. an electric guitar to a guitar amplifier, and an acoustic-electric guitar to a PA system via an integral DI box.

3. A dedicated output is provided to connect a tuner. The Triline can be muted for silent tuning.

4. Using an additional device (E-Frog), one guitar can switch between two amplifier heads. However, both amplifiers use only one speaker cabinet, i.e. the output of the amplifier in use is routed to the speaker cabinet. A load box prevents damage to the amplifier which is not in use.

The routing is done without any audible delay or clicking noise. The outputs to the amplifiers are tranformer isolated to prevent ground loops and humming. You can match the channel gain using the trim potentiometers. There is a special output for connecting up a tuning device. During tuning, the amplifier outputs can be muted.

**Palmer MI PGA 02** - Switching System 2 Guitar Amplifiers to 1 Cabinet for PGA01 - EX DISPLAY

Expands the functions of the PGA01 (Triline). Permits a loudspeaker to be operated with two amplifiers. To be used only in conjunction with the Triline. The Palmer "E-FROG/CABINET SWITCH EXTENDER" expands the functions of the Palmer TRILINE and may only be used in conjunction with it. Technically, it consists of two power relays and an8 ohms lad impedance. The relay routes the inputs AMPLIFIER A/B either to the internal or to the output SPEAKER CABINET. Since the amp, which is liked to the dummy load, doesn't receiveany input from the TRILINE the internal load functions simply as a guard against internal feedback, or it takes over an overhanging signal like reverb, etc. Consequently, the impedance only plays a secondary role, and speaker cabinets with 4, 8, or even 16 ohms may be used. Important is onlythat the output impedance of the amp is matched to the speaker cabinet.

---

https://www.youtube.com/watch?v=NRcKkc7IERE

