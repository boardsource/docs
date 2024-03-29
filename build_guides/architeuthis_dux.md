---
title: Architeuthis dux Solderable Kit Build Guide
description: How to put together your new Architeuthis dux solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9df84c6b834480de6c3d0
subcategory: medium
draft: false
tags: 
- 30%
- ergo
- kit
banner: https://i.imgur.com/OBw7vIf.jpg
thumbnail: https://i.imgur.com/VhvY3Do.png
---
### This guide is for *architeuthis* PCBs.
# Parts
### Required 
| Item | Count |
|------|-------|
| PCB | 2 |
| Promicro-style or similar microcontroller | 2 |
| TRRS Jack | 2 |
| TRRS Cable | 1 |  
| Choc Hotswap Sockets | 30 |
| Choc Switches | 30 |
| *Choc* Keycaps | 30 |


![components](https://i.imgur.com/ZQ76UcC.jpg)

# Soldering

## Hotswap sockets
1. Solder one pad. ![Hot swap socket foot print
soldered](https://i.imgur.com/K9iFUF1.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place
socket down on pad. ![Hot swap socket one pin
soldered](https://i.imgur.com/6mw1P1j.jpg)
3. Solder other pad. ![Hot swap socket
finished](https://i.imgur.com/Gu1ZaG4.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure
  the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers one component face up and one component
face down.
- Note, it is recommended to flash each microcontroller prior to soldering. See
  firmware section for more.
1. Insert headers from front, solder in from the back. ![headers
inserted](https://i.imgur.com/qiEeM6d.jpg)
2. Place microcontroller one component face down and one componant face up.
![microcontroller placed](https://i.imgur.com/5ApcPZW.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/fNjfIpO.jpg)

## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape. ![trrs jack
placed](https://i.imgur.com/hPTzQyx.jpg)
2. Apply solder to all four pins. ![trrs jack
finished](https://i.imgur.com/hKw5Hjw.jpg)



## Firmware

### QMK
In qmk this keyboard can be found under a_dux. To begin, follow the [QMK setup
guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an
existing installation, an
[update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch)
may be needed.) \ For flashing instructions, see
[doc](https://docs.qmk.fm/#/newbs_flashing) or
[video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under a_dux

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
