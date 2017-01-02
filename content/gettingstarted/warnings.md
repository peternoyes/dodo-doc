+++
toc = true
next = "/next/path"
prev = "/prev/path"
weight = 2
title = "Warnings"
date = "2017-01-01T15:10:29-08:00"

+++

- There are 4 components that look nearly identical, yet all are different BEWARE!
- The IC socket is intended for the EEPROM in case it ever needs to be pulled for reprogramming
- The electolytic capacitors are polarized. Be careful that they are installed with the correct orientation
- It can be tricky to install the larger ICs, gently bend the pins inward so that they can be inserted into the holes on the PCB. 
- Refer to the drawings on the PCB for correct orientation. Not all chips are orientated the same direction.
- The 0.01uF and 0.1uF capacitors may look nearly identical. They are distingushed by tiny writing of 103 for 0.01 and 104 for 0.1.
- The battery holders can be tricky to solder. The leads need to first be trimmed. A helping hands tool is very useful for holding everything in place. Be sure the polarity of the battery holders match the polarity shown on the PCB.
- There are two unpopulated components on the PCB; RESET and 5V. The main board of Dodo is designed to work as a generic single board computer without the game based shield that comes with Dodo. A reset butotn on the main board would be useful in the case that it is used by by itself. For this kit the reset button should be installed on the I/O board and should be left unpopulated on the main board.
