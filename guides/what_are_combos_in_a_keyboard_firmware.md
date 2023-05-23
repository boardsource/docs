# What are Combos in a Keyboard Firmware?

Combos are a feature that allows you to assign special functionality to combinations of key presses. Different keyboard firmwares may have different implementations and options for combos, but the basic idea is the same. Some of the common types of combos are:

- **Chords**: Chords are combos that match keys in random order, all pressed within a short time window (usually 50ms or less). For example, you can define a chord that activates KC.ESC when you press KC.A and KC.S together.
- **Sequences**: Sequences are combos that match keys in order, pressed within a longer time window (usually 1s or more). For example, you can define a sequence that activates KC.LWIN when you press KC.A, KC.B and KC.C in order.
- **Leader keys**: Leader keys are special keys that start a sequence of key presses that trigger an action. For example, you can define a leader key that activates KC.LWIN when you press KC.LEAD followed by KC.A.
- **Tap-dance**: Tap-dance is a feature that allows you to assign different actions to the same key based on how many times you tap it. For example, you can define a tap-dance key that activates KC.ESC on one tap, KC.LCTL on two taps and KC.LALT on three taps.

Combos can be useful for saving space on your keyboard, adding functionality to your keys, or creating shortcuts for common tasks. You can define combos to listen to any valid key, even internal or functional keys, like HoldTap or LayerTap¹. However, you need to be careful not to create conflicts or ambiguities with your combos, as they may interfere with your normal typing or gaming.

If you want to use combos on your keyboard firmware, you need to check the documentation and configuration options for your specific firmware. Some of the popular keyboard firmwares that support combos are:

- **KMK Firmware**: KMK Firmware is an open source firmware for computer keyboards written and configured in CircuitPython. It supports chords and sequences as well as other advanced features like RGB lighting and Bluetooth connectivity.
- **QMK Firmware**: QMK Firmware is an open source firmware for AVR and ARM based keyboards. It supports chords, sequences, leader keys and tap-dance as well as other advanced features like OLED display and MIDI support.
- **ZMK Firmware**: ZMK Firmware is an open source firmware for computer keyboards built on the Zephyr RTOS. It supports chords and sequences as well as other advanced features like wireless split keyboards and audio support.

These are some of the keyboard firmwares that support combos. If you are interested in using combos for your keyboard or device, you can follow the getting started guide or visit the website for more information for your specific firmware.

(1) kmk_firmware/combos.md at master · KMKfw/kmk_firmware. https://github.com/KMKfw/kmk_firmware/blob/master/docs/en/combos.md.
(3) QMK Firmware. https://docs.qmk.fm/.
(4) Combos - Vial. https://get.vial.today/manual/combos.html.
