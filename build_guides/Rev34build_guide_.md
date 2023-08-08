---
title: Reviung34 Build Guide
description: How to put together your new Reviung34 solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5f2ef1b52bf5e8714a60f613
subcategory: medium
draft: false
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/cXcIuV6.jpg
thumbnail: https://i.imgur.com/cXcIuV6.jpg
---
### This guide is for *KEYBOARDNAME* PCBs.
https://i.imgur.com/GFpmPNH.jpg
# Parts
### Required 
| Item | Count |
|------|-------|
| SMT Diodes | 33-34 |
| PCB | PCBCOUNT |
| Pro micro stlye or similar microcontroller | Blok |
| Reset Switch | 1 | 
| SOCKETSTYLE Hotswap Sockets | 33-34 | 
| SWITCHSTYLE Switches | 33-34 | 
| *KEYCAPSTYLE* Keycaps | 33-34 |

### Optional 
| Item | Count | 
|------|-------|
| WS2812B LED | 8 |

![components](https://i.imgur.com/CGflXKX.jpg)

# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/l75iEcb.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/qWvV8EY.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/kE9cqeO.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & WS2812B LEDs.
![sk6812 mini e orientation](LEDORIENTATIONIMG1)
![ws2812b orientation](LEDORIENTATIONIMG2)
- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider [soldering your controllers beforehand](#microcontrollers). \
\- The LED order is somewhat outlined ![LED order](LEDORDERIMG) and should be followed in order when building.
1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing WS2812B LEDs)
![sk6812 mini e one pad](LEDCLOSEUPIMG1)
![ws2812b 4 pads](https://i.imgur.com/VdBHZeh.jpg)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](LEDCLOSEUPIMG3)
![ws2812b placed](https://i.imgur.com/7nsE6Ud.jpg)
3. Solder remaining pads.
![sk6812 mini e complete](LEDCLOSEUPIMG5)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/Q4Jvemy.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/p6SgExz.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/bFMwdHh.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/LQE4ido.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/7jRClJk.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/k9s3qkn.jpg)

### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/Qm0ER53.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/fWRp5LL.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under reviung/reviung34.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under reviung/reviung34

Peg can be downloaded [here](https://peg.software/), and the quick start can be seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the quick start can be seen [here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)