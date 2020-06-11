ArduinoLightbox (Improve compliancy with Altinak Generic Commands)
===============


What: LEDLightBoxAlnitak - PC controlled lightbox implmented using the 
	Alnitak (Flip-Flat/Flat-Man) command set found here:
	https://www.optecinc.com/astronomy/catalog/alnitak/resources/Alnitak_GenericCommandsR4.pdf

Who: 
	Created By: Jared Wellman - jared@mainsequencesoftware.com

When: 
	Last modified:  2020/05/11

Bug correction (replace 000 (numbers) by OOO (letters)
Change PWM frequency to 31 kHz

Typical usage on the command prompt:
Send     : >SOOO\n      //request state
Recieve  : *S19000\n    //returned state

Send     : >B128\n      //set brightness 128
Recieve  : *B19128\n    //confirming brightness set to 128

Send     : >JOOO\n      //get brightness
Recieve  : *B19128\n    //brightness value of 128 (assuming as set from above)

Send     : >LOOO\n      //turn light on (uses set brightness value)
Recieve  : *L19OOO\n    //confirms light turned on

Send     : >DOOO\n      //turn light off (brightness value should not be changed)
Recieve  : *D19OOO\n    //confirms light turned off.
