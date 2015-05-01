# μLRS
μLRS - micro LRS receiver, OpenLRSng compatible

## License
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.


## General
μLRS boards are hardware compatible with OpenLRSng firmware for HW 8 (micro RX). Common features for μLRS boards are:
* input voltage 4-16V
* PCB pads for 3.3v UART interface (RX, TX, DTR, GND)
* analog RSSI output pad
* U.FL antenna connector
* RFM22b 100mW radio module
* LFCN-490 low pass filter
* LC filter for radio power supply

## v1 board (prototype)
μLRS v1 is a first prototype board:
* PCB dimensions: 20x18mm
* I2C interface (SDA, SCL) pads
* 3.3v pad
* RESET pad (for SPI programming)
<img src="http://i.imgur.com/7CtICCr.png" style="border-width: 0"/>


## v2 board
This board is not published yet. It will be an improved version of v1 with following changes:
* vias covered by soldermask (v1 has these with copper epxosed)
* removed I2C pads
* removed 3.3v pad
* removed resistors in TX/RX pads
* removed dedicated RESET pad (but still easily accessible)
* a bit smaller board
