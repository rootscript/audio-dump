### UpTone Audio REGEN Power Supply Add-On


I guess it will be like the filter on the SqueezeUpgrade BoTWs power supply, The Squeezebooster?

Nope. Not in the least. 180-degree different direction. Not a filter; Not a battery; Not a like anything currently available.

---
IF it's only on the output side of the SMPS, I can't see how it can do too much about the RF/EMI that this and most other consumer grade SMPS plugpacks dump back into the AC mains supply?

You are right SandyK. And while SMPS dump high frequency noise back into the mains, most all conventional linear supplies (transformer/diodes/caps/regulator) put a lot of low frequency spikes back into the AC and flatten the sine wave a bit too. (Our big choke-filtered JS-2 does not do so--at least not the spike part for sure, I forgot what John told me about top of sine draw with it.)

So yes, the mystery PS product in development--whose primary purpose is to provide very clean and isolated DC to the REGEN (with a switch for 5V out too)--will not, if itself powered by an SMPS (7.5-12V/2A min.), address the issue of what that SMPS dumps back into the house line.

So for those people who have a system sensitive to all SMPS, there will be THIRD product, a rather radical little linear, just for feeding the new PS--that draws current through the whole cycle and does not affect the mains at all. Inspiration on some kooky-clever, never before done way of doing this came to John during a 3-hour phone session we had Friday night.

Sorry to be vague, but once again, another never before done (for any PS, audio or otherwise AFAIK) concept came from his amazing brain and is the sort of valuable IP that we don't want to talk about until we put it in a product for all to see/hear. Spelling out the concept means spelling out the circuits--not a wise business practice. 
[Though we did have a long talk about making some other designs public for both DIY and OEM licensing. Some of what we will be doing in the next year with power supplies is really bigger than just ourselves, and selling some core enabling circuits for this to be scaled in a multitude of ways makes good sense. While a whole line of products can come from this--enough to consume the energies (pardon the pun) of a small firm--we have broader plans and we can neither keep these power things entirely to ourselves, nor do we want to. So circuit licensing and boards may be the best release valve that does not just give everything away for free nor wait for others to copy.]

Of course with nothing announced and shown, all the above might just sound like blowhard posturing so I don't expect anyone to believe or understand the magnitude of the impact I think some of these innovations could have on power supply thinking and practice across the audio equipment spectrum.

We knew in advance that the REGEN was going to do what we expected, and before selling it I did not make over-the-top claims (in fact I tried to keep user expectations low because I was not sure if others would hear what we heard in our own systems). And we all know how that story turned out. 

So regardless of the sonic benefits of what we are working on (heck, neither John or I have even heard it yet, he is just sending off for the prototype boards to be made), I promise you that the concepts and execution are 100% unique and most everyone will say WTF with a big grin.

---

Alex, you mentioned this new gizmo would accept up to 12V. Am curious to know whether it can input 12V and output 9V (or 7.5V) to the Regen (since I understand the Regen should not be connected to 12V if the DAC's USB input is not self-powered) ?

Yes, output from the device will be 7.5V regardless of the input voltage. (Actually, plan is to have output switchable to offer 5V too, just to widen possible sale audience and application beyond just the REGEN.)

---

Alex, can you give us some feel for the size and weight of the 1A power supply? Do you have a prototype board yet? Would it sit on the shelf right beside the REGEN or down on the floor next to the Mean Well SMPS?

Presently planned enclosure (from the same series case as the REGEN) is 4.375 inches x 4.375 inches x 1.125 inches (without whatever sort of feet I decide to stick on it). Don't know the weight yet. 

Thinking that the cable provided (5.5mm x 2.1mm plugs both ends) will be 30 inches (76cm) long, but maybe we should go shorter. Actually have to decide on this fairly soon. Since there availability of decent gauge stock cables with 2.1mm plugs is pretty poor, I am planning to go ahead and have 1,000 made in China, and for that there is a lead time.

So people's input into a good compromise for DC cable length (between the new supply and the REGEN) would be welcome.
Would really like to do an 18awg twisted pair, but not sure if the houses that mold the DC plugs can handle that in their machines. The two choices seen out there are always zip cord or coax--and the latter usually in fairly fine gauge, though I do buy some 1meter 16awg coax with 2.5mm plugs from BixPower.com, so I know that some Chinese factory is doing cables with that.

Yes, the device will have just two "sockets"-- both 5.5mm x 2.1mm jacks. But I have to supply some cable to plug in between it an the REGEN. The device will not radiate any EMI/RFI at all, so having it near audio components is not a problem.

---

[link](http://www.head-fi.org/t/777678/intona-high-speed-usb-isolator/60#post_12345414)

If one wants to maintain total galvanic isolation when using an outboard power supply--without having to resort to batteries--the only LPS I am aware of which "floats" the DC ground (being isolated from the AC mains and chassis ground) is our own JS-2 choke-filtered, dual-output, 5-7A unit.  But at $925 it is a bit overkill for just a REGEN or the like.  Our forthcoming "mystery" 3.3/5/7V 1-amp supply will likewise be 100% isolated form the mains--both on the ground and in all ways (like a battery, but not a battery).
