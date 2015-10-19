============================
C64 PS2-USB Keyboard
============================

**WORK IN PROGRESS**

**This is an early incomplete version**



This project is designed to allow a PS2 or USB keyboard to be used
with a Commodore 64/128 in place of the original Commodore keyboard.


Hardware
--------
* Arduino Uno (PS2 Only) or Arduino Due (PS2 or USB)

* MT8812 or MT8816 Analog Cross switch

* 20 pin female header or male header with cable (PATA cable will work)

* Arduino shield PCB. 
	- Any universal PCB that will line up correctly.

* PS2 keyboard 
	- matching socket or cut/strip and directly wire.

* USB Keyboard
	- USB Type A female to Micro B male adapter.


Documents
---------
* MT88XX.xml
	- Basic wiring chart.
	
* KEYBIN.xml
	- MT88XX AY/AX - Commodore header table.


Usage
-----

* Copy the C64keyboard sub-folder into your Arduino library directory.
	- Typically in windows this is located in your user document directory under: \Arduino\libraries

* Using the Arduino IDE upload the sketch: C64_keyboard.ino : into your Arduino.


!!!POWER REQUIREMENTS!!!!
-------------------------

* The Arduino UNO can be powered from the C64 keyboard header Pin 4

* The Arduino DUE CANNOT BE POWERED FROM THE C64 KEYBOARD HEADER! It will be unstable.

* Currently I am using a cable with clips and barrel connector to the power port on the Arduino.

	- I am connecting the positive(center) to the + side of C19. This is about 10V unregulated.
	  A regulated power source is not needed as the Arduino regulates the power from the power port.
	  
	- Pulling off the 12v regulator has been suggested. However, it appears to cause noise
	  and I have difficultly with the programming connection in this configuration.
	  
	- Suggestions for other places to get the 7v-12v power supply are welcomed. Again this does not need to be regulated.



	
Version 0.5
-----------

* Early release!!!

* USB support not included.

* Some timing issues still exist.

* Not optimized or fully commented.

* Modularity for easy keymap implementation needs to be added

* Not all keys are programmed!! Mostly positional at the moment.


