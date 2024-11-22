---
title: Workstations
description: 
published: true
date: 2024-11-07T10:29:14.558Z
tags: 
editor: markdown
dateCreated: 2024-11-07T10:23:57.605Z
---

## Systems
The physical computer exluding peripherals

* Model: N/A if not prebuilt
* CPU: Includes socket, cores, speed
* RAM: Includes speed/stick configuration
* PCIe support: HL/FH = Half Length / Full Height; FL/FH = Full Length / Full Height
* Connectivity: GbE = Gigabit Over Ethernet,  BT = Bluetooth, Wifi

| Asset ID     | Workstation ID            | Model                | CPU                                   | RAM                        | GPU                                           | Motherboard             | PCIe support                                                                                       | Network Connectivity | Display Connectivity                             | HDD                |
|--------------|---------------------------|----------------------|---------------------------------------|----------------------------|-----------------------------------------------|-------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------|--------------------|
| 241122-001   | MIDDLERED                 | N/A                  | Intel Core i5 4440 - 3.1GHz (4 Core)  | 8Gb (2x4Gb) DDR3 1600MHz   | Integrated Graphics Intel(R) HD Graphics 4600 | Lenovo SDK0E50510       | 1xPCIe 3.0 x16 Hl/FH 4xPCIe 2.0 x 1 HL/FH                                                          | GbE only             | 1xVGA, 1xDisplay Port                            | 256Gb SATA III SSD |  
| 241122-002   | BIG RED (DESKTOP-HUP636H) | N/A                  | Intel Core i7 3770 - 3.4GHz (4 Core)  | 8Gb (2x4Gb) DDR3 1333MHz   | AMD Radeon HD 6450 1GB DDR3                   | Asus P8Q77-M2/CDM/SI    | 1xPCIe 3.0 x16 HL/FH 4xPCIe 2.0 x 1 HL/FH                                                          | GbE only             | 2xDVI-D, 1xDVI-I 1xVGA 1xHDMI 1.3a               | 111Gb SATA III SSD |
| 241122-003   | DESKTOP-1MV4JH5           | Dell Optiplex 9020   | Intel Core i7 4790 - 3.6GHz (4 Core)  | 8Gb (2x4Gb) DDR3 1600MHz   | Integrated Graphics Intel(R) HD Graphics 4600 | Dell 00V62H             | 1xPCIe 3.0 x16 HL/FH 4xPCIe 2.0 x1 HL/FH                                                           | 1GbE Only            | 1xVGA, 2xDisplay Port                            | 447Gb SATA III SSD |
| 241122-004   | DESKTOP-11R0KD4           | N/A                  | Intel Core i5 6500 - 3.2Ghz (4 Core)  | 8Gb (2x4Gb) DDR4 2400MHz   | Intel HD Graphics 530                         | Lenovo BC30 U3E1        | 1xPCIe 3.0 x16 HL/FH 1xPCIe 2.0 x4 HL/FH 2xPCIe 2.0 x1 HL/FH                                       | 1GbE + BT            | 1xVGA, 2xDisplay Port                            | 447Gb SATA III SSD |
| 241122-005   | DESKTOP-00X               | Dell Optiplex 9020   | Intel Core i7 4790 - 3.6GHz (4 Core)  | 8Gb (2x4Gb) DDR3 1600MHz   | Integrated Graphics Intel(R) HD Graphics 4600 | Dell 00V62H             | 1xPCIe 3.0 x16 HL/FH 4xPCIe 2.0 x1 HL/FH                                                           | 1GbE Only            | 1xVGA, 2xDisplay Port                            | 447Gb SATA III SSD |
| 241122-006   | DESKTOP-4UEVDCF           | Dell Precition T1650 | Intel Core i7 3770 - 3.4GHz (4 Core)  | 8Gb (4x2Gb) DDR3 1600MHz   | 1023MB NVIDIA Quadro 2000                     | Dell 0X9M3X             | 1xPCIe 3.0 x16 HL/FH 1xPCIe 2.0 x1 HL/FH                                                           | 1GBe Only            | 1xVGA, 2xDisplay Port                            | 256Gb SATA III SSD |
| 241122-007   | ARTIFACTORY-CAD           | N/A                  | Intel Core i7 7700K - 4.2GHz (4 Core) | 32Gb (2x16Gb) DDR4 2133MHz | NVIDIA GeForce GTX 1060 6GB                   | Gigabyte Z270MX-Gaming5 | 1xPCIe 3.0 x 16(16) FL/FH 1xPCIe 3.0 x 16(x8) FL/FH 1xPCIe 3.0 x 16(x4) FL/FH 1xPCIe 3.0 x 1 FL/FH | 1GbE Only            | 4xDisplay Port, 1xHDMI 1.4, 1xHDMI 2.0b, 1xDVI-D | 476Gb M.2 NVMe SSD |

## Workstations

The peripheral setup excluding computer

| Workstation ID           | System asset ID | Location   | KB             | Mouse        | Screens                                                        | Other Peripherals             | Purpose                                                                  |
|--------------------------|-----------------|------------|----------------|--------------|----------------------------------------------------------------|-------------------------------|--------------------------------------------------------------------------|
| MIDDLERED                | 241122-001      | Lasers     | Acer SK-9610   | Logitech M90 | Dell E2417H 1920x1080 (60Hz)                                   | N/A                           | Laser Cutting Interface                                                  |
| BIGRED (DESKTOP-HUP636H) | 241122-002      | Lasers     | HP KU1156      | Dell MOC-5UO | Samsung S24C450 1920x1200 (60Hz)                               | N/A                           | Laser Cutting Interface                                                  |
| DESKTOP-1MV4JH5          | 241122-003      | Design Lab | Dell KB2-12B   | Dell MOC-5UO | 2x Samsung S24C450 1920x1200 (60Hz)                            | N/A                           | Prepare for 3d Print, Labels, CNC, Laser Cutting                         |
| DESKTOP-11R0KD4          | 241122-004      | Design Lab | HP KU0316      | Dell MS111P  | Samsung S24C450 1920x1200 (60Hz)                               | Wacom Cintiq 21UX Pen Display | Design Digital Artwork                                                   |
| DESKTOP-00X              | 241122-005      | Design Lab | Dell Y UK DEL1 | Dell MS111L  | 2x Samsung S24C450 1920x1200 (60Hz)                            | N/A                           | Induction Presentation, Prepare for 3d Print, Labels, CNC, Laser Cutting |
| DESKTOP-4UEVDCF          | 241122-006      | Design Lab | Dell KB212B    | HP M-UAE-96  | 2x Samsung S24C450 1920x1200 (60Hz)                            | N/A                           | Prepare for 3d Print, Labels, CNC, Laser Cutting                         |
| ARTIFACTORY-CAD          | 241122-007      | Design Lab | Dell KB212B    | HP 320M      | Samsung S24C450 1920x1200 (60Hz), Dell U2722D 2048x1152 (60Hz) | N/A                           | 3d Modelling/CAD                                                         |
