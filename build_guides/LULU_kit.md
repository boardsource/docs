---
title: LULU Solderable Kit Build Guide
description: How to put together your new LULU solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: false
tags: 
- 60%
- ergo
- kit
banner: https://images.boardsource.xyz/v1_images/16a75fce-87f1-4879-82ad-c8e72a3140ce.jpg
thumbnail: https://images.boardsource.xyz/v1_images/02e4fba4-907c-49c9-a258-5836d44fd519.jpg
---
### This guide is for *LuLusolderable* PCBs.
https://i.imgur.com/FOESANU_d.jpg?maxwidth=520&shape=thumb&fidelity=high
https://i.imgur.com/k9hUQhm_d.jpg?maxwidth=520&shape=thumb&fidelity=high
# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 58 |
| PCB | PCBCOUNT |
| CONTROLLERSTYLE or similar microcontroller | CONTROLLERCOUNT |
| TRRS Jack | 2 | 
| TRRS Cable | 1 | 
| Reset Switch | 2 | 
| SOCKETSTYLE Hotswap Sockets | 58 | 
| SWITCHSTYLE Switches | 58 | 
| *KEYCAPSTYLE* Keycaps | 58 |

### Optional 
| Item | Count | 
|------|-------|
| 128x32 OLED Display | 2 | 
| SK6812 Mini-E LED | *58* |
| SK6821-MINI LED | 8 |
| EC11 Encoder + Knob | 2 |
![components](NULLEDCOMPONETSIMAGE)

# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/wy7QK95.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/9wjvMkg.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/VQrsV67.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & SK6821-MINI LEDs.
![sk6812 mini e orientation](https://i.imgur.com/hcw94Po.jpg)
![SK6821-MINI orientation](https://i.imgur.com/DvV3Rbk.jpg)
- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider [soldering your controllers beforehand](#microcontrollers). \
1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing SK6821-MINI LEDs)
![sk6812 mini e one pad](https://i.imgur.com/Wyp0Hsz.jpg)
![SK6821-MINI 4 pads](https://i.imgur.com/3GLu3nV.jpg)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](https://i.imgur.com/fhRqqxF.jpg)
![SK6821-MINI placed](https://i.imgur.com/rnhh1xS.jpg)
3. Solder remaining pads.
![sk6812 mini e complete](https://i.imgur.com/MQWEMSW.jpg)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/2UX7iw9.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/x7VFVli.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/YgssoVO.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/OSXY7sq.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/OSXY7sq.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/TuWKLe0.jpg)

## OLEDs
1. Insert headers from front, solder in from the back.
![Oled placed](https://i.imgur.com/3GM4vPm.jpg)
2. Solder only one of pins to begin with.
![oled back one pin soldered](OLEDCLOSEUPIMG2)
3. While reflowing solder joint, position OLED so that it is level & straight.
4. Solder remaining pins and clip extra length of pins.
![oled finished](https://i.imgur.com/cmdR9DU.jpg)

## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape.
![trrs jack placed](https://i.imgur.com/F2P9kx7.jpg)
2. Apply solder to all four pins.
![trrs jack finished](https://i.imgur.com/qJuzYNS.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/h3Lfg1h.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/POeAytM.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under QMKKEYBOARDNAME.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under KMKKEYBOARDNAME

Peg can be downloaded [here](https://peg.software/), and the quick start can be seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the quick start can be seen [here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)