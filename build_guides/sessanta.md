---
title: Sessanta Build Guide
description: How to put together your new Sessanta solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ecc2008eee64242946c98c1
subcategory: easy
draft: false
tags: 
- kit
banner: https://i.imgur.com/n2h1uYU.jpeg
thumbnail: https://i.imgur.com/n2h1uYU.jpeg
---

### This guide is for Sessanta PCBs.

# Parts
### Required 
| Item | Count |
|------|-------|
| SMD Diodes | 68 |
| PCB | 1 |
| Pro-micro or similar microcontroller | 1 |

| Reset Switch | 1 | 
| MX / Choc Hotswap Sockets | 68 | 
| MX / Choc Switches | 68 | 
| MX / Choc Keycaps | 68 |

### Optional 
| Item | Count | 
|------|-------|
| SK6812 Mini-E LED | 68 |
| WS2812B LED | 8 |


# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](https://i.imgur.com/vlHoyMu.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/TKuBsxg.jpg)
3. Solder other pad.
![diode complete](https://i.imgur.com/YQwuBor.jpg)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & WS2812B LEDs.

- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider soldering your controllers beforehand\

1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing WS2812B LEDs)
![sk6812 mini e one pad](https://i.imgur.com/PaizkC8.jpg)
![ws2812b 4 pads](https://i.imgur.com/wfUZmew.jpg)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](https://i.imgur.com/oyW5QVw.jpg)
![ws2812b placed](https://i.imgur.com/rZ9MIKe.jpg)
3. Solder remaining pads.
![sk6812 mini e complete](https://i.imgur.com/a1jlmZH.jpg)
![ws2812b complete](https://i.imgur.com/6dg4w51.jpg)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/RMN1eoF.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/CmW4ott.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/BZmCPs0.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/9Slvcpv.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/VEGqRNM.jpg)
![top pins tack soldered](https://i.imgur.com/4zvrYZj.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/b1YbpNk.jpg)


# All Done!

Enjoy

![finished](https://i.imgur.com/n2h1uYU.jpeg)


## Firmware

### QMK
In qmk this keyboard can be found under boardsource/Sessanta.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)