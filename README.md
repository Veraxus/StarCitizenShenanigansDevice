# Star Citizen Shenanigans Device
A community-driven repository on how to build and configure Yroethiel's amazing home-built Star Citizen controller.

**This repository is a WORK IN PROGRESS. If you have anything to contribute, please open a pull request.**

## What Is It?
The Shenanigans Device is a left-handed 4dof controller for Star Citizen, created by Reddit user u/Yroethiel. It utilizes two small gimbaled sticks that are controlled with the forefinger and the thumb. Additionally, it incorporates either a custom keyboard or touchscreen for additional quick-access functions.

To-date, Yroethiel 
Version 1: https://www.youtube.com/watch?v=LTITm7ulwR4  
Version 2: https://www.reddit.com/r/starcitizen/comments/gydvvi/touchscreen_interface_for_star_citizen/  

## How is it built?
Yrothiel has revealed the following components:

### Control Board: Arduino Leonardo
Takes input from the gimbals and sends it to the PC as dxinput.

**Buy from:**  
* https://store.arduino.cc/usa/leonardo

### Gimbals: FrSky M7 Hall Sensor Gimbal (Taranis Q X7)
Takes input from the gimbals and passes it to the PC as dxinput.

**Buy from:**  
* https://www.amazon.com/FrSky-Hall-Sensor-Gimbal-Taranis/dp/B073PPTH1C/

### Software: Arduino Joystick Library
Enables translation of hardware input signals to software.

See: https://github.com/MHeironimus/ArduinoJoystickLibrary/blob/master/Joystick/examples/JoystickButton/JoystickButton.ino

## Keyboard / Pad

### V1 Physical Board
Yroethiel's V1 uses a custom designed keyboard PCB designed in KeyCAD and produced by a bespoke manufacturer. It includes 32 keys (the maximum for a joystick), with a 33rd for menu or calibration. Be careful when choosing LEDs. The ones mentioned in the V1 video were made from a cheap plastic that made soldering difficult. The key switches are Blue Zylents V2.

The software libraries used for the keyboard were [FastLED](http://fastled.io/) and [KeyPad](https://www.arduinolibraries.info/libraries/keypad). Joysticks were used to select the color of each key's RGB.

Yroethiel then added a calibration mode to handle noise, dead zones, and sensitivity of the joysticks. No further detail was provided on the implementation of this feature.


### V2 Tablet Board
In his V2 post, Yroethiel mentioned using a Raspberry Pi as a web server, hosting a custom GUI on Chromium in Kiosk mode. The RBP sends the signals to the Arduino via Serial connection.

### Alternate Tablet Board
GameGlass is a very popular tablet-based GUI for games. It can be loaded onto Apple, Android, or Amazon Fire tablets (Fire 7 or 10)... and may be a less expensive, more attractive option for a command board.
