+++
date = "2017-01-01T19:00:54-08:00"
toc = true
next = "/next/path"
prev = "/prev/path"
weight = 3
title = "Memory"

+++

#### Background

Dodo uses a 32KB SRAM for system memory and a 32KB EEPROM for system firmware. Both chips happen to have the exact same pinout and both are connected identically, therefore only one chip is shown below in the diagram.

#### Pin Descriptions

| Pin(s)      | Discription                 |
| ----------- | --------------------------- |
| Address     | A0 - A14 address lines. Note that the 65C02 as an additional address line because the 65C02 has 64KB total address space. A15 from the processor is connected to the [glue logic](/mainboard/gluelogic).
| Data        | D0 - D7 data bus
| WE          | Write enable. Conneced to WR which is generated from the RW signal from the 65C02. See [glue logic](/mainboard/gluelogic).
| OE          | Output enable (Read). Connected to RD which is also generated from the RW signal
| CE          | Chip enable. From the RAM this is connected to the RAM chip select. For ROM, it is connected to the ROM chip select. See [glue logic](/mainboard/gluelogic).

#### Circuit Diagram

![Circuit Diagram](/memory.png?width=50%)

#### Components

| Component                | Description                                   | Image                                 |
| ------------------------ | --------------------------------------------- | ------------------------------------- |
| AT28C256                 | EEPROM                                        | ![Image](/AT28C256.jpg?height=100px)
| AS6C62256A               | SRAM                                          | ![Image](/AS6C62256A.jpg?height=100px)
