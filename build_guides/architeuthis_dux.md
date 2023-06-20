### This guide is for *KEYBOARDNAME* PCBs.
https://i.imgur.com/OBw7vIf.jpg
# Parts
### Required 
| Item | Count |
|------|-------|
| DIODESTYLE Diodes | SWITCHCOUNT |
| PCB | PCBCOUNT |
| CONTROLLERSTYLE or similar microcontroller | CONTROLLERCOUNT |
| TRRS Jack | 2 | 
| TRRS Cable | 1 | 
| Reset Switch | 2 | 
| SOCKETSTYLE Hotswap Sockets | SWITCHCOUNT | 
| SWITCHSTYLE Switches | SWITCHCOUNT | 
| *KEYCAPSTYLE* Keycaps | SWITCHCOUNT |

### Optional 
| Item | Count | 
|------|-------|
| 128x32 OLED Display | 2 | 
| SK6812 Mini-E LED | *SWITCHCOUNT* |
| WS2812B LED | 8 |
| EC11 Encoder + Knob | 2 |
| Piezo Buzzer (AST1109MLTRQ) | 2 |

![components](https://i.imgur.com/ZQ76UcC.jpg)

# Soldering
## Diodes
**Orientation**: Black bar facing downwards or towards the footprint indicator.
1. Solder one pad.
![one pad - diode](DIODECLOSEUPIMG1)
2. While holding diode with tweezers, reflow solder and place diode down on pad.
![diode placed](DIODECLOSEUPIMG2)
3. Solder other pad.
![diode complete](DIODECLOSEUPIMG3)
- Note, when working with [MELF](https://en.wikipedia.org/wiki/Metal_electrode_leadless_face) package diodes,
you may need to reflow and add more solder a couple times before an adequate connection is made.

## LEDs
**Orientation**: Notched corner/pin facing the pad marked with rectangle. This applies for both SK6812 Mini-E & WS2812B LEDs.
![sk6812 mini e orientation](LEDORIENTATIONIMG1)
![ws2812b orientation](LEDORIENTATIONIMG2)
- Notes: \
\- This component is heat sensitive. Be cautious and work at a safe temp (~300c). \
\- It is wise to test the LEDs as you solder then. Consider [soldering your controllers beforehand](#microcontrollers). \
\- The LED order is somewhat outlined ![LED order](LEDORDERIMG) and should be followed in order when building.
1. Solder one pad. (it may be easier to solder all 4 pads before placing LED down when installing WS2812B LEDs)
![sk6812 mini e one pad](LEDCLOSEUPIMG1)
![ws2812b 4 pads](LEDCLOSEUPIMG2)
2. While holding LED with tweezers, reflow solder and place LED down on pad.
![sk6812 mini e placed](LEDCLOSEUPIMG3)
![ws2812b placed](LEDCLOSEUPIMG4)
3. Solder remaining pads.
![sk6812 mini e complete](LEDCLOSEUPIMG5)

## Hotswap sockets
1. Solder one pad.
![Hot swap socket foot print soldered](https://i.imgur.com/K9iFUF1.jpg)
2. While holding hotswap socket (fingers are fine), reflow solder and place socket down on pad.
![Hot swap socket one pin soldered](https://i.imgur.com/6mw1P1j.jpg)
3. Solder other pad.
![Hot swap socket finished](https://i.imgur.com/Gu1ZaG4.jpg)
- Note, don't hesitate to use a little extra solder, as that will help secure the socket and prevent it from being ripped off.

## Microcontrollers
**Orientation**: Both microcontrollers CONTROLLERPLACEMENT.
- Note, it is recommended to flash each microcontroller prior to soldering. See [firmware](#firmware) section for more.
1. Insert headers from front, solder in from the back.
![headers inserted](https://i.imgur.com/qiEeM6d.jpg)
2. Place microcontroller CONTROLLERPLACEMENT. 
![microcontroller placed](https://i.imgur.com/5ApcPZW.jpg)
3. Apply solder to all pins.
4. Use flush cutters or similar to trim excess from pins on each side.
![microcontroller finished](https://i.imgur.com/fNjfIpO.jpg)

## OLEDs
1. Insert headers from front, solder in from the back.
![Oled placed](OLEDCLOSEUPIMG1)
2. Solder only one of pins to begin with.
![oled back one pin soldered](OLEDCLOSEUPIMG2)
3. While reflowing solder joint, position OLED so that it is level & straight.
4. Solder remaining pins and clip extra length of pins.
![oled finished](OLEDCLOSEUPIMG3)

## Misc.
### TRRS jacks
1. Position TRRS jack on front of PCB and secure with tape.
![trrs jack placed](https://i.imgur.com/hPTzQyx.jpg)
2. Apply solder to all four pins.
![trrs jack finished](https://i.imgur.com/hKw5Hjw.jpg)
### Reset switches
1. Solder one pad.
![reset switch placed](RESETCLOSEUPIMG1)
2. While holding switch with tweezers, reflow solder and place switch down on pad.
3. Solder remaining pads.
![reset switch placed](RESETCLOSEUPIMG2)



## Firmware

### QMK
In qmk this keyboard can be found under QMKKEYBOARDNAME.
To begin, follow the [QMK setup guide](https://docs.qmk.fm/#/newbs_getting_started). (if working from an existing installation, an [update](https://docs.qmk.fm/#/newbs_git_using_your_master_branch?id=updating-your-master-branch) may be needed.) \
For flashing instructions, see [doc](https://docs.qmk.fm/#/newbs_flashing) or [video](https://www.youtube.com/watch?v=fuBJbdCFF0Q)

### KMK / PEG
In Peg or KMK this keyboard can be found under KMKKEYBOARDNAME

Peg can be downloaded [here](https://peg.software/), and the quick start can be seen [here](https://peg.software/docs/Peg_Client/#quick-start-and-testing).

For Kmk can be downloaded [here](https://github.com/KMKfw/kmk_firmware) and the quick start can be seen [here](http://kmkfw.io/docs/Getting_Started#tldr-quick-start-guide)



## Extra
For questions, ask in [Boardsource Discord server](https://discord.gg/5qpqbgaTYz)