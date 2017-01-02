+++
title = "Power"
date = "2016-12-31T20:09:57-08:00"
toc = true
next = "/mainboard/processor"
prev = "/mainboard"
weight = 1

+++

#### Boost Converter

Dodo is powered by 2 AAA batteries using the LT1303 boost converter to generate 5v from the 2-3v provided by the batteries. 

A few external components are necessary to complete the boost converter; a capacitor, a diode, and an inductor. The LT1303 is a switched mode power supply. Internally there is a switch that opens and closes rapidly. When the switch is closed, energy builds within the inductor. When the switch opens, the polarity is reversed across the inductor and suddenly it appears as if there are two separate voltage supplies in series, the batteries, and the inductor. The sum of those two is greater than the input voltage of the batteries alone, thus the voltage is boosted. The capacitor is necessary to supply the higher output voltage while the inductor is recharging. The diode is required to prevent the capacitor from discharging back into the power supply. A separate capacitor is also used across the input. Low ESR capacitors are necessary to increase efficiency. Dodo's boost converter is over 80% efficient with the selected components and carefully designed PCB.

#### Low Battery Detection

The LT1303 has a low battery output that pulls low when a minimum voltage threshold of 1.24v is encountered. 1.24v is too small for detecting low voltage across 2 AAA batteries, therefore a voltage divider is needed to scale a more appropriate threshold of 2v down to the 1.24v reference voltage. The 255k and 412k resistors form that divider. 1% resistors are chosen to ensure accuracy. The intention is to illuminate an LED under low battery conditions. The LBO pin only sinks a minimum amount of current, therefore the 2N3906 PNP transistor is necessary to drive the LED.

2v * (255k / 412k) = 1.24v

#### Batteries

Dodo draws just under 200mA at 3v which is a lot of current to be drawing from a typical alkaline AAA battery. Much better battery life is attained with either a lithium batteries, or better yet, rechargeable batteries. 

#### Circuit Diagram

![Circuit Diagram](/power.png?width=50%)

#### Components

| Component                | Description                                   | Image                    |
| ------------------------ | --------------------------------------------- | ------------------------ |
| LT1303                   | Voltage Regulator                             | ![Image](/lt1303.jpg?height=100px)
| 22uH Inductor            | Inductor for Regulator                        | ![Image](/inductor.jpg?height=100px)
| 150uF Cap (Low ESR)      | Output Capactior for Regulator                | ![Image](/150uF.jpg?height=100px)
| 100uF Cap (Low ESR)      | Input Capacitor for Regulator                 | ![Image](/100uF.jpg?height=100px)
| Diode 1N5817             | Switching Diode                               | ![Image](/1N5817.jpg?height=100px)
| 255k Resistor 1%         | Resistor #1 of voltage divider                | ![Image](/255k.jpg?height=100px)
| 412k Resistor 1%         | Resistor #2 of voltage divider                | ![Image](/412k.jpg?height=100px)
| 2N3906                   | PNP Transistor to drive Low Battery LED       | ![Image](/2N3906.jpg?height=100px)
| 100k Resistor            | Pull up resistor for open drain LBO output    | ![Image](/100k.jpg?height=100px)
| 1k Resistor              | Bias resistor for transistor                  | ![Image](/1k.jpg?height=100px)
| Battery Holders          | AAA battery holder                            | ![Image](/batteryholder.jpg?height=100px)
| Switch                   |                                               | ![Image](/switch.jpg?height=100px)

