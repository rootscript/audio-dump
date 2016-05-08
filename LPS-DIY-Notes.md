#LPS DIY information

Just a place to collate information about building a DIY LPS.

Please feel free to add any information you wish here:







### Links to LPS Projects & Guides:

[Link 01 - An inexpensive ($20), but high quality, LPSU for my Regen cascade ](http://www.computeraudiophile.com/blogs/daudio/moving-inexpensive-%2420-high-quality-lpsu-my-regen-cascade-warning-some-diy-688/)

[Link 02 - Powering a Regen cascade - one possibility (a 65VA eBay LPSU), including the 12V dilemma](http://www.computeraudiophile.com/blogs/daudio/powering-regen-cascade-one-possibility-65va-ebay-lpsu-including-12v-dilemma-687/)

65VA Ultra Low Noise linear Power supply

- 4 - U860 - ON Semiconductor ULTRA FAST DIODE (25 and 50 Nanosecond Recovery Time) (8A 600V) TO220
- 2 - 2SC5200 - Toshiba High power NPN epitaxial planar bipolar transistor (15A, 230V) TO-3
- 3 - BD140 - medium-power PNP transistor (1.5 A, 80V) TO-225
- 1 - (2S) K30a - Silicon N-channel junction FET (.01A, 50V) TO-92
- 1 - LM336-2.5 - Shunt Regulator Diode Voltage Reference (2.49V) TO-92
- 1 - NE5534 - Low Noise Operational Amplifier

### Op-Amp Based Linear Regulators
[link to notes](https://tangentsoft.net/elec/opamp-linreg.html)

####Why DIY a Regulator?

####How Does a Series Linear Regulator Work?

####Sophistication Begins: The Sulzer Regulator

####Sulzer Variations

####Sulzer-Borbely Regulator

####Jung Super Regulator

####Jung 2000 Regulator


---

###Archived page from http://waltjung.org/Regs.html

The articles listed below are involved with higher performance references and/or regulation stages 
for audio amplifiers and other solid state gear. They are listed in their order of appearance. Some of 
the very early articles are of mainly historical interest, but are included here due to the very strong 
interest in regulators.

1969: 'Don't Shun the Shunt Regulator' was published in the July 5, 1969 issue of ED, pp. 70-
72. This very early regulator used a 2N3638 reference, a CA3018 IC array and a 2N3055 as 
a pass device. Old parts, but still a viable technique with the substitution of more modern 
stuff.   [Dont Shun the Shunt Regulator](https://github.com/rootscript/audio-dump/blob/master/_PDF/Dont_Shun_the_Shunt_Regulator.pdf)

1974: 'IC Regulated Power' was published in The Audio Amateur, within issue 4 of 1974, pp. 
14-20. This article focused on the basic performance of the op amp-based series type 
voltage regulator. It included a PCB layout suitable for a complete +/- output 1.5A lab supply, 
using the LM395 IC as the pass device. Mine is still working after 30+ years!    [IC Regulated 
Power ](https://github.com/rootscript/audio-dump/blob/master/_PDF/IC_Regulated_Power.pdf) 

1994: 'Getting the Most from IC Voltage References' was published in issue 28-1 of Analog 
Dialogue, pp. 13-21. This article explores the basic operation of both series and shunt mode 
zener and bandgap type voltage reference ICs, as well as their specifications and 
applications.  [Getting the Most from IC Voltage References](https://github.com/rootscript/audio-dump/blob/master/_PDF/Getting_the_Most_from_IC_Voltage_References.pdf)

1995: 'Regulators for High-Performance Audio' was a four part series published in The 
Audio Amateur, within issues 1-4. This series goes into the design, testing, layout and 
system performance of audio regulators. Parts 1 and 2 listed below, were authored by Walt. 
Part 3 was authored by Jan Didden, and is listed below, courtesy of Jan. Part 4 of this series 
is by Gary Galo.

[Part 1 ](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regs_for_High_Perf_Audio_1.pdf) 
[Part 2 A](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regs_for_High_Perf_Audio_2_A.pdf)
[Part 2 B](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regs_for_High_Perf_Audio_2_B.pdf)
[Part 2 C](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regs_for_High_Perf_Audio_2_C.pdf)  
[Part 3](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regs_for_High_Perf_Audio_3.pdf)

1997: In 'Regulator Excels in Noise and Line Rejection', in EDN January 12, 1997 pp. 92, 93, 
a scheme of driving the op amp supply from the regulated output appears. The circuit is the 
basic positive regulator from the 1995 series (above), enhanced with a buffer/level shifter to 
allow the rail bootstrapping. Line rejection is enhanced considerably. [Regulator Excels in 
Noise and Line Rejection](https://github.com/rootscript/audio-dump/blob/master/_PDF/Regulator_Excels_In_Noise_and_Line_Rejection.pdf)

1997: 'Low Noise Power for Analog Circuits', was a 'Walt's Tools and Tips' column, within the 
ED Analog Applications Issue of June 23, 1997, pp. 65-68. This regulator version retains the 
scheme of driving the op amp supply from the regulated output, but is applied to lower 
voltages such as 5V.   [Low Noise Power for Analog Circuits](https://github.com/rootscript/audio-dump/blob/master/_PDF/Low_Noise_Power_for_Analog_Circuits.pdf)

2000: 'Improved Positive/Negative Regulators' was a upgrade and sequel to the 1995 article 
series on regulators. It was published in Audio Electronics, issue 4 of 2000, with 
photographic and other assists from Mark Kovach. [Improved Positive/Negative Regulators](https://github.com/rootscript/audio-dump/blob/master/_PDF/Improved_PN_Regs.pdf)