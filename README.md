# Physalis_Kenji_X1_version_5.8
Kenji-X1 Tele-Presence UGV Platform Firmware Source Code
/*****************************************************************************************************************************
* ------------------------------------------------- =( Physalis Labs. )= --------------------------------------------------- *
* ---------------------------- =( Kenji-X1 Tele-Presence UGV Platform Firmware Source Code )= ------------------------------ *
* -------------------------------------------------------------------------------------------------------------------------- *
* --------------------------------------------- =( Firmware Version 5.7B )= ------------------------------------------------ *
* ----------------------------- =( Automated UGV for Tele-Presence and Remote Operations )= -------------------------------- *
* -------------------------------------------------------------------------------------------------------------------------- *
* -------------------------------------------------------------------------------------------------------------------------- *
* ---- [ Electronic Systems and Hardware Technical Specifications ] -------------------------------------------------------- *
* -------------------------------------------------------------------------------------------------------------------------- *
* [MCU/ Micro-Controller]: Atmel ATmega-1284p picoPower AVR 8-Bit RISC Architecture CPU Frequency = 20 MHz                   *
* [Drivetrain / Power Unit]: Dedicated H-Bridges with Dual (25 mm) Geared DC Motors, Reduction Factor 1:150                  *
* [Drivetrain / Stall Current]: 4500 mA                                                                                      *
* [Drivetrain / Stall Torque]: 9.5 kg NaN                                                                                    *
* [Drivetrain / Rated Current]: 1200 mA                                                                                      *
* [Drivetrain / Noise]: 56 dB                                                                                                *
* [Drivetrain / Working Voltage]: 9 Volt DC                                                                                  *
* [Drivetrain Tower/MastCam ]: Stepper-Online 1.8-Angle 200 Steps, 2-Phase (12V, 500mA), Stepping Motor on Planetary Gearbox *
* [Photocells]: Advanced Photonix/NSL-5910, PHOTOCELL, CDS TO-8 Hermetic, Photo-Conductive Cells (Cadmium-Sulfide)           *
* [Vibration Detection Unit]: Murata Electronics/7BB-27-4CL0, Vibration Measurement Probe on Piezo-Electric Sensor           *
* [Infrared Proximity Sensor]: Sharp GP2Y0A02YK0F (20 - 150 cm op. range), (PSD + IRED), Analog                              *
* [Speaker]: Visaton, 5V, DC, Impedance = 8 Ohm, (System Alarms and Sounds)                                                  *
* [Bar-Graph]: Broadcom Limited/HDSP-483210, Green-Yellow-Red, 10-Seg., (Indications of Various System States)               *
* [Lights]: Cree High-Power LED, on Convoy Driver PCB, TIR Lens, Warm White                                                  *
* [WLAN Module]: SBC (RaspberryPi B+/Zero-W), Wireless Communication Unit and Remote-Control Functionality                   *
* [Battery Unit]: Panasonic NCR18650B 3.7 v 3400 mAh, Li-Polymer Cells Assembled 3 x 3.7V 3500mA = 12.700V                   *
* [EEPROM]: Microchip 256 kByte EEPROM, non-Volatile Memory and System Critical Data Storage                                 *
* [LIDAR]: Garmin LIDAR-Lite v3HP, Update_rate >= 1KHz, Res = 1cm, Accur = -/+2.5cm, IPX7-Rated, Range = 5cm-40m             *
* [FRAM]: Cypress Semiconductor FM25V20A-G-ND, 2-Mbit Ferroelectric RAM (automotive), non-Volatile Memory, and Data Storage  *
* [GPIO-I2C-Expander]: NXP/PCF8575TS, 16-Bit GPIO Expander on I2C BUS, adds 16 GPIOs to ATmega-1284p MCU                     *
* [Display]: 16 x 2 Character Display on Motorola HD44780 1602 LCD Driver IC, on I2C BUS (Color = Blue/White)                *
* [PWM Controller]: NXP/PCA9685PW, 16-GPIO, Res=12-Bit, PWM-Controller,I2C-BUS,Controls Mecha-Arms Servo Drives              *
* [Digial Temperature Sensor]: NXP/LM75ADP-118, Temperature Sensor, Res=0.125°C, I2C-BUS, Sigma-Delta A-D Conv.              *
* [Mecha-Arms]: DSSERVO (RDS5160,3216,3115MG), High-Torque, Servo-Motors (Left/Right)]: 7 x Servos per Arm and 2 x Claws     *
* [USB-to-UART Bridge]: Cypress Semiconductor CY7C65213-28PVXIT, USB 2.0 Full-Speed controller, and a UART-Transceiver       *
* -------------------------------------------------------------------------------------------------------------------------- *
* [Source File]: "main.c" Running all Input/Output Operations of [ATmega-1284p] MCU ---------------------------------------- *
* -------------------------------------------------------------------------------------------------------------------------- *
* -------------------------------------------------------------------------------------------------------------------------- *
* [written by]:Dr.-Ing. Zohrabyan David, Physalis Labs. [Potsdam 26.10.2022], Hans-Marchwitza-Ring.21, 14473 --------------- *
