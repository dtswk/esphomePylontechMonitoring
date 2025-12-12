# esphomePylontechMonitoring

Sharing my working code based on a M5Stack AtomS3 Lite with the Atom RS232 base 

I wanted something simple and compact rather than solding up my own, it's my first time using the M5Stack and I liked it.  Clip together and good to go..!

What I hated was the doco wasn't very helpful and often misleading, hopefully this will save other people the hours I wasted.

**Learnings**
* Ignore the writing on the RS232 base the GPIO is as per my code
* The RX and TX from the base I think is flipped it references the device, either way copy my photo it works  :-)   
* I was overrunning the uart buffer as my newer batteries can be a longer string up to 16.  I've made the buffer larger to resolve that issue.  Default is 1500 I've set to 2048 increase if you have a larger battery system
* The cable to you make from the RS232 device to the pylontech I think needs to be relatively short, mine was originally 3 metres so I could stay near easy power, lots of errors, made that shorter ie 30cm and used an long USB cable problem resolved.

I take measures every 600s ie 10 minutes, so it will take awhile for the first reading, if you want an immediate one use either the devices webserver or in HA click the button to get an immediate reading.  Also feel free to modify the code.

https://docs.m5stack.com/en/core/AtomS3%20Lite
https://docs.m5stack.com/en/atom/atomic232

References
https://esphome.io/components/pylontech/

Note:  I have wired the RJ45 to 568B and therefore is Pin 3 white / green, Pin 6 is Green, Pin 8 Brown.  ESPHOME doco says white/green is RX and Green is TX, you will see that is opposite based on the R and T with the R5Stack...

<img width="557" height="849" alt="image" src="https://github.com/user-attachments/assets/f435d31a-0984-460a-b4c7-1ef67029b607" />

<img width="525" height="1075" alt="image" src="https://github.com/user-attachments/assets/ac4a19ec-edc3-4843-993f-58e1dc01b80a" />

<img width="525" height="1137" alt="image" src="https://github.com/user-attachments/assets/7891b1ea-cdee-4f65-8d11-5bef7e62d87b" />
