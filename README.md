# Advanced Arduino H-Bridge control library

This is an Arduino library for the Toshiba TB6612FNG DC motor driver

## Features:
- Adjustable fader for smooth speed changes
- brake active or not in neutral mode
- selectable input signal range (e.g. 0 - 100, 0 - 1023, -255 - 255 etc.)
- selectable neutral position width. This allows you to optimize it for your joystick
- the motor rotation direction is reversible in software, so you don't have to switch your motor wires, if the direction is reversed
- The end-speed is adjustable during runtime. This allows you to simulate different gear ratios
- drive function returns true while driving or false while in neutral
- brakeActive function returns true, while the vehicle is getting slower. Used to control brake lights
- Backlash compensation for self balancing applications

New in V 1.1:
- Pin configuration moved to begin() function. This change was necessary due to new requirements in my new "Micro RC Receiver" V1.7 software revision
- If you've used the previous version in a project, you will have to change the pin configuration in accordance with the provided example. The archived V1.0 is enclosed and will not be maintained anymore.

New in V1.2:
- minPWM input variable added to the drive() function. Allows to eliminate the backlash in self balancing applications
- IMPORTANT!! You have to add this new input variable to your existing sketches! Ohtherwise it will not compile.


## Usage

See [example](https://github.com/TheDIYGuy999/TB6612FNG/blob/master/examples/TB6612FNG/TB6612FNG.ino).


(c) 2016 - 2017 TheDIYGuy999
