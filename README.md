Arduino Battery Capacity Tester 3.1
===================================

Adapted from [Hesham Moshiri's code](https://www.instructables.com/Battery-Capacity-Tester-Using-Arduino-Lithium-NiMH/) as [modified by Debasish Dutta](https://www.opengreenenergy.com/post/arduino-battery-capacity-tester-v2-0) but still using Hesham's [PCB layout](https://www.pcbway.com/blog/technology/Battery_capacity_measurement_using_Arduino.html)). Ported to [lcdgfx](https://github.com/lexus2k/lcdgfx/) for handling the OLED. To the best of my knowledge the original idea for the hardware, and the very first sketch, came from Adam Welch, [who uses a Nokia LCD and some protoboard](http://static.adamwelch.co.uk/2016/01/lithium-ion-18650-battery-capacity-checker/) for it.

## Features

- cleaned-up UI, including zero-padded running time
- cleaned-up code, including some comments
- reasonably pleasant/appropriate buzzer sounds
- error message for "no battery attached"

## How to use?

This sketch can be used with either the Arduino IDE (just open the `.ino` file inside of the `CapacityTester` folder – but you'll have to read the `#include` statements and install libraries manually) or with PlatformIO (clone this repository, then execute `pio run -t upload` with the Arduino Nano connected to the computer via USB; libraries will be downloaded and installed for you). Before uploading it, you might want to use a multimeter to measure your power supply's exact voltage and note that down under `#define VCC` in the sketch as that directly influences the battery voltage measurement. If someone wants to implement setting that from the Nano's internal voltage reference, I'll gladly accept a PR! 
