The MAX14900 device and MAX31912 uses SPI1 module on the W5100S-EVB-Pico board as the W5100S uses SPI0. Here are some traces of the SPI module 1 
lines when polling the device from OpenPLC software. 
The captures are made when using the Arduino firmware  https://github.com/mhanuel26/Wiznet-PoE-Rudge-PLC-Firmware
and the OpenPLC implementation https://www.openplcproject.com/

Figure 1 shows the two SPI transactions, first is for comms with MAX14900 (using chip select signal O_CS), second is MAX31912 (using chip select signal I_CS)
![readout_spi_plc_1](https://user-images.githubusercontent.com/2257779/166002119-2a237120-35ca-49f4-a737-b76ecd669224.png)

Figure 2 shows consecutive readings as per the internal loop in Arduino code and the two Ethernet requests.
![readout_spi_plc_2](https://user-images.githubusercontent.com/2257779/166002742-86a22417-e1f2-48f9-868a-4a54e7ebfcab.png)

Figure 3 shows the 100ms polling time between SPI bursts, this 100ms time is configured under OpenPLC software as shown in Picture 4. 
![readout_spi_plc_3](https://user-images.githubusercontent.com/2257779/166002941-1bea873a-60bb-4fd4-be73-1d1d543139f0.png)


