# Focuser
Focuser for Astronomy based on Arduino (usable by Indi)

This focuser is used with Indilib (http://indilib.org/)
It use the protcol Moonlite (As documented in the indilib project).
A LM335 is used as temperature sensor.
The Stepper Motor is controled by a A4988 Controller. This controler is used by a lot of 3D printer like the RepRap and it should be easy to find.

Features:
- Several speeds
- full, half, quater, eighth and sixteenth step
- temperature compensation (compensate the dilatation of the instrument)
- software temperature adjustement
- separate display

## Element used
- Arduino Uno ([link](https://www.arduino.cc/en/Main/ArduinoBoardUno))
- A bipolar stepper motor
- A Temperature Sensor LM335 ([Datasheet](http://www.ti.com/lit/ds/symlink/lm335.pdf))
- The [Moonlite Protocol](http://www.indilib.org/media/kunena/attachments/1/HighResSteppermotor107.pdf)
- A [A4988](https://www.pololu.com/file/0J450/a4988_DMOS_microstepping_driver_with_translator.pdf) Stepper motor controller

## Internal library
- LM335. Used to interface the temperature sensor
- Moonlite. Used to code and decode the Moolite protocol
- StepperControl_A4988. Used to command the stepper motor

## Extern library
- The graphical library [U8g2](https://github.com/olikraus/u8g2/)

## Compilation
This project used the standard Arduino file organisation. A main file in the the folder Focuser and the librairies used are in the folder libraires.
The Arduino IDE is recommanded for an easy compilation. 
To compile you need to copy or create some links in your Arduino directory (which is automaticaly created when you install the Arduino IDE).
The Arduino IDE can be found hier: [link](https://www.arduino.cc/en/Main/Software)

Compile and transfer the program to the Arduino.

When you start your Indi server use the **indi_moonlite_focus** module to enable the focuser. 
The software provided by Moonlite on Windows is also usable.

The library U8g2 support several displays. It is easy to adapt it to another one.
