---
title: Guide to the Unicorne PCB
description: Everything you need to know about the Unicorne PCB by Boardsource.
author: Boardsource
product_link: https://boardsource.xyz/store/unicorne-pcb
subcategory: easy
draft: true
tags:
- building
- programming
- learning
banner: https://images.boardsource.xyz/unicorne_pcb_guide_16_9.jpg
thumbnail: https://images.boardsource.xyz/unicorne_pcb_guide_1_1.jpg
---

# Introduction

The Unicorne PCB, designed by Boardsource, is a cutting-edge split keyboard PCB powered by an RP2040 microcontroller with 16MB of ROM on each side. This PCB is perfect for those looking to build a unique and feature-rich keyboard. In this guide, we will cover all the essential information you need to make the most of your Unicorne PCB.

## Key Features

The Unicorne PCB boasts a wide range of features that set it apart from other keyboards. Here's what you can expect:

* **Split Design:** The Unicorne PCB is split into two halves, making it an ergonomic choice for typists who want a comfortable and customizable typing experience.

* **RP2040 MCU:** Each side of the Unicorne PCB is powered by an RP2040 microcontroller, providing ample processing power for advanced features and customization.

* **16MB of ROM:** With 16MB of ROM on each side, you have plenty of space for storing keymaps, macros, and even animations for OLED displays.

* **OLED Support:** The Unicorne PCB comes with pre-installed OLED headers, allowing you to easily add OLED screens to both halves of your keyboard. You can display current layer information, typing speed (WPM), keyboard status, or simply showcase cool art.

* **RGB Perkey & Underglow** The Unicorne PCB supports vibrant RGB per-key lighting for individual key customization and dynamic underglow lighting to illuminate your workspace in style.

* **USB-C Connectivity:** The Unicorne PCB uses USB-C to USB-C cables to connect the two halves, ensuring a stable and reliable connection between the split keyboard sections.

* **Joystick Support:** Each side of the Unicorne PCB has a dedicated joystick input, making it a great choice for gaming or navigating menus.

* **Boot and Reset Switches:** Conveniently located on the top of the PCB, labeled boot and reset switches make it easy to access and manage firmware updates and resets.

* **Breakaway Outer Column:** The Unicorne PCB's outer columns are breakaway, allowing you to create a 5-column Corne keyboard for a compact 30% keyboard design.

* **Backwards Compatibility with Corne/CRKBD PCBs:** The Unicorne PCB is fully backward compatible with the Corne/CRKBD PCB, ensuring that any case designed for the Corne will also fit the Unicorne seamlessly.

## Pin Configuration


### **Left Half**

| Pin Name | Python Name | Function                     |
|----------|-------------|------------------------------|
| gpio0    | TX          | Split Com                    |
| gpio1    | RX          | Split Com (defaults disabled)|
| gpio2    | GP02        | Column 0                     |
| gpio3    | GP03        | Column 1                     |
| gpio4    | GP04        | Column 2                     |
| gpio5    | GP05        | Column 3                     |
| gpio6    | GP06        | Column 4                     |
| gpio7    | GP07        | Column 5                     |
| gpio8    | GP08        | Encoder A (MX Only)          |
| gpio9    | GP09        | Encoder B (MX Only)          |
| gpio14   | GP14        | Row 0                        |
| gpio15   | GP15        | Row 1                        |
| gpio16   | GP16        | Row 2                        |
| gpio17   | GP17        | Row 3                        |
| gpio18   | GP18        | Command Pin                  |
| gpio22   | GP22        | OLED SDA                     |
| gpio23   | GP23        | OLED SCL                     |
| gpio25   | GP25        | SPI CS                       |
| gpio26   | GP26        | Joystick X & SPI SCK         |
| gpio27   | GP27        | Joystick Y & SPI TX          |
| gpio29   | GP29        | RGB LED Control              |

### **Right Half**

| Pin Name | Python Name | Function                     |
|----------|-------------|------------------------------|
| gpio0    | TX          | Split Com                    |
| gpio1    | RX          | Split Com (defaults disabled)|
| gpio2    | GP02        | Column 0                     |
| gpio3    | GP03        | Column 1                     |
| gpio4    | GP04        | Column 2                     |
| gpio5    | GP05        | Column 3                     |
| gpio6    | GP06        | Column 4                     |
| gpio7    | GP07        | Column 5                     |
| gpio8    | GP08        | Encoder A (MX Only)          |
| gpio9    | GP09        | Encoder B (MX Only)          |
| gpio14   | GP14        | Row 0                        |
| gpio15   | GP15        | Row 1                        |
| gpio16   | GP16        | Row 2                        |
| gpio17   | GP17        | Row 3                        |
| gpio18   | GP18        | Command Pin                  |
| gpio22   | GP22        | OLED SDA                     |
| gpio23   | GP23        | OLED SCL                     |
| gpio25   | GP25        | SPI CS                       |
| gpio26   | GP26        | Joystick X & SPI SCK         |
| gpio27   | GP27        | Joystick Y & SPI TX          |
| gpio28   | GP28        | Buzzer Control (Right)       |
| gpio29   | GP29        | RGB LED Control              |


## Case Compatibility

The Unicorne PCB is designed to fit seamlessly into compatible cases. Below is a list of cases that are compatible with the Unicorne PCB:

* **MX Cases:**
    - [Unicorne MX Case](https://www.boardsource.xyz/products/unicorne)
    - [FR4 Corne Case](https://www.boardsource.xyz/products/Corne)

* **LP Cases:**
    - [Unicorne LP Case](https://www.boardsource.xyz/products/unicorne-LP)
    - [Corne LP](https://www.boardsource.xyz/products/Corne_LP)
    - [FR4 Corne Case](https://www.boardsource.xyz/products/Corne)


## Getting Creative

One of the standout features of the Unicorne PCB is the exposed pins that allow for customization and hacking. You can take advantage of the following functionalities:

* **Full-Color TFT Screens:** While full-color TFT screens are not yet supported in Peg, they can be used with CircuitPython and QMK. These screens are perfect for displaying various information, animations, or even just cool art.

* **I2C and ADC Lines:** With access to I2C and three ADC lines, you have the flexibility to experiment and create custom functionalities or expand your keyboard's capabilities.

## Notes on Programing
The Unicorne PCB comes pre flashed with a QMK via map, to be used with [VIA](https://usevia.app/).
You can use [QMK Configurator](https://config.qmk.fm/#/boardsource/unicorne/LAYOUT_split_3x6_3) to reprogram your keyboard.

And of course you can swap over to BS-python and use peg, [here](https://peg.software/docs/board-update) is guide on how to do that.
then you can plug it into peg and let it take care of the rest.

## Lets Talk About Getting Into The Bootloader
Being that its flashed With QMK by default you can hold down the top left key as you plug it in, this will put you into bootloader. 
And there is the classic that will always work of holding down the boot switch and pushing the reset switch then letting go of the boot switch.

The boot and reset switches are labeled on the PCB, but we will stat it here too. 
Boot is the right most switch rest is the left most switch. 

This is a rp2040 keyboard so you never need to use QMK Toolbox. 
As soon as you get your keyboard into bootloader it will show up as a drive named "RPI-RP2" now you can drag and drop your new keymap onto it.
