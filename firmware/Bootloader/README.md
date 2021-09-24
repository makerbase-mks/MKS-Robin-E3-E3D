# Bootloader description
This hex file works for MKS Robin E3 or E3D motherboard

# How-to-upload-it-to-board
- Use upload tool, ST-LINK or J-LINK
- Connect to board's SWD interface
  ```
             MKS Robin E3/E3D                 
         ___________________________                 
      2 | 3.3V       GND        GND | 6      
      1 | PA13(DIO)  PA14(CLK)  RST | 5      
         ---------------------------  
  ```
- Programming(Use J-LINK)
  - Download JFLASH
  - Run JFlash.exe
  - Open project settings file: File->Open project
  - Open bootloader file: File->Open data file
  - Run: Target-connect, Target-Auto and wait upload bootloader hex file
  
- Programming(Use ST-LINK)
  - Download STM32 ST-LINK Utility v4.6.0：https://github.com/makerbase-mks/MKS-Robin-Nano-V1.X/blob/master/Tool/en.stsw-link004_v4.6.0.zip
  - Install and run: STM32 ST-LINK Utility
  - Open bootloader: File -> Open file
  - ST-LINK -> printf via SWO viewer - Start
  - Target -> Erase chip
  - Target -> Program -> Start
