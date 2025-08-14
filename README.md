# Power-World-Quiet-Pro
Modbus integration of an Power World Quiet Pro

<img width="366" height="245" alt="Screenshot 2025-08-13 at 12-41-26 China Custom Kunststoff Inverter Pool Wärmepumpe Hersteller Fabrik" src="https://github.com/user-attachments/assets/83c1b540-9da1-4b5c-aa9e-6b49cb65af7e" />

Models
PW040KZXYCH 	PW050KZXYCH 	PW060KZXYCH 	PW080KZXYCH

This Heat Pump is also sold as with diferent Brand names 
Twister Pooltech
SPA Lagert.dk
Kensol


The Board inside is the CC1010B
![PXL_20250814_045921613](https://github.com/user-attachments/assets/36b17ad8-fecf-4e22-a6b8-a81159adb6e6)

The wiring of the board
![PXL_20250814_045906760](https://github.com/user-attachments/assets/2754d63a-2180-4454-8ab8-223f4135b618)

The port I used as there is more than one with the yellow circle on the board labeled CN8
![PXL_20250814_045930297](https://github.com/user-attachments/assets/3786c158-1986-45d8-9f0f-a261858e1eec)

The connector which fits is a PH XH RM 2,54 mm 4 pin
![PXL_20250814_051158750](https://github.com/user-attachments/assets/fb79a904-2aaf-4d1f-b7e3-332407708520)

my setup with an ESP32, a MAX485Converter and a stepdown converter to generate the 5V needed for ESP32 and the the RS485 board
![PXL_20250814_051646964](https://github.com/user-attachments/assets/42222671-c224-4219-a373-93582a9fa9d1)

the wiring will follow

I used on the ESP pin 16, 17 and 4 for the modbus/serial communication

The only registers wich seems toe be accessable are the holding regsiters (0x30 Mode in Modbus)
Currently for teating and finding out the meaning of the registers i read register 40000 to 40300 in batches of 50.
The frequency is every 7 aeconds all register are updated in the ESP
For writing use 0x60 with same register range.
The registers wich I already use and know what is inside are documented in the Excel.
