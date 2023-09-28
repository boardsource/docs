---
title: Horizon Solderable Kit Build Guide
description: How to put together your new Horizon solderable kit.
author: skarrmann
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: true
tags: 
- 60%
- ergo
- kit
banner: https://i.imgur.com/3PRrVSy.jpga
thumbnail: https://i.imgur.com/3PRrVSy.jpg
source: https://github.com/skarrmann/horizon/blob/main/README.md
---

### This guide is for *Horizon* PCBs.

# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 52 |
| PCB | PCBCOUNT |
| CONTROLLERSTYLE or similar microcontroller | 1 |
| Reset Switch | 1 | 
| MX Hotswap Sockets | 52 | 
| MX Switches | 52 | 
| *MX* Keycaps | 52 |

![components](https://i.imgur.com/SNZ79Y0.jpg)

# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/KntosS2.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/5h5tL9z.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/eiSoYuR.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/RJZayFD.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/ulCIb8k.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/unhaijT.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/WV2uoNg.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/2YeofvD.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/SZAt4eX.jpg)


## Misc.
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/yK8lNWI.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/JlLXcWx.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under QMKHorizon.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under KMKHorizon

Peg can be downloaded [here](https://peg.software/), and the quick start can be seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the quick start can be seen [here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)