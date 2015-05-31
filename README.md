# μLRS
μLRS - micro LRS receiver, OpenLRSng compatible<br/>
RCGroups thread: http://www.rcgroups.com/forums/showthread.php?t=2371835

## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.


## General
μLRS boards are hardware compatible with OpenLRSng firmware for HW 8 (micro RX). Common features for μLRS boards are:
* input voltage 4-16V (max 3S lipo, 4S is too much voltage)
* PCB pads for 3.3v UART interface (RX, TX, DTR, GND) - do **NOT** try to use it with 5v uart interface
* analog RSSI output pad
* U.FL antenna connector
* RFM22b 100mW radio module
* LFCN-490 low pass filter (can be easily removed by replacing it with 1206 0R resistor)
* LC filter for radio power supply
* Atmega328P-MU microcontroller (QFN case)
* 0603 sized components - can be soldered at home (only atmega chip requires strong soldering skills)

## v2 board
Improved version of μLRS v1 with following changes:
* vias covered by soldermask (v1 has these with copper epxosed)
* removed I2C pads
* removed 3.3v pad
* removed resistors in TX/RX pads
* removed dedicated RESET pad (but still easily accessible at the most bottom-right capacitor pad)
* smaller board - 16x16mm (0.63" x 0.63"), exactly the same size as RFM22b module
* PCBs can be ordered here: https://oshpark.com/shared_projects/H6KfYEk2

<img src="http://i.imgur.com/lzrO92k.png" style="border-width: 0"/>

## v2 BOM
* 4x 1k 0603 resistor
* 1x 10k 0603 resistor
* 2x 22p 0603 capacitor
* 4x 100nF 0603 capacitor
* 2x 1uF 0603 capacitor (on schema one is 0402, but 0603 fits perfectly and is easier to solder)
* 2x 10uF/6.3v 0603 tantalum capacitor
* 1x 47uF/16v SMD B tantalum capacitor (schema is for SMD A, but 16v SMD A cannot be found, you can use SMD-A 6.3v but then you are limited to 5v power supply)
* 1x SOT-323 Schottky diode (let it be around 200mA), for example BAT165
* 1x green 0603 led
* 1x red 0603 led
* 1x LFCN-490 filter
* 1x mcp1703cb SOT23 voltage regulator (supports max 16V)
* 1x 16MHz crystal oscillator 3525 case
* 1x 10uH 1210 inductor
* 1x Atmega328P-MU (MLF32 case) microcontroller
* 1x RFM22B-433-S2 radio module
* 1x U.FL antenna connector

## v1 board (deprecated)
μLRS v1 is a first prototype board:
* PCB dimensions: 20x18mm
* I2C interface (SDA, SCL) pads
* 3.3v pad
* RESET pad (for SPI programming)
* big 47uF tantalum capacitor for input voltage filtering
* two 10uF tantalum capacitors (one for 3.3v filtering, another one for RSSI analog output)
* can be used also as a **transmitter**
* PCBs can be ordered here: https://oshpark.com/shared_projects/nFa7UehY

<img src="http://i.imgur.com/7CtICCr.png" style="border-width: 0"/>


