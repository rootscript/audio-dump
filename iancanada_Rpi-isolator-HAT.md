#Rpi isolator HAT - [forum link](http://www.diyaudio.com/forums/pc-based/291261-something-cool-raspberry-pi-odroid-i2s-dsd-isolator-hat-native-dsd-decoder.html)

> I came up with a new idea: An I2S/DSD isolator HAT with optional native DSD decoder for Raspberry Pi and ODROID. 
> 
> It will have following functions:
> 
> 1. To isolate ground and all other signals between RPi/ODROID and audio system.
> 
> 2. Compatible with both RPi and OROID.
> 
> 3. Supports native DSD playback by plugging in an optional DSD decoder daughter board. The daughter board will convert DoP stream back into native DSD stream bit-perfect at real-time. In this case, all current SD image such as Volumio, MoodeAudio, RuneAudio, and most others, will have native DSD play-back features.
> 
> 4. Raspberry Pi DACs and other audio gears will work with ODROID (may need software support for configuration).
> 
> 5. Has isolated I2C control bus for RPi DACs, as well as optional I2C EEPROM ID bus. It will work very well with all RPi DACs and other audio gears by flowing Raspberry Pi HAT design specification.
> 
> Since I'm working on multi-channel I2S/DSD FIFO PCB, hopefully I can place a bulk order. 
> 
> Here is the block diagram:
> ![image](https://farm8.staticflickr.com/7768/26903537231_a7479f990f_o.png)
> [iancanada]

Can other PI HAT DACs be put on top of it??
Or at least would there be a "plug-in" option for a small DAC chip as used by HifiBerry IQaudio asf. 

I understand that the main intention behind this project is to provide external I2S DACs
with a quality streaming interface.

However. There is huge number of users out there using and loving HAT DACs because of their simplicity. Usually price/performance ratio is outstanding with these DACs too. 

At least from my perspective it would be nice to have a simple stack and forget "transparency layer" that cleans up the mess between my PI and my HAT DAC. 

> This Rpi isolator HAT is originally designed as "transparency layer". That means all current DAC HAT, such as HifiBerry DAC, DAC+ and DAC Pro, and meany others, will work with this isolator as if there is without this isolator. No any additional overlay or software support will be needed.
> 
> By following foundation's HAT specification, all DAC can be stacked on top of my RPi isolator. Because all GPIO connectors and dimensions are as same as a RPi.
> 
> So, all RPi DAC users can enjoy this isolator by just simple stacking it over a Raspberry Pi, then their DAC HAT.
> [iancanada]

So it will work where the DAC HAT is master for BCLK/LRCK, (eg. HB DAC+ Pro, Digi, Takazine SabreBerry32), feeding those signals from the HAT to the Pi, rather than receiving them from the Pi? (Even with the FPGA DoP->DSD?)
[clivem]

---

Will both the 3.3v and the 5v feeds to the stacked Rpi HAT DAC be isolated from the Rpi and fed regulated power from your isolator?

> Yes, both new 5V and new 3.3V power will be fed into RPi DAC HAT that stacks on top of the this isolator board. New power supplies are 100% isolated from PRi. Linear power supply would be highly recommended in this case.
> [iancanada]

