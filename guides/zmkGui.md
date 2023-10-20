---
title: ZMK GUI
description: How to use a GUI to configure your ZMK powered keyboard.
author: Boardsource
subcategory: easy
draft: false
tags: 
- zmk
- flashing
banner: https://boardsource.imgix.net/3f11ba0e-4a8f-4dd6-894d-4e275a073c4c.jpg
thumbnail: https://boardsource.imgix.net/f2a7c864-074e-406f-9c23-1d26813114e4.jpg?auto=format&ixlib=react-9.2.0&q=80&w=200&dpr=1
---

# Getting started with ZMK on a GUI!

One of the big put off's for people with ZMK has been the lack of GUI tools and
editing the keymap by hand. That's no longer the case thanks to
[Nick](https://github.com/nickcoutsos), one of the amazing community members.
This will work with any keyboard that ZMK supports, and we are making it even
easier to get up and running to start editing with their keymap editor on a
brand new board!

# Step 1: Pick your keyboard

We have made templates for our boards that support ZMK to make this easy for
anyone without the need to ever open the command line. Just select your keyboard
from the table below, and make sure you pick the controller that matches what's
in your keyboard. For example the nice!nano (or SuperMini uses the nice!nano),
or integrated if there is no controller that a user solders to the board.

| Nice!Nano/SuperMini                                                       | Blok | Integrated |
|---------------------------------------------------------------------------|------|------------|
| [Corne](https://github.com/boardsource/zmk-config_corne_nnv2)             |      |            |
| [Lily58/Lulu](https://github.com/boardsource/zmk-config_lily58_nnv2)      |      |            |
| [Microdox v2](https://github.com/boardsource/zmk-config_microdoxv2_nnv2)  |      |            |
| [Sweep](https://github.com/boardsource/zmk-config_sweep_nnv2)             |      |            |
| [TG4X](https://github.com/boardsource/zmk-config_tg4x_nnv2)               |      |            |
| [3x4 Macropad](https://github.com/boardsource/zmk-config_3x4_nnv2)        |      |            |
| [Sofle](https://github.com/boardsource/zmk-config_sofle_nnv2)             |      |            |

# Step 2: Create a reposity from the template.

You will need a GitHub account for this. If you don't have one, take a moment
now to create one. Not only does this make working with ZMK easier, it means
that your keymaps are always backed up and ready for you anywhere in the world!
Once you have an account, and are logged in, you'll create a repository for your
keyboard like this. Make sure to name the repository something you'll remember.
Many people use `zmk-keyboardNameHere`

![](https://images.boardsource.xyz/template%20how%20to.png)

# Step 3: Connect the GUI tool to the reposity you created

At this point, we are almost there! We'll want to go to [the keymap
editor](https://nickcoutsos.github.io/keymap-editor/) and follow the
instructions given. It will want you to connect your code from GitHub to the
tool so it can access and edit your keymap all in the tool.

# Step 4: Getting the files for your keyboard

![](https://images.boardsource.xyz/signal-2023-10-20-120918_002.png)

![](https://images.boardsource.xyz/signal-2023-10-20-120918_003.png)

We have everything we want, and just have to put it on the keyboard. 
In the editor, there's a save icon at the top. Make sure to hit that, and then
the button to the right. That will take you back to GitHub to get your firmware,
built automatically for you! If you see a yellow spinning icon or text like `0/2
jobs completed`, just wait a moment while it does the compiling for you. It may
take just a minute or two. Once it's all green, you'll see a file in the
Artifacts section called `firmware.zip`. Click that and download it. That will
be your firmware ready to go for your board! Make sure to extract the zip into
UF2 files. Split keyboards get 2 firmware. One for left, and one for right.
Make sure to not mix them up.

# Step 5: Flashing

This is the normal process for flashing your controller. With most controllers,
you can double tap reset, and you'll have a "flash drive" show up on your
system. You simply drop the UF2 file onto it, and it will flash and
automatically reboot, ready to go as a keyboard.
