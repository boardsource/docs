---
title: Single Key Not Working - A Troubleshooting Guide
description: Learn and follow the steps necessary to diagnose and fix a single key not working on your keyboard.
author: Boardsource
product_link: https://www.boardsource.xyz/products/MX_Hot_Swap_Sockets
subcategory: easy
draft: false
tags:
- building
- soldering
- learning
- troubleshooting
banner: https://images.boardsource.xyz/single_key_not_working_16_9.jpg
thumbnail: https://images.boardsource.xyz/single_key_not_working_1_1.jpg
---

# Single Key Not Working

Encountered a non-responsive key on your newly built mechanical keyboard? Fear not! This issue is a very common one for people to run into, and it's usually a very easy fix. Our guide is tailored to help you identify and fix the problem with ease.

Let's ensure you're in the correct troubleshooting zone before getting into it:

- If you've encountered an entire row or column of unresponsive keys you'll find assistance in a separate Help Article [here]. This troubleshooting steps and solutions in this guide do NOT apply if an entire row or column is not working.
- This guide is applicable even if multiple non-aligned keys malfunction. For example, if both 'S' and 'P' keys are unresponsive, you're in the right place.

## Step 1 - Inspect The Switch

Begin by examining the switch of the malfunctioning key. Often, a bent leg during insertion is the culprit. Inspect the back of the hotswap socket; ideally, both legs should be visible through the socket holes. A missing leg often indicates a bend.

If you see both of the switch's legs in the hotswap socket then the switch is likely not the reason the key doesn't work. You can check nearby hotswap sockets on keys you know function to see how it should look.

You can remove and inspect the switch separately if you're not sure. A visibly bent leg outside the keyboard obviously confirms this is at least one reason the key doesn't work.

To correct a bent leg, gently straighten it and re-insert the switch, ensuring full insertion into the hotswap socket, and confirm the switch was inserted without bending by checking the back of the PCB again. Make sure to support hotswap sockets from the back when inserting switches. If you don't, you can potentially break the socket away from the PCB.

**Tip:** Testing with an alternate switch can verify if the original switch is defective. However, such cases are extremely rare, typically stemming from a bent leg.

## Step 2 - Inspect Hotswap Socket

Inspect the hotswap socket associated with the problematic key closely. Occasionally, a socket might lack solder on one side or exhibit a "floating" solder joint, failing to establish a good connection with the PCB.

Determining a solid connection visually can be challenging, but sometimes there are obvious issues like a pad completely missing solder. Add solder to the pad(s) you think are missing solder or not making a good connection.

## Step 3 - Inspect Diode

Investigate the diode associated the key, similar to the hotswap socket inspection. Identifying the associated diode can be done by tracing the connection from the hotswap.

Similar to how we inspected the hotswap socket, ensure both diode pads have solder and are securely connected to the PCB. Sometimes it looks like there is a lot of solder on a side of the diode, but when inspected from the side you may notice it is floating and not flat against the PCB.

Missing solder or a pad not making a solid connection will stop the key from functioning. Add solder where it's missing, or de-solder the diode and re-install it flat so both sides are making a solid connection with the PCB.

## Step 4 - Re-flow All Pads Associated With the Key

If the key remains unresponsive after previous steps, it's time to re-flow the solder joints of all inspected components (both hotswap socket and diode pads, 4 solder joints in total).

Even if you feel like all the components passed your visual inspection re-flowing these joints ensures a secure connection.

Reflowing means to heat each joint until the solder melts and then allowing it to cool. You do not always need to add solder, usually just heating and allowing it to cool will work, but it won't hurt to add a bit of solder if you want.

## Step 5 - Replace Components

On rare occasions, components might be defective. If the issue persists after re-flowing all of the pads:

1. Replace the diode, as it's the most likely component to fail (though still extremely rare).
2. Consider replacing the hotswap socket next.
3. If problems continue, try substituting the switch, assuming it hasn't been replaced already.

If you're still running into issues, then reflow all of the pads again just to rule out soldering being the reason for the defective key.

## Step ∞ - Advanced Troubleshooting

Exhausted all previous steps without success? You might face a rare hardware issue or PCB defect.

Join our Discord server by following [this invite link](https://discord.gg/6ZNvRMFj) and seek guidance in the build help channel and explain the troubleshooting steps you've taken. Our community can assist in isolating the issue further and helping to test for hardware issues.

Happy typing!
