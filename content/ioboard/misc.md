+++
next = "/ioboard/assembly"
prev = "/ioboard/cartridge"
weight = 5
title = "Misc"
date = "2017-01-01T13:29:04-08:00"
toc = true

+++

#### Background

##### LEDs

330 ohm resistors are chosen in order to limit the current flowing through the LEDs to 10mA. The LEDs have a voltage drop of 1.8v. 

Therefore there is 3.2v across the resistor (5 - 1.8 = 3.2). 

V = IR, which can be rewritten as R = V/I. 

Plugging in 10maA as 0.01 gives 3.2 / 0.01 which is 320 ohm. 330 is a close enough value.

#### Components

| Component                | Description                                   | Image                    |
| ------------------------ | --------------------------------------------- | ------------------------ |
| 0.01uF Cap (2x)          | Bypass caps for level shifters                | ![Image](/io/0_01uF.jpg?height=100px)      
| LED (2x)                 | Battery / Status LEDs                         | ![Image](/io/led.jpg?height=100px)
| 330 ohm Resistor (2x)    | Current limiting resistors for LEDs           | ![Image](/io/330.jpg?height=100px)
| Reset Button             | Momentary Switch                              | ![Image](/io/reset_button.jpg?height=100px)
| 50 Pin Connector         | Female Connector to Main Board                | ![Image](/io/header_female.jpg?height=100px)