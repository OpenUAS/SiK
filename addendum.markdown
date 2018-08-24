SiK Addendum
=====
##New feature

An additional compiler flag is added **FLEX_FREQ** Defining this add a Change Main Frequency Feature at cost of a MAX_WINDOW can only use the default value

There is **NO** need to upgrade the Bootloader, so not need to fiddle with weird debugger hard and software

##WHY

sometime you want to use the hardware you have in another region of the world, most common you come from the US or Australia, and want to use it in Europe.
Then you can set you modem from 900range to 868range at the cost of some range, or vise versa ofcourse

##Is it really working

Read http://www.bytebang.at/Blog/Changing+the+frequency+of+a+HM-TRP+3DR+Radio

##Disadvantages

Most of the hardware has an additional tuned filter circuit. Realistically switching from  915Mhz to 433Mhz range... without new hardware filter, no, not really.

##HOW

The new parmaeter called "MAIN_FREQ" has the  following values that can be used:

 - 433mhz range	=       ( in HEX is: 0x43 )
 - 470mhz range	=       ( in HEX is: 0x47 )
 - 868mhz range	=       ( in HEX is: 0x86 )
 - 915mhz range	=       ( in HEX is: 0x91 )
 
##Example 

 ATS15=145 sets the main frequency to 868 MHz
				
Typical steps to change frequency are:

 - +++          (to enter AT commands mode)
 - ATS16=134    (to change MAIN_FREQ to 868 MHz)
 - AT&W	        (to save the new setting)
 - ATZ			(to reboot, yes, that is mandatory)
 
##NOTES
Please make sure to use correct Antenna for the selected frequency.
 



