---
title: Uno 1%
description: Getting you going with your new uno
author: Snipeye
source: https://github.com/Snipeye/Uno_IR_KMK
product_link: https://boardsource.xyz/store/5f2ef1b52bf5e8714a60f613
subcategory: easy
draft: false
tags: 
- 1%
banner: https://boardsourcev2.nyc3.digitaloceanspaces.com/uno_main_16_9_jumbo-1713547300461.jpg
thumbnail: https://boardsourcev2.nyc3.digitaloceanspaces.com/uno_main_1_1-1713546129237.jpg
---

# Uno Guide
## Building
Building the Uno is quite simple all you need to do is break the PCB into (dont worry its designed to do this) Next socket the top PCB(the one with the mx hotswap socket) Into the lower PCB(the one with the usb).
After that you can socket in a mx key switch and keycap, and you are ready to move onto programing.

## Programing 
### Uno_IR_KMK
This repository contains the code (and compiled circuitpython .uf2) to run KMK on the Uno IR.  This includes the keyboard files for easy remapping, as well as a plugin/module to handle the infrared decoding.

### IR Decoding
The IR Decoding module is, to the best of my knowledge, a novel approach: it should handle most IR protocols and deocde consistently - though it may not always decode in the manner intended by the manufacturer.  It has so far been tested with NEC and Sony IR protocols, but is generic enough that I expect it to work with most consumer remotes.

### Installation
When you plug the Uno IR into your computer, a new drive will mount (like a USB flash drive) named "RPI-RP2".
1. Copy the ```firmware.uf2``` file to this drive.  After the copy finishes (it will take a minute), the drive should automatically unmount, then a new drive will mount named "CIRCUITPY".
2. Delete all the files on the CIRCUITPY drive.
3. Copy all the files inside the "board" directory from this repository into the CIRCUITPY drive.  The file structure should now look like: ```CIRCUITPY/uno.py``` and ```CIRCUITPY/main.py```... etc.

### Modification
```main.py``` contains the keymap (keyboard.keymap) and the IR Map (irHandler.map) (like a keymap, but maps IR codes to functions instead of button presses to functions), as well as the encoder map (encoder_handler.map) if you've soldered an encoder on.  For instructions on how to build macros, etc, I recommend taking a look at the [KMK Documentation](http://kmkfw.io).