---
title: Equals kit Build Guide
description: How to put together your new Equals solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5f2ef1b52bf5e8714a60f613
subcategory: medium
draft: false
tags: 
- 40%
- ergo
- kit
banner: https://i.imgur.com/OOQouF0.jpg
thumbnail: https://i.imgur.com/NjN2XvX.png
---
### This guide is for *EQUALS* PCBs
# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | 60 |
| PCB | 1 |
| Promicro style or similar microcontroller | 1 |
| Reset Switch | 1 | 
| SOCKETSTYLE Hotswap Sockets | 60 | 
| SWITCHSTYLE Switches | 60 | 
| *KEYCAPSTYLE* Keycaps | 60 |

### Optional 
| Item | Count | 
|------|-------|
| SK6812 Mini-E LED | *60* |
| WS2812B LED | 10 |
![components](https://i.imgur.com/8h2rClk.jpg)

# Soldering
## Diodes
**Orientation**: Place the diode on the pcb with the black bar facing the thick white line on the pcb.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/ARJgn51.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/ycIxaYC.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/L9Bw86b.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & WS2812B LEDs.
![sk6812 mini e orientation](https://i.imgur.com/hcw94Po_d.jpg?maxwidth=520&shape=thumb&fidelity=high)
![ws2812b orientation](LEDORIENTATIONIMG2)
- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider [soldering your controllers beforehand](#microcontrollers). \
\- The LED order is somewhat outlined ![LED order](LEDORDERIMG) and should be followed in order when building.
1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing WS2812B LEDs)
![sk6812 mini e one pad](https://i.imgur.com/CzNgJjl.jpg)
![ws2812b 4 pads](https://i.imgur.com/HNruR0N.jpg)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](https://i.imgur.com/10rMG0j.jpg)
![ws2812b placed](https://i.imgur.com/v1z97ud.jpg)
3. Solder remaining pads.
![sk6812 mini e complete](https://i.imgur.com/cfytqak.jpg,https://i.imgur.com/SGx5Rxe.jpg)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/TvVu7mr.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/kVzCyZM.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/NIIgjbi.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.
- Oreantation of middle cluster of hot swaps 
![hot swap oreantation](https://i.imgur.com/zOeROG9.jpg)

## Microcontrollers
**Orientation**: Place controller with the companants faceing down.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/0LIcQwb.jpg)
2. Place microcontroller face down. 
![microcontroller placed](https://i.imgur.com/Z80g7oY.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](CONTROLLERCLOSEUPIMG3)


## Misc
### Reset switches
1. Solder one pad.
![reset switch placed](https://i.imgur.com/wI6NdQN.jpg)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](https://i.imgur.com/pBkpjSF.jpg)



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