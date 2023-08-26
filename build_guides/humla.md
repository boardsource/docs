---
title: Humla Build Guide
description: How to put together your new Humla solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/MISSING
subcategory: medium
draft: true
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/iFoeTYd.jpg
thumbnail: https://i.imgur.com/Gsbvhhi.png
---

### This guide is for *Humla* PCBs.
# Parts
### Required 
| Item | Count |
|------|-------|
| Smd Diodes | 36 |
| PCB | 1 |
| Pro-Micro or similar microcontroller | 1 |
| Reset Switch | 1 |
| Choc Hotswap Sockets | 36 |
| Choc Switches | 36 |
| Choc Keycaps | 36 |



![components](https://imgur.com/jT8HUQ3.jpg)

# Soldering
## Diodes
**Orientation**: place the diode with the black bar towrds the white bar
indicator on the pcb.
1. Solder one pad. ![one pad - diode](https://imgur.com/4xkhNLN.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://imgur.com/ebNhsk3.jpg)
3. Solder other pad. ![diode complete](https://imgur.com/xgMnV9D.jpg)
- Note, when working with
[MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package
diodes, you may need to reflow and add more solder a couple times before an
adequate connection is made.



## Hotswap sockets
1. Solder one pad. ![Hot swap socket foot print
soldered](https://imgur.com/Vzn1JnV.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place
socket down on pad. ![Hot swap socket one pin
soldered](https://imgur.com/NWXUwe0.jpg)
3. Solder other pad. ![Hot swap socket finished](https://imgur.com/4jkgbsp.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure
  the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: microcontroller face down.
- Note, it is recommended to flash each microcontroller prior to soldering. See
  [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back. ![headers
inserted](https://imgur.com/RvOAjJe.jpg)
2. Place microcontroller face down. ![microcontroller
placed](https://imgur.com/0NZEMJe.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://imgur.com/Nuecurb.jpg)



## Misc.

### Reset switches
1. Solder one pad. ![reset switch placed](https://imgur.com/HfQZimm.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on
   pad.
3. Solder remaining pads. ![reset switch placed](https://imgur.com/CUYsUdS.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under QMKKEYBOARDNAME. #TODO To begin, follow
the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working
from an existing installation, an
[update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch)
may be needed.) \ For flashing instructions, see
[doc](https://docs.qmk.fm/#/newbs_flashing) or
[video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under KMKKEYBOARDNAME #TODO

Peg can be downloaded [here](https://peg.software/), and the quick start can be
seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the
quick start can be seen
[here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)

Here are some links to other articles that may help you get the most out of your
new keyboard:
* Get the most out of your PCB [Unleashing the High-Tech Power of Custom
  Keyboards](https://new.boardsource.xyz/docs/articles-features)
* [Keyboard
  Programing](https://new.boardsource.xyz/docs/guides-keyboard_programing)

## Extra
For questions, ask in [Boardsource Discord
server](https://discord.gg/5qpqbgaTYz)
