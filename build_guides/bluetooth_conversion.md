---
title: From Wired to Bluetooth
description: How To Add Bluetooth to Most Keyboards
author: Boardsource
subcategory: easy
draft: true
tags: 
- 40%
- 60%
- ergo
- kit
banner: 
thumbnail: 
---

### Hardware
| Item                      | Count | Required    |
|---------------------------|-------|-------------|
| BLE Controller            | 1/2   | [x]         |
| Battery                   | 1     | [x]         |
| Battery Helper PCB        | 1/2   | []          |
| Power Switch              | 1     | []          |
| Keyboard Kit (solderable) | 1     | [x]         |
| Milmax sockets/pins       | 1/2   | []          |

# The hardware changes

Building a bluetooth keyboard is very similar to building a wired keyboard. The
main difference is changing out the controller to something that supports
bluetooth, and a battery to give it power. Controllers like the
[Nice!Nano](https://www.boardsource.xyz/products/nice!nano_v2) and
[SuperMini](https://www.boardsource.xyz/products/supermini) will both work with
bluetooth and replace a pro micro/elite C/blok as those don't have a wireless
function.

# When to buy optional items

For things like the [Battery
Helper](https://www.boardsource.xyz/products/Battery-Helper), these are useful
if your PCB does not support a battery+switch as many keyboards were built
without wireless in mind. While you do not need a switch, it's highly
recommended to be able to turn off your keyboard for storage or transport. The
power switch is usually supported on any keyboard if it already supports a
battery. The most common power switch for keyboards is
[this](https://www.boardsource.xyz/products/smd-slide-switch), and one is
included with the battery helper if you use that. Milmax sockets and pins are
massively recommended as they allow you to easily remove the controller if you
want to test things, or if something goes wrong and you need to replace it.
Desoldering controllers from standard headers is quite difficult, and most
people would not want to go through that should they need to repair/replace
anything.

# PCB's that include battery+switch support

This is a short list of keyboards that we offer that do not need the battery
helper if you want to use a power switch. These PCB's have the function
integrated into the keyboard. Anything not on this list will likely need a
battery helper.

- Corne
- Sweep

# Installing the battery

If you are using the battery helper, you can see the [documentation for that
here.](BatteryHelper.md)

For other keyboards that integrate batteries and switches, please reference the
image below for their pinout and where to connect them.

### Corne

Photo of corne with battery attached
Image of corne pins for power switch and polarity for battery

### Sweep

Photo of sweep with battery attached
Image of sweep pins for power switch and polarity for battery

# Final checks

It's recommended to check power switch (if used), and the voltage of the battery
with a multimeter to ensure that the controller is getting the correct voltage.
Most controllers will flash a light when they see power, but this is a good
thing to check before you start wrapping things up. It may be a good idea to
flash a firmware before installing the controllers as well as it may be easier
to debug.

# Further reading

Some other useful articles that we have about ZMK may help you get your firmware
in working order.

[What is ZMK?](../guides/what_is_zmk.md)

[A GUI for ZMK!](../guides/zmkGui.md)

[How to Flash](../guides/flashing_a_uf2.md)

## Extra
For questions, ask in [Boardsource Discord
server](https://discord.gg/5qpqbgaTYz)
