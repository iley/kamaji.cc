---
title: "Bill of materials"
date: 2023-01-14T14:19:25Z
weight: 1
---

Here's what you'll need to assemble your own Kamaji buttons. The quantites shown are per single button. Multiply that by the number you need and consder ordering some spares.

Everything (except the custom PCB) can be found on Aliexpress or other marketplaces for cheap.

| Item                                       | How many | Search query              |
|--------------------------------------------|----------|---------------------------|
| [Custom PCB](#pcb)                         | 1        | N/A                       |
| [Cherry MX switch](#switch)                | 1        | cherry mx keyboard switch |
| [2×3×4 square LED](#led)                   | 1        | 2x3x4 square LED          |
| [M2.5 6mm bolt](#bolts-and-inserts)        | 1        | M2.5 bolt 6mm             |
| [M2.5 threaded insert](#bolts-and-inserts) | 1        | M2.5 threaded insert      |
| [RJ10 (4P4C) socket](#rj10-socket)         | 1        | RJ10 socket               |
| [Translucent keycap](#keycap)              | 1        | cherry mx keycap clear    |
| [Telephone cable](#cable)                  | 1        | telephone cable 4p4c      |

## PCB

<img src="/images/button-pcb.jpg">

For information on how to get the printed circuitboards manufactured, see [next step](/hardware/buttons/pcb).

## Switch

<img src="/images/switch.jpg">

The Kamaji button uses standard mechanical keyboard switches compatible with Cherry MX. You can buy original Cherry switches of your choice (e.g. blue, brown, black, red), or go for a compatible alternative from Kailh or Gateron.

One thing to check when ordering switches is __whether they have a slot for an LED__. The original Cherry switches do, but some clones might not have them.

We would not recommend saving pennies by going with no-name clone switches. The ones from respectable brands are cheap enough, and you only need one per player button.

## LED

<img src="/images/button-parts-led.jpg">

The LEDs in the buttons are mounted into the slot of the keyboard switch. We recommend using 2×3×4 square LEDs, as they fit well. Other LEDs with the same lead spacing might work too. For more information see [this thread on Geekhack](https://geekhack.org/index.php?topic=62943.0).

## Bolts and inserts

<img src="/images/bolt-and-insert.jpg">

The enclosure parts and the PCB are held together with an M2.5 bolt and a threaded insert.

The bolt is a standard 6mm M2.5 bolt with a round head.

We used [brass threaded inserts from CNC Kitchen](https://cnckitchen.store/products/gewindeeinsatz-threaded-insert-m2-5-standard-100-stk-pcs). Other brands should work fine too, as long as they have similar dimensions (outer diameter 4.6mm, length 4mm). When ordering make sure to __check the outer diameter__ of the inserts as it may vary significantly.

## RJ10 Socket

<img src="/images/rj10-sockets.jpg">

Kamaji uses RJ-10 (4P4C) sockets that are commonly used for landline phones.

There are two things to look up for when ordering sockets:
 * Make sure you're ordering 4-pin sockets, not 6-pin.
 * On Aliexpress and similar marketplaces there are two common types of sockets, one is narrower and the other is wider. Look for the __narrow__ ones (~12mm wide).

## Keycap

<img src="/images/clear-keycap.jpg">

You'll need Cherry MX compatible keycaps. The keycaps should be translucent/clear so that it's easier to see when the LED below is lit.

## Cable

<img src="/images/rj10-cable.jpg">

Now, with cables you have two options:

1. Buy pre-made.
2. Make your own.

The former is simpler, the latter is cheaper and more flexible.

If you'd like to buy pre-made cables, search for 4P4C telephone cables on Aliexpress or in local hardware stores.

For making your own cables you'll need a crimping tool. Make sure it supports 4P4C plugs, not all tools do. Buy flat 4-wire telephone cable and 4P4C plugs and crimp cables of the desired length.

<img src="/images/crimper.jpg">

An added benefit of having a crimping tool and plugs is that you can repair broken cables by trimming and re-crimping them.

## Next

While you're waiting for all parts to arrive, go ahead and [order the PCBs](/hardware/buttons/pcb).
