---
title: Uno 1%
description: Getting you going with your new uno
author: Snipeye
source: https://github.com/Snipeye/Uno_IR_KMK
product_link: https://www.boardsource.xyz/products/uno
subcategory: easy
draft: false
tags: 
- 1%
banner: https://boardsourcev2.nyc3.digitaloceanspaces.com/uno_main_16_9_jumbo-1713547300461.jpg
thumbnail: https://boardsourcev2.nyc3.digitaloceanspaces.com/uno_main_1_1-1713546129237.jpg
---

# Uno Guide
## Building
Building the Uno is quite simple: all you need to do is break the PCB in two along the "mousebites" between the two halves - don't worry, it's designed for this! Next, socket the top PCB (the one with the MX hotswap socket and RGB LED) into the lower PCB (the one with the USB): it connects on the 2x4 block of header pins.  After that, you can socket in an MX key switch and keycap, and you are ready to move onto programing.  Alternatively, you can solder in a rotary encoder instead of using a keyswitch.

## Programing 
### Uno_IR_KMK
[This repository](https://github.com/Snipeye/Uno_IR_KMK) contains the code [(and compiled circuitpython .uf2)](https://github.com/Snipeye/Uno_IR_KMK/raw/main/firmware.uf2) to run KMK on the Uno IR.  This includes the keyboard files for easy remapping, as well as a plugin/module to handle the infrared decoding.  There are 3 different examples given: one that demonstrates the button, another that shows the rotary encoder, and a final one for use with IR.  You can combine pieces from the examples together easily.

### IR Decoding
To the best of Snipeye's knowledge, the IR decoding method a novel approach: it should handle most IR protocols and deocde consistently - though it may not always decode in the manner intended by the manufacturer.  It has so far been tested with NEC and Sony IR protocols, but is generic enough that it's expected to work with most consumer remotes.  For guidance on how to program it, take a look at the ```options/ir/main.py``` example in the repository.  For details on the decoding process, look into ```board/IRModule.py```.

### Installation
When you plug the Uno IR into your computer, a new drive will mount (like a USB flash drive) named "RPI-RP2".
1. Copy the ```firmware.uf2``` file to this drive.  After the copy finishes (it will take a minute), the drive should automatically unmount, then a new drive will mount named "CIRCUITPY".
2. Delete all the files on the CIRCUITPY drive.
3. Copy all the files inside the "board" directory from this repository into the CIRCUITPY drive. The file structure should now look like: ```CIRCUITPY/uno.py``` and ```CIRCUITPY/IRModule.py```... etc.*
4. Choose which example you want to work from - in the ```options``` folder, there are examples for the button only, the encoder, or the IR module: each should be fairly self-explanatory - you can build your own version, too. Depending on which option you want, look in the ```options/``` folder, pick a subfolder, and copy the contents to ```CIRCUITPY/``` - you should now have a ```CIRCUITPY/main.py``` plus, potentially, a couple other files (depending on the example).
* NOTE: The included ```boot.py``` adds a behavior that you may or may not want: when the Uno is plugged in, it will work as a keyboard as normal - but it will not mount the ```CIRCUITPY``` drive for easy editing *unless* you hold the button down while plugging the Uno in.  If this isn't desired behavior, don't copy the ```boot.py``` file over: without this file, the ```CIRCUITPY``` drive will mount whenever Uno is plugged in, regardless of whether the key is pressed or not.


### Modification
```main.py``` from the various examples contains the keymap (keyboard.keymap) or the IR Map (irHandler.map) (like a keymap, but maps IR codes to functions instead of button presses to functions), as well as the encoder map (encoder_handler.map) if you've soldered an encoder on.  For instructions on how to build macros, etc, I recommend taking a look at the [KMK Documentation](http://kmkfw.io).
