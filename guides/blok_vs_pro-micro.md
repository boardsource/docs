

## Pro Micro vs. Blok: Exploring Controller Differences in Keyboard Firmware

When it comes to building custom keyboards, the choice of controller plays a crucial role in determining the capabilities and features of your keyboard. Two popular controller options, the Pro Micro and the Blok, offer unique advantages and compatibility with different firmware options. In this article, we'll delve into the differences between these controllers and how they function within the same keyboards, focusing on their compatibility with QMK, KMK, and ZMK firmware.

### Pro Micro: ATmega32U4 Controller

The Pro Micro, powered by the ATmega32U4 microcontroller, has long been a popular choice for custom keyboard enthusiasts. Its compact size, affordability, and compatibility with QMK firmware have made it a staple in the community.

The ATmega32U4 controller is based on the AVR architecture and features a USB interface for easy communication with your computer. It offers sufficient processing power to handle keypresses, handle key matrix scanning, and execute custom functions defined by the firmware. With QMK firmware, you can unleash the full potential of the Pro Micro, remapping keys, creating macros, and implementing advanced features.

### Blok: RP2040 Controller

The Blok, on the other hand, is equipped with the RP2040 microcontroller, which is based on the ARM Cortex-M0+ architecture. The RP2040 brings increased performance, improved power efficiency, and additional capabilities to the table.

The Blok's RP2040 controller offers native USB support, enabling seamless connectivity and smooth communication with your computer. While the Blok is compatible with QMK firmware, it requires a slight adjustment during the compilation process. To compile your keymap for the RP2040 controller, you need to use the `CONVERT_TO=blok` flag when running the QMK compilation command. This ensures that the firmware is generated with the correct settings and optimizations for the Blok's RP2040 controller.

Examples:

**Using QMK CLI:**

>qmk flash -c -kb boardsource/microdox/v2 -km default -e CONVERT_TO=blok

**Using make:**

>make boardsource/microdox/v2:default CONVERT_TO=blok

For more information on QMK converters see the [docs](https://docs.qmk.fm/#/feature_converters?id=overview)

Furthermore, the Blok stands out from the Pro Micro by offering compatibility with other firmware options beyond QMK. It can run both KMK and ZMK firmware, providing additional customization possibilities and a different approach to programming your keyboard.

### Choosing the Right Controller for Your Custom Keyboard

When selecting between the Pro Micro and the Blok, consider your specific requirements and preferences. If you prefer the familiarity of QMK firmware and ability to use the [QMK Configurator](https://config.qmk.fm/#/boardsource/microdox/v2/LAYOUT_split_3x5_3) the Pro Micro with its ATmega32U4 controller is a reliable choice.

On the other hand, if you seek improved performance and the ability to explore alternative firmware options such as KMK and ZMK, the Blok with its RP2040 controller offers a compelling solution.

It's important to note that while both controllers work within the same keyboards and can run QMK firmware,the Pro-Micro is a default and easy option with lots of information and documentation about it. But the Blok provides the added flexibility of supporting KMK and ZMK firmware. This opens up a broader range of customization options and allows you to experiment with different firmware ecosystems.

