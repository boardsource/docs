---
title: ETERNAL Keypad Build Guide
description: How to put together your new ETERNAL Keypad solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ecc2008eee64242946c98c1
subcategory: easy
draft: false
tags: 
- macro
- kit
- gaming
banner: https://i.imgur.com/u7KRFV9.jpg
thumbnail: https://i.imgur.com/u7KRFV9.jpg
---
# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 36 |
| PCB | PCBCOUNT |
| CONTROLLERSTYLE or similar microcontroller | CONTROLLERCOUNT |
| TRRS Jack | 0 | 
| TRRS Cable | 0 | 
| Reset Switch | 1 | 
| MX Hotswap Sockets | 36 | 
| MX Switches | 36 | 
| *MX* Keycaps | 36 |

### Optional 
| Item | Count | 
|------|-------| 
| SK6812 Mini-E LED | *36* |
| WS2812B LED | 8 |

![components](https://i.imgur.com/fo77y4X.jpg)

# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/zsCmpM5.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/tXpqRro.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/zic55Px.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & WS2812B LEDs.
![ws2812b orientation](https://i.imgur.com/guu0UiP_d.jpg?maxwidth=520&shape=thumb&fidelity=high)
- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider [soldering your controllers beforehand](#microcontrollers). \
\- The LED order is somewhat outlined ![LED order](LEDORDERIMG) and should be followed in order when building.
1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing WS2812B LEDs)
![sk6812 mini e one pad](LEDCLOSEUPIMG1)
![ws2812b 4 pads](https://i.imgur.com/StfQVUN.jpg)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](LEDCLOSEUPIMG3)
![ws2812b placed](https://i.imgur.com/bLVeVvu.jpg)
3. Solder remaining pads.
![sk6812 mini e complete](https://i.imgur.com/A5ppUFI.jpg)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/Jh7tqQQ.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/RrK1IFS.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/6msPm1l.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/uLeKpKX.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/kHDmH1w.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/ehYRVqj.jpg)

## Misc.
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/sTuoxPH.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/BxkbzxR.jpg)



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