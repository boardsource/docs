---
title: Arachnophobe Solderable Kit Build Guide
description: How to put together your new Arachnophobe solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: false
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/8zi3Gt9.jpg
thumbnail: https://i.imgur.com/c7dVmmF.png
---
### This guide is for *arachno* PCBs.
https://i.imgur.com/8zi3Gt9.jpg
# Parts
### Required 
| Item | Count |
|------|-------|
| SMD Diodes | 30 |
| PCB | 1 |
| Seeed Style or similar microcontroller | 1 |
| Reset Switch | 0 |
| Choc Hotswap Sockets | 30 |
| Choc Switches | 30 |
| *Choc* Keycaps | 30 |


# Soldering
## Diodes
**Orientation**: Place the diode with the black bar facing the white closed end
of the square.
1. Solder one pad. ![one pad - diode](https://i.imgur.com/B0tFJq5.jpg)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](https://i.imgur.com/nebKz9q.jpg)
3. Solder other pad. ![diode complete](https://i.imgur.com/MYz765l.jpg)
- Note, when working with
[MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package
diodes, you may need to reflow and add more solder a couple times before an
adequate connection is made.


## Hotswap sockets
1. Solder one pad. ![Hot swap socket foot print
soldered](https://i.imgur.com/xBaLlFa.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place
socket down on pad. ![Hot swap socket one pin
soldered](https://i.imgur.com/ZYlgY65.jpg)
3. Solder other pad. ![Hot swap socket
finished](https://i.imgur.com/YLqHcUj.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure
  the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Place controller with compontants facing up.
- Note, it is recommended to flash each microcontroller prior to soldering. See
  [firmware](#firmware) section for more.
1. Solder one pad ![headers inserted](https://i.imgur.com/6DlAxNB.jpg)
2. Place microcontroller with componants facing up and reflow the soldered pad
to secure the controller. ![microcontroller
placed](https://i.imgur.com/1tLroev.jpg)
3. Apply solder to all pins. ![microcontroller
finished](https://i.imgur.com/IsLYdjX.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under arachnophobe. This will require a fork
of QMK found
[here](https://github.com/sadekbaroudi/qmk_firmware/tree/master/keyboards/fingerpunch/arachnophobe).
To begin, follow the [QMK setup
guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an
existing installation, an
[update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch)
may be needed.) \ For flashing instructions, see
[doc](https://docs.qmk.fm/#/newbs_flashing) or
[video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under arachnophobe. #TODO

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
