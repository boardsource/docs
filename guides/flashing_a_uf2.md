---
title: How To Flash A Keyboard with .UF2
description: How To Flash A Keyboard with a uf2 bootloader.
author: Boardsource
product_link: https://boardsource.xyz/store/628b95b494dfa308a6581622
subcategory: easy
draft: false
tags: 
- qmk
- via
- uf2
- bootloader
- flashing
banner: https://images.boardsource.xyz/boot_loader.jpg
thumbnail: https://images.boardsource.xyz/uf2,boot_loader.jpg
---


# How To Flash A Keyboard with.UF2

This guide will show you how to flash a keyboard with a.uf2 bootloader.

## Step 1: Get the.uf2 file

First, you will need to get the.uf2 file for your keyboard. You can get a .UF2 file by following our [guide for QMK Configurator](https://www.boardsource.xyz/docs/guides-qmk_configurator) or from [VIA](https://www.caniusevia.com/docs/download_firmware) or by following our [ZMK GUI guide](https://www.boardsource.xyz/docs/guides-zmkGui)

## Step 2:  Get into Boot loader

So you have the.uf2 file, now you need to get into the bootloader. This can be done a lot of ways I will list them here from easy to hard.

* Hold down special key while you plug in the keyboard.
    * This is the easiest way to get into you bootloader. 
    But it only works if you keyboard is already flashed with QMK.
    The key you would need to hold down is the key is the first key on the first column.
    99% of the time that's the escape key.
    on a split keyboard it would be escape (for the left side) and `y` or `6` (for the right side)
* Double tap your reset switch.
    * Like the method above this only works if your keyboard is already flashed with QMK.
    This is a little bit more annoying then holding down a key because you may need to open your keyboards case to gain access to your reset switch.
* Hold down boot switch while you plug in your keyboard.
    * if your keyboard is using a RP2040 (Blok, Lulu, Unicorne) you will have a boot switch and a reset switch. Please refer to your keyboard or controller on how to locate it.
* Hold down boot switch while you tap your reset switch. 
    * here you need to have access to both BOOT and RESET Switches and you simply hold down the boot switch while you tap the reset switch. (some keyboard use a slide switch for boot to make this easier)

### Now you know all the ways you can get access to your boot loader how do you know one of them worked?

As soon as you get into bootloader a new drive will show up on your computer. This drives name will be "RPI-RP2" or "Nicenano" 
![boot loader drive](https://images.boardsource.xyz/boot_loader.jpg)


## Step 3: Flash the.uf2 file

Once you have gotten your board into bootloader and you can access the "flash drive" all you need to do is simply copy over you .UF2 file  example shown in gif below.

![how to flash uf2](https://images.boardsource.xyz/how_to_uf2_flash.gif)


After the file is done transferring your keyboard will restart and you should no longer be in bootloader mode. 
At this point your done and nothing else is needed.
Use your keyboard and enjoy.

## Extra
For questions, ask in [Boardsource Discord
server](https://discord.gg/5qpqbgaTYz)
