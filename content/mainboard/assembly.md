+++
weight = 8
title = "Assembly"
date = "2017-01-01T13:27:59-08:00"
toc = true
prev = "/mainboard/passives"
next = "/ioboard"

+++

![All Parts](/main/allparts.jpg?width=50%)

It is recommended to be familiar with soldering before attempting this kit. Here are some general soldering tips:

- Solder flows toward heat. Use this to your advantage by heating the plated hole as best as possible and pushing the solder into the joint. Heating just the lead will cause the solder to bead instead of flowing into the hole.
- Have a small amount of solder on the tip before soldering
- Do not use a wet sponge, instead use a brass cleaning sponge, this way you will not lose any heat.
- If using lead free solder, set to 750 degrees

![Soldering](/main/soldering.jpg?width=50%)

### Step 1 - ICs

There is no right order to assemble this board as long as all components are installed in the correct orientation. Below is a reasonable order that is not too difficult to manage. The order does not match the functional grouping of components, it goes by short components first followed by taller ones so that when the board is upside down the components are pushed flush against the board. ICs are relatively short, so they are a great place to start. For all of the ICs double check the orientation before soldering.

![ICs](/main/ics.jpg?width=50%)

#### LT1303

The voltage regulator should be done first because it is a tad shorter than the others

![LT1303 1](/main/lt1303_1.jpg?width=50%)

![LT1303 2](/main/lt1303_2.jpg?width=50%)

#### EEPROM Socket

The EEPROM socket should be soldered next. The EEPROM itself is the AT28C256 and can be inserted into the header at a later time.

![IC Socket](/main/icsocket.jpg?width=50%)

The board will most likely be unstable while doing this. Propping the board with a small item can make soldering easier.

![Prop](/main/prop.jpg?width=50%)

#### SRAM - AS6C62256A

By soldering the SRAM next, the board will now be pretty balanced for soldering the remaining ICs. It can be tricky to insert these larger ICs into the board. The pins need to be bent slightly inward before inserting, and it may take even more bending while simultaneously gently pushing the IC into the holes.

![SRAM](/main/sram.jpg?width=50%)

![Bend Pins](/main/bendpins.jpg?width=50%)

#### MAX202CPE - RS-232 Interface

![MAX202CPE](/main/max202cpe.jpg?width=50%)

#### 65C02 - Processor

![65C02 1](/main/65C02_1.jpg?width=50%)

![65C02 2](/main/65C02_2.jpg?width=50%)

#### 65C22S - Peripherial Adapter

![65C22 1](/main/65C22_1.jpg?width=50%)

![65C22 2](/main/65C22_2.jpg?width=50%)

#### 65C51 - Communication Adapter

Below shows inserting a chip from one side. At this point gently bend then pins inward while working the rest of the chip into the holes.

![65C51](/main/65C51.jpg?width=50%)

#### 74HC30 - 8 input NAND gate

![74HC30 1](/main/74HC30_1.jpg?width=50%)

![74HC30 2](/main/74HC30_2.jpg?width=50%)

#### 74HC138 - 3 to 8 Decoder

![74HC138](/main/74HC138.jpg?width=50%)

#### 74HC00 - Quad 2 input NAND gate

![74HC00](/main/74HC00.jpg?width=50%)

#### ICs are Complete

All of the ICs should now be in place!

![ICs Completed](/main/ics2.jpg?width=50%)

### Step 2 - Oscillators

#### 1.000mhz Oscillator - Main clock

The oscillators need to be installed in the correct orientation. 3 of the corners are rounded and 1 is square. The square corner needs to be aligned with the square corner on the PCB's silkscreen.

![1.000mhz 1](/main/1000mhz_1.jpg?width=50%)

![1.000mhz 2](/main/1000mhz_2.jpg?width=50%)

For the first time, leads need to be trimmed. Flush wire cutters work best.

![Flush Clippers](/main/flushclippers.jpg?width=50%)

#### 1.8432mhz Oscillator - Clock for the baud generator in the 65C51

![1.8432mhz](/main/18432mhz.jpg?width=50%)

### Step 3 - Switch

![Switch 1](/main/switch_1.jpg?width=50%)

To make sure the switch is flush against the board, it may need to be propped up.

![Switch 2](/main/switch_2.jpg?width=50%)

### Step 4 - TO-92 components

Be careful not to cause any bridges when soldering these components. The leads are spaced pretty close to each other. If you have a multimeter it might be worthfile double checking that there are no shorts. Also, these components look very similar, and there are an additional 2 TO-92 components on the I/O Board. Double check that the correct component is being installed.

#### DS1813 - Reset Package

![DS1813 1](/main/DS1813_1.jpg?width=50%)

