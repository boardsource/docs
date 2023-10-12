---
title: Flashing keyboards and you
description: Everything you could want to know about flashing terms.
author: Boardsource
subcategory: easy
draft: true
tags: 
- learning
---

 # Welcome to the ultimate flashing terms guide

 By the end of this you should know everything you could ever want to know about
 the basics of flashing keyboards.

 Table of contents:
 * [What is flashing](#what-is-flashing)
 * [What is a microcontroller](#what-is-a-microcontroller)
 * [What is a firmware](#what-is-a-firmware)
 * [What is a bootloader](#what-is-a-bootloader)

## What is flashing

"Flashing" is a term that is used to refer to putting code onto a
microcontroller (read what this is below). Because these are fully programmable,
it's up to us to choose what we want them to do! Depending on your firmware
(also defined below), there will be a few different steps on how to get this
code, but over all, the process of flashing is just to let the keyboard know
it's actually a keyboard, and that's how you want it to act.

## What is a microcontroller

A microcontroller is basically "the brains" of the operation. There are many out
there, but they all serve the same purpose in the end. To turn our thing that
looks like a keyboard, into something that knows it's a keyboard! Sometimes the
microcontroller is built into the keyboard itself, and sometimes you have to
solder a "generic" microcontroller onto the keyboard itself. The microcontroller
choice is important to you as it is what decides what all features the keyboard
could have in terms of being bluetooth, or how much storage you have for things
like screen images. It can also change what kind of firmware is supported if you
have a preference between them. We'll cover that in a bit.

### Common generic microcontrollers

Most commom microcontrollers for keyboards are based on the Pro Micro pinout.
That means that any keyboard that can take a Pro Micro controller can also have
these installed instead. While the pro micro is the historical choice for
keyboards, it's quite limited these days, so we have many more options. 

| Features    | Boardsource Blok | Other RP2040 Controllers | Pro Micro/ Elite-c | Nice!Nano |
|-------------|------------------|--------------------------|--------------------|-----------|
| CPU Cores   | 2                | 2                        | 1                  | 2         |
| CPU Speed   | 133MHz           | 133MHz                   | 16MHz              | 64MHz     |
| RAM         | 264KB            | 264KB                    | 32kb               | 265Kb     |
| ROM         | 16MB             | 8MB                      | 1KB                | 1MB       |
| KMK Support | Yes              | Yes                      | No                 | No        |
| QMK Support | Yes              | Yes                      | Yes                | No        |
| ZMK Support | Yes*             | Yes*                     | No                 | Yes       |

* ZMK does not at the moment support split keyboards with a wire. You must use
  bluetooth for split keyboards, and anything with Yes* marked, will not work
  for split keyboards on ZMK specifically. This may change at a later date.

### Firmware overviews

You can read a bit more about firmwares at these links. Hopefully they can
provide some information to you on which firmware you should choose, or which
controller may be suited if you have a choice on controllers. Integrated boards
will tell you which they have on the sales page usually. Anything sold at
Boardsource integrates a Blok for keyboards with a wire, or a Nice!Nano for
anything sold as wireless.

- [QMK firmware](https://www.boardsource.xyz/docs/guides-what_is_qmk) 
- [KMK firmware](https://www.boardsource.xyz/docs/guides-what_is_kmk) 
- [ZMK Firmware](https://www.boardsource.xyz/docs/guides-what_is_zmk) 

There are graphical front ends to make it easier to configure keyboards as well.
These are built on top of the firmware's listed above, so compatibility should be
checked for those, but just to be sure to include them, I'll list them below.

- [Peg](https://getpeg.xyz/) Built on top of KMK firmware
- [VIA](https://www.caniusevia.com/) Built on top of QMK
- [Vial](https://get.vial.today/) Built on top of QMK

## What is a bootloader

Now that we know what firmware there is, and we have the file we want, we need
to actually flash the keyboard! This is where bootloader comes in. There's 2
real modes for a your keyboard to be in. Acting like a keyboard, and waiting for
the new code to run your keyboard on. It can't do both at the same time
(usually, expections are listed later). In order to get your keyboard ready to
get into bootloader, there's a few ways depending on your controller. Most
keyboards you can quickly double tap the reset button on the keyboard's PCB.
This will take you into the bootloader. If you have a blok, integrated
controller keyboard, or nice!nano, you will probably see a new "flash drive"
appear on your system. It's usually called RPI-RP2, or NiceNano or something
similar. If you have an older board, or Pro Micro or Elite C, you will not see
this drive, and a new serial device will appear. If you have a serial device,
you are using QMK and the tools should find it automatically. Blok can also boot
into bootloader by holding the BOOT button on the edge of the board. Don't get
it mixed up with the other reset button back there or it won't work.

### KMK and bootloader

KMK/Peg break the rule of needing to be in bootloader to flash, most of the
time. If you want to switch from another firmware to KMK/Peg, you'll need to
flash it's "hypervisor" in the bootloader, but it's no more difficult than
dropping a file on just like any other firmware. You also may want to get
updates for it every once in a while. Further instructions for that process can
be found [here](https://getpeg.xyz/docs/board-update) and are only needed for KMK/Peg.


## Wrap up

That should be almost everything you need to know about the basics of flashing
basically any controller, and how to get into the bootloader. Feel free to reach
out on our discord if you have any further questions or issues! We'll be glad to
help you out.
