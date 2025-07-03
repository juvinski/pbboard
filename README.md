# PocketBeagle 2 DIY Cape for Ardupilot
This project aim enable to run [Ardupilot](https://ardupilot.org/) on the [PocketBeagle 2](https://www.beagleboard.org/boards/pocketbeagle-2) Board.

# Board manufacturing
## PCBWay
I'm using the PCBWay to produce the boards - 5 boards have a cost of USD 5.00
You can use [this file](Board_Archives_Manufacturing/PocketPilot2.kicad_pcb.zip).

## Other Services
I believe the same file can be used by other online PCB manufactures.

# Board Images
## Board Only
![BOARD ONLY](Images/BoardTop.png)

## Board Components - Preview
![BOARD_PARTS](Images/BoardTopComponentes.png)

# Hardware instructions
## Schematic
The schematic can be found [here](Schematic/PocketPilot2.pdf).

## Parts
	- 1 IMU [GY-912](https://www.ebay.com/itm/166809278501)
	- 4 Resistors 1KΩ
	- 3 Led Red, Blue and Green color 
	- 1 BC548 NPN Transistor
	- 1 I2C Digital [Power Module/Monitor](https://ardupilot.org/copter/docs/common-powermodule-landingpage.html#i2c-power-monitor)
	- 6 Pin header 1 x 5 straight
	- 3 Pin header 1 x 4 straight
	- 1 Pin header 1 x 6 straight
	- 6 Pin header 1 x 3 straight or 90°
	- 1 Pin header 1 x 2 straight
	- 1 Pin header female 1 x 8 - optional

## Details
To reduce the board size the Power Monitoring need to be digital - I'm using the [Holybro PM2D](https://holybro.com/products/pm02d-power-module?srsltid=AfmBOoraJGVR_kFEiSwKRgzMLQZ1dEZXMhWgGvN6DEnkXQVvNgj2pTN2).
The outputs of the sensor was changed by a female reader and both 5Volts output connectec together as the GND.
The GY-912 is soldered direct over the board once the PocketBeagle 2 is over it and the space between the PocketBeagle 2 board and the DIY board it's small.
Once the Kicad project is shared, you can modify freely according your needs.
The CAN interface need a CAN Transceiver breadboard like CJMCU-1051 (or any TJA1051) with 3.3Volts interface for TX and RX.
The buzzer circuit is simple but powerfull.
For the USB OTG you are free to use what kind of USB is more suitable for you. The board export 5 pins there the 4th is not connected.

## Board details
	- 4 UARTs - One have the I2C to be used with a GPS + Compass
 	- 2 I2Cs - One is under the Power header
  	- 4 GPIO pins with GND
   	- 6 Outputs
   	- Buzzer output for an Active buzzer
*** All pins is just 3.3 Volts ***
*** 5 Volts will brick your PocketBeagle 2 ***

# Software Instructions
The software instructions will be published soon.
