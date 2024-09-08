# Max/MSP Patches, Abstractions, Externals, RNBO, VSTs, and Ableton Max for Live 

## br.delay.pitch



By Brian Riordan  
[guaguanco127@gmail.com](mailto:guaguanco127@gmail.com)  
[brianriordanmusic@gmail.com](mailto:brianriordanmusic@gmail.com)  
[https://www.brianriordanmusic.com/](https://www.brianriordanmusic.com/) 

Repository for br.delay.pitch, with all related files, can be found here: [https://github.com/guaguanco127/br.delay.pitch](https://github.com/guaguanco127/br.delay.pitch)  
Additional programs can be found here: [https://github.com/guaguanco127/plugins](https://github.com/guaguanco127/plugins)  


These files were created with Max/MSP version 8.5.6. 

## Links

[About](#About)   
[Ableton Max for Live Device](https://github.com/guaguanco127/br.delay.pitch/tree/main/Ableton%20Max%20For%20Live%20) To use inside of Ableton Suite   
[Max/MSP Abstraction](https://github.com/guaguanco127/br.delay.pitch/tree/main/MaxMSP%20Abstraction) To use as an abstraction within Max/MSP  
[Version History](#Version)      


## <a name="About"></a>About

This is a delay-based Max/MSP abstraction, and Ableton Max for Live device that introduces a pitch-shifter in the delay line. A low pass and high pass filter is included to prevent extreme build up of high and low frequencies within the feedback line. 

The delay line goes through a high pass filter set to 40 Hz, and a low pass set to 12,000 Hz. This is to prevent pitchshifted frequencies in the feedback line that from going too high or too low. 

Only works as an abstraction or a device. External objects and RNBO not available yet.  

**On/Off:** Turn the effect on or bypass
  
**Pitchshift:** Pitch-shift Factor in steps. -24. to 24. Default 0. Microtonal pitch-shifting is possible by using numbers in between integers. For example, -0.50 is pitch-shifted down by a quarter tone. This portion of the effect introduces a latency of 2048 samples. 

**Delay Time:** Delay time in ms. Between 0. and 1000 ms. It is important to note that the lowest possible delay time is actually the signal vector size in samples. For example, if the vector size is set to 256 samples (Which is approximately 5.8 ms at 44,100 sample rate) combined with the latency of the pitch-shifter  (Which is approximately 46.43 at 44,100 sample rate) then the shortest delay would be approximately 52.23 ms. Regardless of the perscribed ms delay time, this will be the resulting minimum delay. If the delay time is set to be above 5.8 ms, then the delay time will be the perscribed time plusthe latency of the pitch-shifter. 
  
**Feedback:** The amount of signal that is fed back into the delay line. The range is between 0 and 0.99 

**Dry/Wet:** The amount of dry and wet signal between 0. and 100. The default is 100.  

## <a name="Version"></a>Version History  

Version 1.1 included a dc block into the feedback line on 05-14-2024. 

 