![DS1813 2](/main/DS1813_2.jpg?width=50%)

#### 2N3906 - PNP Transistor for driving Low Battery LED

![2N3906 1](/main/2N3906_1.jpg?width=50%)

![2N3906 2](/main/2N3906_2.jpg?width=50%)

![2N3906 3](/main/2N3906_3.jpg?width=50%)

### Step 5 - Inductor

The inductor is not polarized

![Inductor 1](/main/inductor.jpg?width=50%)

### Step 6 - Header

It is best to use the male header for the main board so that logic analyzer probes could be easily hooked up

![Male Header](/main/header_male.jpg?width=50%)

### Step 7 - DB9 Connector

There are two large holes for the DB9 clips to hold it in place. These require a large amount of solder. To solder, move the iron and solder around to different sides of the hole to ensure it completely fills with solder.

![DB9 1](/main/db9_1.jpg?width=50%)

![DB9 2](/main/db9_2.jpg?width=50%)

![DB9 3](/main/db9_3.jpg?width=50%)

![DB9 4](/main/db9_4.jpg?width=50%)

### Step 8 - Electrolytic Capacitors

The electrolytic capacitors are polarized. The ground lead goes into the round hole. The positive lead goes into the square hole. Note that the capicitors look nearly identical but one is 100uF and one is 150uF. 

#### 150uF

![Electrolytic 3](/main/electrolytics_3.jpg?width=50%)

#### 100uF

![Electrolytic 1](/main/electrolytics_1.jpg?width=50%)

![Electrolytic 2](/main/electrolytics_2.jpg?width=50%)

![Electrolytic 4](/main/electrolytics_4.jpg?width=50%)


### Step 9 - Resistors

#### 255k

The 255k resistor is: RED GREEN GREEN ORANGE

![255k 1](/main/255k_1.jpg?width=50%)

![255k 2](/main/255k_2.jpg?width=50%)

#### 412k

The 412k resistor is: YELLOW PURPLE RED ORANGE

![412k](/main/412k.jpg?width=50%)

#### 100k

The 100k resistor is: BROWN BLACK BLACK ORANGE

![100k](/main/100k.jpg?width=50%)

#### 1k

The 1k resistor is: BROWN BLACK RED

??? missing picture

#### 3.3k

There are 3 3.3k resistors and they are: ORANGE ORANGE RED

![3.3k 1](/main/3.3k_1.jpg?width=50%)

![3.3k 2](/main/3.3k_2.jpg?width=50%)

![3.3k 3](/main/3.3k_3.jpg?width=50%)

### Step 10 - Diodes

The Diodes are polarized. There is a line on one side of the diode that matches a line on the PCB silkscreen.

![Diode 1](/main/diode_1.jpg?width=50%)

![Diode 2](/main/diode_2.jpg?width=50%)

![Diode 3](/main/diode_3.jpg?width=50%)

### Step 11 - Ceramic Capictors

The ceramic capacitors are not polarized, it doesn't matter the orientation that they are installed. There are both 0.1uF capacitors and 0.01uF capacitors. There are 5 0.1uF and they are all installed in the vicinity of the MAX202CPE IC. The 0.1uF have the number 104 printed on them. There are 8 0.01uF bypass capacitors that are installed next to each IC. They have 103 printed on them.

#### 0.1uF

![0.1uF 1](/main/0_1uF_1.jpg?width=50%)

![0.1uF 2](/main/0_1uF_2.jpg?width=50%)

![0.1uF 3](/main/0_1uF_3.jpg?width=50%)

![0.1uF 4](/main/0_1uF_4.jpg?width=50%)

#### 0.01uF

![0.01uF 1](/main/0_01uF_1.jpg?width=50%)

![0.01uF 2](/main/0_01uF_2.jpg?width=50%)

### Step 12 - Battery Holders

The battery holders are the trickiest part of building Dodo. First, the leads need to be trimmed.

![Battery Holders 1](/main/batteryholders_1.jpg?width=50%)

![Battery Holders 6](/main/batteryholders_6.jpg?width=50%)

To position the battery holder in place while soldering, either use a helping hands tool as shown, or place something a few millimeters tall under the board so that they battery holder can rest in place.

Allow a large amount of solder to flow so that entire pad is covered and the leads are encased in solder, this is to ensure that there is a strong mechanical connection for the battery holders.

![Battery Holders 2](/main/batteryholders_2.jpg?width=50%)

![Battery Holders 3](/main/batteryholders_3.jpg?width=50%)

![Battery Holders 4](/main/batteryholders_4.jpg?width=50%)

![Battery Holders 5](/main/batteryholders_5.jpg?width=50%)

#### Complete

![Complete](/main/complete.jpg?width=50%)




