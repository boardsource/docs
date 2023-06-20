---
title: Sweep Build Guide
description: How to put together your new Sweep keyboard kit.
author: Boardsource
product_link: https://boardsource.xyz/store/61d0b772319a1f3cc53ba2fb
subcategory: easy
draft: false
tags: 
- Sweep
- split
banner: https://boardsource.imgix.net/a49277b0-28d9-11ed-8771-8b53559ba1bf.jpg
thumbnail: https://boardsource.imgix.net/a8107ae0-28d9-11ed-bdbc-ab99b282b508.jpg?auto=format&ixlib=react-9.2.0&q=80&w=200&dpr=1
---
### This guide is for *Sweep* PCBs.
https://i.imgur.com/xCyMaet.jpg
https://i.imgur.com/abjDor6.jpg
https://i.imgur.com/0yCdYyN.jpg
# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 34 |
| PCB | 2 |
| Blok or similar microcontroller | 2 |
| TRRS Jack | 2 | 
| TRRS Cable | 1 | 
| Reset Switch | 2 | 
| MX Hotswap Sockets | 34 | 
| MX Switches | 34 | 
| *MX* Keycaps | 34 |

![components](https://i.imgur.com/TOSEbBB.jpg)

# Soldering

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/0NiHxI1.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](SOCKETCLhttps://i.imgur.com/eueMfUN.jpgOSEUPIMG2)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/3T4OOt8.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/j0L0UKX.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/WXPr74c.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/NEkz8Hb.jpg)


## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape.
![trrs jack placed](https://i.imgur.com/RGORZIJ.jpg)
2. Apply solder to all four pins.
![trrs jack finished](https://i.imgur.com/V29nVRL.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/XgvlIBi.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/6TieoFz.jpg)



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