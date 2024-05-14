# Max/MSP Abstraction: br.delay.pitch.abs-1.0  
   
By Brian Riordan  
[guaguanco127@gmail.com](mailto:guaguanco127@gmail.com)  
[brianriordanmusic@gmail.com](mailto:brianriordanmusic@gmail.com)  
[https://www.brianriordanmusic.com/](https://www.brianriordanmusic.com/) 
  
Repository for br.utility.stereo.1.0, with all related files, can be found here: [https://github.com/guaguanco127/br.delay.pitch.1.0](https://github.com/guaguanco127/br.delay.pitch.1.0)  
Additional programs can be found here: [https://github.com/guaguanco127/plugins](https://github.com/guaguanco127/plugins)

These files were created with Max/MSP version 8.5.6. 
## Table of Contents 

[About](#About)   
[What is an abstraction?](#Abstraction)  
[How To Install](#Install)  
[How To Use](#Use) 
 
 

## <a name="About"></a>About

This is a delay-based Max/MSP abstraction, and Ableton Max for Live device that introduces a pitch-shifter in the delay line. A low pass and high pass filter is included to prevent extreme build up of high and low frequencies within the feedback line. 

Only works as an abstraction or a device. External objects and RNBO not available yet.  

**On/Off:** Turn the effect on or bypass
  
**Pitchshift:** Pitch-shift Factor in steps. -24. to 24. Default 0. Microtonal pitch-shifting is possible by using numbers in between integers. For example, -0.50 is pitch-shifted down by a quarter tone. This portion of the effect introduces a latency of 2048 samples. 

**Delay Time:** Delay time in ms. Between 0. and 1000 ms. It is important to note that the lowest possible delay time is actually the signal vector size in samples. For example, if the vector size is set to 256 samples (Which is approximately 5.8 ms at 44,100 sample rate) combined with the latency of the pitch-shifter  (Which is approximately 46.43 at 44,100 sample rate) then the shortest delay would be approximately 52.23 ms. Regardless of the perscribed ms delay time, this will be the resulting minimum delay. If the delay time is set to be above 5.8 ms, then the delay time will be the perscribed time plusthe latency of the pitch-shifter. 
  
**Feedback:** The amount of signal that is fed back into the delay line. The range is between 0 and 0.99 

**Dry/Wet:** The amount of dry and wet signal between 0. and 100. The default is 100.   


## <a name="Abstraction"></a>What is an Abstraction?

An abstraction is a subpatcher that is saved as an external file, and can be used just like a standard Max object. As long as your abstraction can be found in the Max file path, you can type its name into a new object box and it will be loaded directly into your patch.  

By saving your logic in an abstraction, you can create modules that can be used in future work with little or no additional programming. This allows you to parlay your Max knowledge into more efficient work in the future, and will help you create programming systems that are modular and easier to maintain.

## <a name="Install"></a>How To Install

1. Make sure you have Max/MSP 8 installed in your computer. And, make sure you are using a Max patch that is inside of a folder.  

2. For the normal version of this abstraction, copy and paste br.delay.pitch.abs.1.0.maxpat inside of the same folder as the Max patch you are using.      

3. In the Max patch you are using, create an object called br.delay.pitch.abs.1.0 

4. Alternatively, you could also create this inside of a bpatcher object and use all of the preset UI objects featured inside the abstraction. To do this, create a bpatcher object. Then, go inside of its inspector, select "choose" next to "Patcher File" and select the br.delay.pitch.maxpat located within the same folder as your project. 


## <a name="Use"></a>How To Use

The first two inlets are for the left and the right stereo signals. 

The 3rd inlet turns the effect on, or bypasses the signal. It takes an integer of 0 or 1. The default is 1. 

The 4rd inlet is the Pitch-shift Factor in steps. -24. to 24. Default 0. Microtonal pitch-shifting is possible by using numbers in between integers. For example, -0.50 is pitch-shifted down by a quarter tone. 

The 5th inlet is the delay time in ms. It takes a float between 0. and 1000. The default is 100 ms. Please see note above about latency within the patch regarding the pitch-shift and minimum delay time. 

The 6th inlet is the feedback. It takes a float between 0. and 0.99. 

The 7th inlet is the amount of dry and wet signal between 0. and 100. The default is 100.  

Double click on the object and you can see inside of the object. This way you can study how it was built. 
    



 





