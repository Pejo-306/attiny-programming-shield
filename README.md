# ATTiny programming shield (using an Arduino Uno)

This project is a simple PCB design which can be used to program an
ATTiny(25/45/85) with an Arduino Uno as an ISP.

# Getting started

## Required parts
The following is a list of the parts used in this project:

* DIP 8-pin socket
* 10uF electrolytic capacitor
* Male pin headers 2.54mm pitch
  * 01x10 (1 piece)
  * 01x08 (1 piece)
* LED 5mm (optional)
* 220 ohm resistor (optional)
* Arduino Uno board
* ATTiny(25/45/85)

_Note_: all components use THT

The listed LED and resistor are optional and can be used as indication that the
Arduino is providing 5V power to the circuit.

## Assembling the board
After gathering the required parts, you can either order the PCB from your
favorite PCB manufacturer or create the PCB yourself. The circuit can also
be assembled on a breadboard with relative ease.

## Programming the ATTiny
You must first upload the example ISP sketch to the Arduino Uno 
(in the Arduino IDE: "File -> Examples -> 11.Arduino ISP -> Arduino ISP").
Afterwards, place both the Arduino Uno board and the ATTiny on the PCB.

You will need ATTiny board definitions for the Arduino IDE. The ones I
recommend (and use) are those by Spence Konde in his ATTinyCore github project
(link below). Other board definitions can also be used but you must research them
on your own.

After you have obtained the required board definitions, select the appropriate
one (i.e. ATTiny(25/45/85)) from the "Tools -> Board" menu in the Arduino IDE.
Select the port ("Tools -> Port") where the Arduino is connected. Under the 
"Tools -> Programmer" menu choose "Arduino as ISP". Afterwards, write your code
and upload it. If all goes well, then your ATTiny should be executing your
uploaded program.

_Note_: different ATTiny board definitions may have specific requirements
(such as the suggested ATTinyCore ones). Refer to your chosen board
definitions' documentation for more details.

## Using the ATTiny
If your code has successfully been uploaded to the ATTiny chip, you should be
able to take it out of the IC socket and use it in your other projects.

_Note_: the ATTiny does not support all of the functionality that the
Arduino boards provide. You must research/experiment to find out what works
and what does not.

# Acknowledgments

* [Arduino KiCad library](https://github.com/Alarm-Siren/arduino-kicad-library)
by Alarm-Siren - Arduino boards schematic symbols and footprints for KiCad
* [ATTinyCore](https://github.com/SpenceKonde/ATTinyCore)
by Spence Konde - suggested Arduino IDE board definitions for ATTiny chips
* [GreatScott's YouTube video on the topic](https://www.youtube.com/watch?v=9LjfkjwMqXI&t=186s) - 
inspiration for this project

