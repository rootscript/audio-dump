# gathered information about Linear Power Supply transformers

###John Swenson on the benefits of a choke-filtered linear power supply:

The choice to use a costly, custom, electrostatically shielded 100VA R-core transformer is highly beneficial to the JS-2 design.
Just powering the computer, **the difference—between the R-core and a toroidal transformer in the bass was shocking. And in comparisons powering a DAC or other audio-signal-handling component, the sonic benefits ranged top-to-bottom, cymbals and piano to deep bass.  Plus R-core transformers, due to the gapless construction of the core, are mechanically silent.**

The traditional cap only filter (transformer, diode bridge, big cap) produces raw DC with a sawtooth riding on top. That sawtooth produces lots of high frequency components that the regulator has to deal with. Traditional regulators do very well at low frequencies, but have lousy characteristics at high frequencies which means a fair amount of those high frequency components from the cap-only filter get through to the regulator. Fancy discrete regulators do well at blocking the high frequency components, but add cost and complexity to a PS. Our approach is to use a properly designed choke-based supply whose ripple is a perfect sine wave, no high frequency components, thus a traditional regulator works very well. The discrete regulator is not needed to deal with the high frequency components, since there aren't any.

All diode types except Schottkys emit a burst of ultrasonic noise as they turn off. This noise can go forward into the load circuit AND it can go back into the AC line, and it can also excite the transformer resonance. The "slow" diodes still have this ultrasonic noise. Schottkys are the only type which do not have this noise. Schottkys also usually have about half the voltage drop of other diode types and are usually faster. Which type to use depends a lot on what your supply looks like and what you are trying to optimize for. 
With a traditional low voltage design with a large cap right after a bridge you get large current spikes, these produce a large amount of high frequency noise which needs to be filtered by what comes after the cap. In this type of circuit the slow diodes can help cut down on the extent of the high frequencies generated by the sharp high current pulse. BUT they still generate the ultrasonic noise.

This is another reason why we like to use the choke-based design. With the choke there is no steep high current pulse, so no disadvantage to Schottky diodes. You get the advantage of no ultrasonic noise, lower voltage drop (so lower power consumption in the diode) and no big massive current pulses.

---

###Mains noise:
Noise can easily get through a transformer, both in transverse and common modes. Transverse noise is any noise or waveform distortion that is effectively superimposed on the incoming AC waveform, and this is coupled through the transformer along with the wanted signal - the mains.

Common mode noise is any noise signal that is common to both the active (hot) and neutral mains leads. This is not coupled through the transformer magnetically, but capacitively. The higher the capacitance between primary and secondary windings, the more common mode noise will get through to the amplifier. **The much loved toroidal transformer is much worse than conventional 'EI' (Ee-Eye) lamination transformers in this respect because of the large inter-winding capacitance. An electrostatic shield will help, but these are uncommon in mass produced toroidal transformers. The conventional transformer is usually better, and by using side-by-side windings instead of concentric windings, common mode noise can be reduced by an order of magnitude.**

---
### Notes gathered from forums:

As I understand it toroidals have lower magnetic leakage but higher inter winding capacitance. That makes them prone to slightly higher "noise" in the 60hz range. They can also be lighter for a given power compared to split bobbin transformers.

---
Toroidal transformers are a good example of being distracted by shiny objects and marketing hype. There was a time it was implied, and to some degree still is as evidenced by this thread, that unless the gear has a toroidal transformer it can't possibly be top tier or perform well. That's simply not true. Hence, do not be distracted by shiny objects.

**For dacs and source gear in particular, I'd rate them as follows in terms of suitability (from best to least):**
- **R-core**
- **EI core**
- **Toroidal**

**R-core have characteristics that are best suited for low level source applications.**

---
Someone here suggested that R-Core was better for Dacs. I went and checked and it seems that R-Cores are easier to make as the coil wrapping is less tight. The higher tolerance in the torroidal to get it right means that there is less EMI radiation coming off and that is a good thing in digital.
Is that evereyone's understanding?

What you have stated is mostly true. However, **the reason why R-core transformers are the best choice for ALL low level audio applications, is due to their far lower coupling. This means that any mains-bourn interference will be greatly attenuated by an R-core transformer, compared to a toroidal. E-I type transformers lie somewhere in the middle. Better than toroidals, but not as good as R-core types. And yes, radiation is higher with both R-core and E-I types, but that can effectively dealt with by either good shielding, or placing the transformer in a separate enclosure.**

But isn't mains bourne interference dealt with by chokes and capacitors?

It should be, but every bit helps. And **R-core transformers are around 100 times better than toroidals. They're not just a little bit better. They are spectacularly, brilliantly better. The reality is, that for anyone purporting to build the best product possible, then the best components should be used (within cost constraints, of course). I will remind you once more: Toroidals are the very WORST choice of power transformer for low level (audio) components. ANY transformer will make a better choice.**

* Shielding materials will depend on the desired outcome. The best shielding material is silver, followed closely by copper, then aluminium. Conductivity is the key to good shielding. Steel is way down the list. Magnetic shielding is best accomplished by 'mu-metal'. Mu-metal is around 5 times more effective than iron. Steel is bad news, due to magnetic remnance.
* Unless you have actually tried using an R-core tranny in a Lampi or VAD DAC, then you can never claim that toroidals are superior. Toroidals are used because they are convenient, cheap and require less shielding. They are not a superior transformer for a low level audio product. 
