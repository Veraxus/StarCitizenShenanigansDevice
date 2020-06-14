# Star Citizen Shenanigans Device
A community-driven repository on how to build and configure Yroethiel's amazing home-built Star Citizen controller.

**This repository is a WORK IN PROGRESS. If you have anything to contribute, please open a pull request.**

Version 1: https://www.youtube.com/watch?v=LTITm7ulwR4
Version 2: https://www.reddit.com/r/starcitizen/comments/gydvvi/touchscreen_interface_for_star_citizen/

## What Is It?
The Shenanigans Device is a left-handed 4dof controller for Star Citizen, created by Reddit user u/Yroethiel. It utilizes two small gimbaled sticks that are controlled with the forefinger and the thumb. Additionally, it incorporates either a custom keyboard or touchscreen for additional quick-access functions.

## How is it built?
Yrothiel has revealed the following components:

### Hardware
| Component                                   | Purpose                                                         | Link                                                                   |
|---------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------|
| Arduino Leonardo                            | Takes input from the gimbals and sends it to the PC as dxinput. | https://store.arduino.cc/usa/leonardo                                  |
| FrSky M7 Hall Sensor Gimbal (Taranis Q X7)  | Finger joysticks                                                | https://www.amazon.com/FrSky-Hall-Sensor-Gimbal-Taranis/dp/B073PPTH1C/ |

### Software
| Component                                   | Purpose                                                         | Link                                                                                                                  |
|---------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Arduino Joystick Library                    | Enables translation of hardware inputs to software.             | https://github.com/MHeironimus/ArduinoJoystickLibrary/blob/master/Joystick/examples/JoystickButton/JoystickButton.ino |

