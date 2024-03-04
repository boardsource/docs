---
title: lulu Flashing Guide
description: How To Flash your lulu.
author: Boardsource
product_link: https://boardsource.xyz/store/61d0b772319a1f3cc53ba2fb
subcategory: easy
draft: false
tags: 
- qmk
- kmk
- flashing
banner: https://boardsource.imgix.net/582cb260-2419-11ed-b578-8b4b9b5190c0.jpg?auto=format&ixlib=react-9.2.0&q=80&w=500&dpr=1
thumbnail: https://boardsource.imgix.net/2c78ccd0-2419-11ed-821e-f55d25e8770a.jpg?auto=format&ixlib=react-9.2.0&q=80&w=500&dpr=1
---
# Flashing Your lulu PCB

## Quick Links
* [Build Guide](https://boardsource.xyz/help/612317c39c85c6050be18f95)
* [lulu FAQ](https://boardsource.xyz/help/630a9da38c8d9776570a5f14)

This page is meant to be a reference to flashing your lulu SMT PCB.

Please note that updating and making edits to your keymap is not covered here, but the lulu is designed to work out of the box with Peg. [Click here to learn more about Peg and download](peg.software). 

Please follow this guide in it's entirety, but if you feel you need additional help, feel free to [enter our Discord server](https://discord.gg/b4R25WSZvH) and ask for help under in the #hardware-help channel. 

## Flashing With Defaults

While using Peg, you do not need to use the Boot switch or Reset switch. If for some reason you need to get your PCB back to a known working state or ‘Factory Reset’ it, you can flash the PCB with the default Peg map.

The files below come with everything you need, BS-Python (CircuitPython Fork), KMK, all required libs, and the default lulu keymap.

* [Recent](https://github.com/boardsource/bs-python/releases/download/v1.9.2/boardsouce_lulu_full.uf2)
* [Latest](https://github.com/boardsource/bs-python/releases)

## Flashing With VIA

Below you will find the VIA Map available for download. Download the VIA Map and continue with the guide as normal.

* Coming Soon

##  Flashing Process

First, unplug your lulu PCB from the computer.

On the back of your PCB you will notice a sliding switch around where the controller would sit on the other side. This switch has two states, Default and Boot. When you open your PCB, the switch should be in the default position. The switch’s default position is outlined with silkscreen. 

In order to put the PCB into boot mode, you must (while the PCB is unplugged) put the switch into Boot mode. When the switch is in Boot mode you will notice the silkscreen outline indicating it’s Default position. 

Check the diagrams below to see these two states, Default and Boot.

## Default Boot Switch State
![boot switch](https://boardsource.imgix.net/a5660340-2416-11ed-bb98-d52a22ef97df.jpg)

## Boot Mode Switch State
![boot switch](https://boardsource.imgix.net/dfd19c10-2416-11ed-af40-7d5df7221082.jpg)

With the PCB in Boot mode, you can plug it back into your computer. 

After a few moments, your PCB should appear as a Drive on your computer named  "RPI-RP2.” After you locate this drive, before doing anything else, put your PCB back into Default mode. The drive will NOT disappear. 

With the Drive "RPI-RP2" located on your computer AND the Switch reset to it’s Default position you can drag and drop the Uf2 files onto the drive (onto the PCB). When it is done transferring the file, your PCB will reboot. Because you put the switch back to it’s Default position, when the board restarts it will no longer be in Boot mode and will be good to go. 

If you’ve successfully transferred the Uf2 file, you should see the LEDs turn back on, and a new ‘BSPYTHON’ drive mount to your computer. If the transfer fails for any reason, simply repeat the steps, starting back from the beginning with the PCB unplugged from your computer.v
