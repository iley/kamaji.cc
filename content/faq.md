---
title: "FAQ"
date: 2026-03-15T00:00:00Z
---

### Flashing firmware

#### How do I flash firmware to a new v1 chip?

New ATmega328p chips need their fuses programmed before the firmware can be flashed. Run the `set_fuses_v1` script from the repository using an ISP programmer (e.g. USBasp). After the fuses are set, flash the firmware with `pio run -e v1 -t upload`.

#### avrdude: verification error, first mismatch at byte ...

When flashing v1:

```
avrdude: verification error, first mismatch at byte ...
```

This typically happens with fresh chips. Use avrdude directly without the `-D` flag (which prevents chip erase):

```
avrdude -Pusb -v -p atmega328p -C <path>/avrdude.conf -c usbasp -U flash:w:.pio/build/v1/firmware.hex:i
```

Removing `-D` allows a full chip erase before writing, which resolves the verification mismatch.

#### avrdude: error: program enable: target doesn't answer

On v1:

```
avrdude: error: program enable: target doesn't answer
```

The fuses on the chip have not been set yet. Run the `set_fuses_v1` script from the repository. Also check that the ISP programmer is properly connected to the ICSP header on the board.

#### How do I flash firmware to v2 over USB?

The v2 uses an ATmega32U4 which supports USB natively. However, for the first flash, you need an ISP programmer to install the Caterina bootloader (found in `bootloader/caterina` in the repository). After the bootloader is installed, you can flash firmware over USB with `pio run -e v2 -t upload`.

#### v2 USB upload fails

```
avrdude: butterfly_recv(): programmer is not responding
```

During USB upload, you need to hold one of the player buttons (3rd or 4th) at the moment the chip resets at the start of the upload process. The button only needs to be held during the reset, not the entire time.

If USB upload remains unreliable, use an ISP programmer (USBasp) instead — it always works.

#### v2 is not recognized on Windows when connected via USB

Install the Arduino Leonardo USB driver. The v2 board (ATmega32U4) uses the same USB interface as Arduino Leonardo.

#### The firmware doesn't compile

```
Arduino.h:257:26: fatal error: pins_arduino.h: No such file or directory
```

This can happen after updating PlatformIO or Arduino framework libraries. Make sure you're using the library and framework versions specified in the repository's `platformio.ini`. Avoid updating libraries locally if the current versions work.

#### Firmware exceeds flash size on v2

```
Error: The program size (XXXXX bytes) is greater than maximum allowed (28672 bytes)
```

The ATmega32U4 on v2 only has 28KB available for firmware (32KB minus 4KB bootloader). If the firmware grows too large, you can save space by disabling unused features in the U8g2 graphics library via build flags. See the [u8g2 FAQ on flash optimization](https://github.com/olikraus/u8g2/wiki/faq#how-can-i-reduce-the-flash-memory-usage) for details.

### Hardware issues

#### Player buttons stop registering or LEDs don't light up

The most common hardware failure is a bad RJ10 cable crimp. Re-crimp the connectors using a crimping tool. It helps to keep spare pre-crimped cables on hand.

#### Where do I find RJ10 connectors? Are RJ11 connectors compatible?

RJ10 (4P4C) and RJ11 (6P4C) are different connectors and are not interchangeable. Use the specific RJ10 connectors linked in the project documentation.

#### The system behaves erratically / glitches out

Try cleaning the board with isopropyl alcohol to remove flux residue left over from soldering. Residual flux can cause unintended connections between traces, leading to unpredictable behavior.

If that doesn't help, try re-flashing the firmware via the ISP programmer.

#### The signal lamp doesn't work

Check the solder joints around the lamp connector. This has been a recurring issue across multiple units. Try a different lamp to rule out the lamp itself being faulty.

Note: USB-powered LED lamps with built-in batteries are not suitable as signal lamps, because they stay lit even after the system cuts power to the port.

#### Powerbank turns off while powering the system

Some powerbanks auto-shutoff when current draw is too low. The Kamaji system draws very little power in idle, which can trigger this. Use a wall outlet with an extension cord for reliable power, or look for a powerbank that doesn't have auto-shutoff.

#### LCD contrast keeps drifting (v1)

There is a potentiometer on the back of the LCD module that can be adjusted through a hole in the PCB. If the contrast keeps drifting persistently, the screen may need replacement.

#### USB-C to USB-C cable doesn't work with Arduino Pro Micro clones

(This is relevant for the Headless only).

Some cheap Arduino Pro Micro clones with USB-C ports are missing the CC pull-up resistors required by the USB-C specification. They will only work with USB-C to USB-A cables. As a workaround, use a USB-A adapter. When ordering new boards, look for models that correctly implement USB-C.

### What does the name Kamaji mean?

It's a reference to [Spirited Away](https://en.wikipedia.org/wiki/Spirited_Away).
