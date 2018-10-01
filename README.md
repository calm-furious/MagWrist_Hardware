# MagWrist_Hardware

## About MagWrist
This is a project created by **QINGHAO LIU**.
The basic idea is that:

The program of the system has two parts: Hardware(Embedded Board) and Software(PC).

This README _Only_ talks about **HARDWARE** part.

## Install Keil(TI Cortex-M4 Development Environment)

Due to the problem of copyright. Ask your professor for the installation program, which may contains 5 files.

Installation program name | Details
------------------------- | -------
MDK522.EXE | The main setup file of Keil 5.22
MDKCM522.EXE | The setup file for Keil legacy devices
Keil.TM4C_DFP.1.1.0.pack | Tiva C Series device support and examples
SW-EK-TM4C1294XL-2.1.4.178.exe | Firmware development package setup
uniflash_sl.4.1.1250.exe | Uniflash setup(Maybe no use)

## About TI Cortex-M4 Embedded Board

(Picture here)

(The head files and functions defined outside of **MagWrist_ReadData.c** is provided by Prof. Wei Liu _SJTU_.)

The pins on the front side is enough(**Boosterpack 1 and 2** written in white).

xxxx | Debug port | xxxx | xxxx | xxxx    
---- | ---------- | ---- | ---- | ----
3.3V | 5V |  | PF1 | GND
PE4 | GND |  | PF2 | PM3
PC4 | PE0 |  | PF3 | PH2
PC5 | PE1 |  | PG0(I2C1 SCL) | PH3
PC6 | PE2 |  | PL4 | ~RST 
PE5 | PE3 |  | PL5 | PD1(I2C7' SDA)
PD3(I2C8' SDA) | PD7 |  | PL0(I2C2' SDA) | PD0(I2C7' SCL)
PC7 | PA6(I2C6 SCL) |  | PL1(I2C2' SCL) | PN2
PB2(I2C0 SCL) | PM4 |  | PL2 | PN3
PB3(I2C0 SDA) | PM5 |  | PL3 | PP2
 ~ | ~ | ~ | ~ | ~
3.3V | 5V |  | PG1(I2C1 SDA) | GND
PD2(I2C8' SCL) | GND |  | PK4(I2C3 SCL) | PM7
PP0 | PB4(I2C5 SCL) |  | PK5(I2C3 SDA) | PP5
PP1 | PB5(I2C5 SDA) |  | PM0 | PA7(I2C6 SDA)
JP4(PD4/PA0(I2C9 SCL)) | PK0 |  | PM1 | ~RESET
JP5(PD5/PA1(I2C9 SDA)) | PK1 |  | PM2 | PQ2/PA3(I2C8 SCL)
PQ0 | PK2 |  | PH0 | PQ3/PA2(I2C8 SDA)
PP4 | PK3 |  | PH1 | PP3
PN5(I2C2 SCL) | PA4(I2C7 SCL) |  | PK6(I2C4 SCL) | PQ1
PN4(I2C2 SDA) | PA5(I2C7 SDA) |  | PK7(I2C4 SDA) | PM6

## About magnetometer HMC5983

(Photo here)
(Data sheet)


## About motion sensor  MPU9250

(Photo here)
(Data sheet)

## Magnetometer Array

(Photo here)
(Support by Prof. Hao He _SJTU_.)

## System Architecture

(Figure Here)

## Test the hardware program

1. Download this repository to your PC.
2. Find the **MagWrist_ReadData.uvprojx** file and open it with Keil.
(picture here about the postion of the src file)
3. Double click the **MagWrist_ReadData.c** file on the left side.
4. Configuration.
   1. (Read Data Rate)
   2. (Measurement Scale)
5. Click on the **Rebuild** button on the up-left side.
   1. If **0 Error(s)**, then _Congratulations!_(Ignore the warnings)
   2. If there is any error, try debug it by yourself first.
      1. Check whether there is any syntax error.(Maybe you tapped your keyboard by mistake)
      2. Right click **Target1** on the left side and choose **Options for Target 'Target 1'**.
      3. Click **Device** and check you have chosen **TM4C1294NCPDT**.
      4. Click **C/C++** and check **Include Paths**  is `.\inc;.\driverlib_`.
   3. If you have no idea, ask your professor.
6. Ready to download the program to your embedded board.
      

