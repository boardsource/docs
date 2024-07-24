---
title: 📱+ 🎮 Gamepad Build Guide
description: How to put together your new 📱+ 🎮 solderable kit.
author: Boardsource
product_link: https://boardsource.xyz/store/5ecc2008eee64242946c98c1
subcategory: easy
draft: false
tags: 
- kit
banner: https://i.imgur.com/dNG37ef.jpeg
thumbnail: https://i.imgur.com/dNG37ef.jpeg
---
# Overview
#### This build guide walks you through how to build the 📱+ 🎮.

![all the parts](https://i.imgur.com/04DtAWG.jpg)


## Kit Contents
* PCB
* FR4 Backplate
* FR4 Plate
* rp2040 zero controller
* start select switches
* Hotswap Sockets (optional)
* choc switches & keycaps
* Standoffs
* M2 Screws
* Rubber Feet


# Prep
![parts broken apart](https://i.imgur.com/JtGC1qK.jpg)

Break apart the PCB to do so use some clippers to clip the mouse bites.

# Soldering

## Controller 

Place your controller on the top side of the pcb (opposite of the hotswaps) and line up the holes in the pcb. 
> **tip:** it can be helpful to use some of the pins included with the controller to line up the contrler but we **DO NOT** solder the pins into the pcb.

![placing the controller](https://i.imgur.com/GFYKI9b.jpg)

once you have lined up the controller solder in one conner to lock it in place 

![soldering one pin on controller](https://i.imgur.com/UlGWFDL.jpg)

![soldering second pin on controller](https://i.imgur.com/35kZK2f.jpg)

After that you can continue around the controller and solder the rest of the pins.

![contoller finished](https://i.imgur.com/nyWRj08.jpg)

## Buttons

Solder one pad.

![installing puttons pt1](https://i.imgur.com/ppEJNCD.jpg)

Reflow that ond pad and Push one of the switches into the liquid solder.

![installing puttons pt2](https://i.imgur.com/Lz2BGZz.jpg)

After one side is done solder the other side of the switch

![installing puttons pt3](https://i.imgur.com/iGbdQBr.jpg)

Done 

![soldering the case together pt2](https://i.imgur.com/rdBeVqv.jpg)


## Finish the build

Place the PCB labeled as `level 0` onto the back of your PCB

![soldering the case together pt1](https://i.imgur.com/2SxWWA9.jpg)

And solder through one of the holes on the `level 0` plate.
Once you are happy with the alignment, do the other 2 holes. 

![soldering the case together pt6](https://i.imgur.com/XnTv3XA.jpg)

Next lay `level 2` onto the PCB over the installed switches and controller, and solder the holes together again.


Follow the same for `Level 3`

![soldering the case together pt3](https://i.imgur.com/PZ0YJxf.jpg)
![soldering the case together pt4](https://i.imgur.com/DOeSVt6.jpg)
![soldering the case together pt5](https://i.imgur.com/WtQTW4l.jpg)
# Build Done
![controller finished](https://i.imgur.com/rQfJPCx.jpg)
# Flashing.

## Downloads
This kit uses the awesome [gp2040-ce](https://gp2040-ce.info/) gamepad firmware 

Download the file below.
* [firmware](https://github.com/OpenStickCommunity/GP2040-CE/releases/download/v0.7.9/GP2040-CE_0.7.9_WaveshareZero.uf2)


Once you have the file downloaded we need to flash the firmware. 
To do so you need to hold down the boot button on the blue controller in the center, while you plug in the controller to your computer.

After you do that it will show up as a drive and you can transfer the .uf2 file you downloaded from the first link.

![how to flash uf2](https://images.boardsource.xyz/how_to_uf2_flash.gif)

# Really done this time go play some games.