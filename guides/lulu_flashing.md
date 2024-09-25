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

> This page is meant to be a reference to flashing your lulu SMT PCB.

Please note that updating and making edits to your keymap is not covered here, the lulu is now shipped to work with [QMK Configurator](https://config.qmk.fm/#/boardsource/lulu/rp2040/LAYOUT). In QMK Configurator, create your layout, compile it, and then download the firmware, it will download as a Uf2 file.

Please follow this guide in it's entirety, but if you feel you need additional help, feel free to [enter our Discord server](https://discord.gg/b4R25WSZvH) and ask for help under in the #hardware-help channel.

## Flashing Process

First, unplug your lulu PCB from the computer.

The easiest way to get the PCB into boot mode is to plug the keyboard back into the computer while holding down the outside upper corner key down.

After a few moments, your PCB should appear as a Drive on your computer named  "RPI-RP2.”

With the Drive "RPI-RP2" located on your computer you can drag and drop the Uf2 files onto the drive (onto the PCB). When it is done transferring the file, your PCB will reboot. When the board restarts it will no longer be in Boot mode and will be good to go. Do this with both halves of the board.

If you’ve successfully transferred the Uf2 file, you should see the LEDs turn back on. If the transfer fails for any reason, simply repeat the steps, starting back from the beginning with the PCB unplugged from your computer.
