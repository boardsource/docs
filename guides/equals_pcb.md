---
title: Guide to the new Equals PCB
description: Everything you could want to know about the equals PCB.
author: Boardsource
product_link: https://boardsource.xyz/store/5ec9fc5d64caf04f83aa646c
subcategory: easy
draft: false
tags:
- building
- programming
- learning
banner: https://images.boardsource.xyz/equals_smt_pcb_mx_components_replaced.png
thumbnail: https://images.boardsource.xyz/equals_smt_pcb_mx_components_1_1.png
---


# Introduction


The equals PCB was designed to be our new ortho layout PCB. We tried to make a PCB that will last the test of time and be a great core to your ortho keyboard for years to come.
We have done so by bringing every feature we could think of to this well know and loved layout.


## So whats 60 and 48?
So the Equals PCB is a 5x12 ortho PCB that in that config is the equals 60 you can snap off the bottom row to have a equals 48.
I know explaining the joke makes sure its not funny. 
But the story behind the name is kinda a math play on words. 5x12=60 4x12=48, so.... =60 -> equals 60 (meaning 60 keys).


## Case compatibility
The equals PCB is designed to be compatible with the following cases:


* **MX**
    - [Equals 60 mx](https://boardsource.xyz/store/5ec9fc5d64caf04f83aa646c)
    - [Equals 48 mx](https://boardsource.xyz/store/5ec9fc5d64caf04f83aa646c)
* **LP**
    - [Equals 60 lp](https://boardsource.xyz/store/5ec9fc5d64caf04f83aa646c)
    - [Technik](https://boardsource.xyz/store/5ffb9b01edd0447f8023fdb2) * see notes


## Features


Lets get all the basic features out of the way that were there on the old Technik PCB


* **UBB-C**
* **perkey rgb lighting**
* **underglow rgb lighting**


Now whats new


* RP2040 MCU
* 16mb of rom
* [Peg](https://peg.software/) support
* 2u spacebar support
* piezo buzzer
* OLED both 32x128 && 64x128
* 1.8 Inch Full Color 128x160 SPI TFT
* exposed pins for you to hack on


## Pin out


![PCB image](https://images.boardsource.xyz/equals_pinout.jpg)




| image key | pin name | python name | function      | alt function         |
|-----------|----------|-------------|---------------|----------------------|
| 1         | RST      | NA          | reset board   | NA                   |
| 2         | BOOT     | NA          | UF2 boot mode | NA                   |
| 3         | BOOT     | NA          | UF2 boot mode | NA                   |
| 4         | RST      | NA          | reset board   | NA                   |
| 5         | gpio22   | SDA         | I2c SDA       | digital input output |
| 6         | gpio23   | SCL         | I2c SCL       | digital input output |
| 7         | VCC      | NA          | 3.3v          | NA                   |
| 8         | GND      | NA          | GND           | NA                   |
| 9         | VCC      | NA          | 3.3v          | NA                   |
| 10        | gpio25   | GP25        | SPI CS        | digital input output |
| 11        | gpio20   | GP20        | SPI dc        | digital input output |
| 12        | gpio28   | GP28        | SPI rx        | ADC                  |
| 13        | gpio27   | GP27        | SPI tx        | ADC                  |
| 14        | gpio26   | GP26        | SPI sck       | ADC                  |
| 15        | VCC      | NA          | 3.3v          | NA                   |
| 16        | GND      | NA          | GND           | NA                   |


### **Not listed in the image**


| pin name | python name | function      |
|----------|-------------|---------------|
| gpio0    | TX          | col 0         |
| gpio1    | RX          | col 1         |
| gpio2    | GP02        | col 2         |
| gpio3    | GP03        | col 3         |
| gpio4    | GP04        | col 4         |
| gpio5    | GP05        | col 5         |
| gpio6    | GP06        | col 6         |
| gpio7    | GP07        | col 7         |
| gpio8    | GP08        | col 8         |
| gpio9    | GP09        | col 9         |
| gpio10   | GP10        | col 10        |
| gpio11   | GP11        | col 11        |
| gpio12   | GP12        | row 0         |
| gpio13   | GP13        | row 1         |
| gpio16   | GP16        | row 2         |
| gpio17   | GP17        | row 3         |
| gpio18   | GP18        | row 4         |
| gpio21   | GP21        | rgb led pin   |
| gpio24   | GP24        | status led    |
| gpio29   | GP29        | buzzer pin   |




## Screens


So you can see there are 2 pin headers exposed on the PCB.
These are exposed for you to have access to a funky split ortho style keyboard.
You can remove the center 2 columns of switches and install an OLED or a TFT screen.
While full color TFT screens are not supported in peg yet, they are supported in Circuitpython and in QMK.
Much like OLEDS before they are not super helpful per say but they are cool to look at and with the 16mb of rom storage you should be able to load up quite a lot of animation frames or whatever you like to do the same things you would on an OLED.

* display current layer
* display wpm
* display keyboard state eg: win ctrl swap.
* just show off cool art (Now in full color!)


Doing so now moves this keyboard into a pseudo split 30% keyboard, with a very large screen.


Beyond installing a screen these pins were chosen to be used because you now have access to I2c and 3 ADC lines to hack on how you see fit.


## **Notes**
**When breaking off the bottom row slight trimming may be required to fit into Technik cases.**
**Old Technik plates will not work with the new PCB.**


**image key (1,2,3,4)**:If you want to swap the function of the two reset switches on the back of the PCB, you need to cut between the pads 2 and 4 and jump the pads 1 and 3.
Of course the standard firmware tricks for resetting your board make reset switches mostly unneeded.



