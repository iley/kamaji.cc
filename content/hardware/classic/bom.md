---
title: "Bill of materials"
date: 2023-04-07
lastmod: 2023-05-06
weight: 1
---

__Work in progress. Please check back later.__

Here's what you'll need to assemble your own Kamaji Classic system.

Everything except the custom PCB can be bought from marketplaces (e.g. Aliexpress) or electronics components stores (e.g. Mouser, Digikey, Farnell).

| Item                                                         | How many |
|--------------------------------------------------------------|----------|
| [Custom PCB](#pcb)                                           | 1        |
| [ATmega328p microcontroller in DIP 28 package](#atmega328p)  | 1        |
| 1602 LCD                                                     | 1        |
| 12mm piezo buzzer                                            | 1        |
| RJ10 socket                                                  | 5        |
| BS-170 MOSFET transistor                                     | 1        |
| 2x5 right-angle IDC connector female                         | 1        |
| USB-A socket                                                 | 1        |
| USB-B socket                                                 | 1        |
| 0.1uF through-hole ceramic capacitor                         | 3        |
| 1K through-hole resistor                                     | 6        |
| 10K through-hole resistor                                    | 2        |
| 10K potentiometer                                            | 1        |
| 12mm pushbutton with cap                                     | 3        |


## PCB

<img src="/images/classic-pcb-top.jpeg">

For information on how to get the printed circuit boards manufactured, see [next step](/hardware/classic/pcb).


## ATmega328p

<img src="/images/atmega328p-pu.jpeg">

This is the microcontroller we're using, ATmega328p. It's a popular 8-bit AVR microcontroller which was used e.g. in Arduino Uno.

Make sure to order the ATMEGA328P<b>-PU</b> variant i.e. the one in 28-pin DIP package. The ATmega328p comes in a few different packages, and we need specifically the through-hole DIP 28 package, **not** a QFN or QFP package.

_To be continued._
