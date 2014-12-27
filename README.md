EM7180_SENtral_sensor_hub
=========================

There are two files in this repository. 

The FirmwareUpload.ino file is a sketch that takes the firmware file xxx.fw (~22 kbyte) generated by the EM7180 SENtral Tool Kit Configuration tool and writes it to an ST Microelectronics M24512DFM EEPROM from an SD card. Both the SD card and the SENtral breakout board need to be connected to a micrcontroller; I use the Teensy 3.1. The SENtral breakout board is connected to the the I2C port on pins 16 and 17 and the SD card reader is connected to the SPI port. Once the firmware is loaded onto the EEPROM it doesn't have to e done again unless the firmware changes or is updated. 

The other file is a the sketch that configures the SENtral for either normal mode, where is manages the BMX055 sensors as slaves providing scaled sensor output and quaternions,  or pass-through mode, where the Teensy micrcontroller can directly communicate with the BMX055 motion sensor and the MS5637 pressure sensor.

This project is a work in progress and will be updated...
