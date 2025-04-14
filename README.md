# Micro Invaders - Hardware

This repository contains the hardware-related files of Robot Uprising Micro Invaders. The folder structure is as follows
* Root: Contains 3D printable basic robot parts
	* Accessories: Contains 3D printable accessories designed by Robot Uprising
	* Advanced: Contains design files
	* Images: Contains images mainly for README files
	* Misc: Contains miscellaneous 3D printable files related to the design, but not needed for the competition

The Micro Invaders robot is designed with simplicity in mind. It has very little amount of mechanical parts, and all the parts are 3D-printable. Moreover, it is designed to be assembled or disassembled without using any tools. 

If you need a 3D-printing guide, here is our guide: [3D-Printing Guide - Ultimaker 3](https://docs.google.com/document/d/1BAfrNYozn9PcpJIatZrwz-if5QTi_UQTAYi0SMTYilM/).

## Table of Contents <!-- omit in toc -->

- [Micro Invaders - Hardware](#micro-invaders---hardware)
	- [Mechanical parts](#mechanical-parts)
		- [Printing Checklist](#printing-checklist)
		- [Accesories](#accesories)
	- [Electronics](#electronics)
		- [Driver PCBA](#driver-pcba)
			- [PCB Gerber files and Bill of Materials](#pcb-gerber-files-and-bill-of-materials)
			- [PCBA Bill of Materials](#pcba-bill-of-materials)
		- [ESP32](#esp32)
		- [Motors](#motors)
		- [Batteries](#batteries)
		- [Cables and connectors](#cables-and-connectors)

## Mechanical parts

![Robot Parts Explanation](https://raw.githubusercontent.com/robot-uprising-hq/ai-robot-hardware/master/Images/Robot%20Parts%20Explanation.png)

**Drive wheel:** This part drives the track, and the robot hence the name "drive wheel". The clearances are adjusted so that it fits nicely on the motor shaft, but it features a screw hole in case it doesn't.

**Idler:** This is the non-driving wheel for the tracks, but it also doubles as a tensioner. Thanks to its eccentric shaft, it can be used to adjust the slack on the chain.

**Idler retainer:** Idler retainer retains the idler :)

**Body:** This is the chassis of the robot. It houses all the parts. There are two versions of body. One is accessorizable and the other one is plain (located in Misc folder). As the name implies, accessorizable body is designed to fit accessories utilizing standard accessory connector.

**Top cover:** This part basically prevents things from falling off. It keeps the batteries in place, it prevents circuit board to fall off, and it even acts as the idler retainer retainer. All these functions in one single part. It attaches to the body by one rigid attachment point in the back, and one flexible attachment point in the front. This part also has two versions, accessorizable and plain (located in Misc folder).

**Track:** This is the part that moves the robot. It is basically a chain with 20 links.

### Printing Checklist

You will need to print the following parts for the competition.

| Amount | Part                       |
| :----: | -------------------------- |
|   1    | Body (accessorizable)      |
|   1    | Top cover (accessorizable) |
|   1    | Aruco marker holder        |
|   2    | Drive wheel                |
|   2    | Idler retainer             |
|   2    | Track                      |
|   2    | Idler                      |

See folders `./Mechanics/Robot/STL` and `./Mechanics/Accessories/STL` for the STL-files for printing.

We recommend printing the parts in the given order as the latter parts are more advanced, and you might benefit from the experience. 
 
Also, feel free to design and print your own super exotic accessories or custom robot bodies for showing off between the matches, although you might not be allowed to use them in the competition. 

### Accesories

You can design and print your own front accessory as long as it complies with the [rules](https://github.com/robot-uprising-hq/ai-rules-mi2020).

## Electronics

### Driver PCBA

#### PCB Gerber files and Bill of Materials

You can find Gerber files for the PCB in the folder "Gerber Files". You can upload the compressed file to a PCB manufacturers website (e.g. JLCPCB)

#### PCBA Bill of Materials

ID matches the schema and the PCB silkscreen

|         ID         | Description with link                                                                                                                                                                                              | Amount |
| :----------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :----: |
|       C1, C2       | [25V 100uF electrolytic THT capacitor](https://www.digikey.fi/en/products/detail/panasonic-electronic-components/ECA-1EM101B/268461)                                                                               |   2    |
|   D1, D2, D3, D4   | [RED clear 0805 SMD LED](https://www.digikey.fi/en/products/detail/liteon/LTST-C171KRKT/386801)                                                                                                                    |   4    |
|         F1         | [2.5A (Max Hold Current), 5A (Trip Current) 16V Fuse 2920 (7351 metric) package](https://www.digikey.fi/en/products/detail/bel-fuse-inc/0ZCF0250FF2C/4156185)                                                      |   1    |
|         J1         | [3-pin JST XH 2.50mm pitch connector](https://www.digikey.fi/en/products/detail/jst-sales-america-inc/S3B-XH-A/1651048)                                                                                            |   1    |
|       J2, J3       | [2-pin JST PH 2.00mm pitch connector](https://www.digikey.fi/fi/products/detail/jst-sales-america-inc/S2B-PH-SM4-TB/926655?s=N4IgTCBcDaIMpgEIFoAKAJZcCyAWZAKoiALoC%2BQA)                                           |   2    |
| R1, R2, R3, R4, R6 | [1 kΩ 0805 SMD resistor](https://www.digikey.fi/en/products/detail/stackpole-electronics-inc/RMCF0805JT1K00/1757881)                                                                                               |   5    |
|         R5         | [2.2 kΩ 0805 SMD resistor](https://www.digikey.fi/en/products/detail/stackpole-electronics-inc/RMCF0805JT2K20/1757894)                                                                                             |   1    |
|        SW1         | [Slide switch](https://www.digikey.fi/en/products/detail/c-k/OS102011MA1QN1/1981430)                                                                                                                               |   1    |
|         U1         | [7805 5V linear regulator (D2PAK Package)](https://www.digikey.fi/en/products/detail/onsemi/MC7805CD2TR4G/919332)                                                                                                  |   1    |
|    U2 (J4, J5)     | [For ESP-32 two 20-pin 2.54mm pitch female headers which needs to be trimmed to 19 pins](https://www.digikey.fi/fi/products/detail/w%C3%BCrth-elektronik/61302011821/16608603?s=N4IgTCBcDaIGwEYDMAGMKEIBxgSAugL5A) |   2    |
|         U3         | [Dual H-bridge motor driver 293D](https://www.digikey.fi/en/products/detail/stmicroelectronics/L293D/634700)                                                                                                       |   1    |

### ESP32

ESP32-DEVKITC-32E:

- 1 x https://www.digikey.fi/en/products/detail/espressif-systems/ESP32-DEVKITC-32E/12091810

### Motors

Olimex LTD: MG-6-48

- 2 x https://www.digikey.fi/en/products/detail/olimex-ltd/MG-6-48/21662315

### Batteries

Two 18650 Li-Ion batteries (we recommend >2200mAh, with protection circuit):

- 2 x https://akkula.fi/tuote/xtar-18650-li-ion-akku-2600-mah-36v-suojapiiri-button-top/

Li-Ion 18650 battery charger:

- 1 x https://akkula.fi/tuote/xtar-mc2-plus-usb-pikalaturi-kahdelle-li-ion-akulle/

18650 battery holder for two batteries:

- 1 x https://akkula.fi/tuote/2-x-18650-asennuskotelo-johdoilla-max-1-a-virta/

### Cables and connectors

We recommend getting JST XH (2.50mm pitch) and PH (2.00mm pitch) connector assortment with crimp tool.
The JST connectors require crimping the cable ends with a tool such as https://www.partco.fi/fi/tyoekalut/puristuspihdit/loput-puristuspihdit/11353-ht213.html. 
Unless you're very much into crimping all the things, instead of buying the tool you can probably find one at your local university electronics lab, makerspace or https://hacklab.fi.

There are also preassembed wires: (we recommend 12" ones so that they are long enough)

XH:
https://www.digikey.fi/en/products/filter/jumper-wires-pre-crimped-leads/453?s=N4IgTCBcDaIFYGcAuACAHgCxAXQL5A

12" ones:
https://www.digikey.fi/en/products/detail/jst-sales-america-inc/ASXHSXH22K305/6684932

PH:
https://www.digikey.fi/en/products/filter/jumper-wires-pre-crimped-leads/453?s=N4IgTCBcDaIFYGcAuACADgCxAXQL5A

12" ones:
https://www.digikey.fi/en/products/detail/jst-sales-america-inc/ASPHSPH24K305/6009459


3-pin JST XH 2.50mm pitch Connector for battery terminal:
- Female 1 x https://www.digikey.fi/fi/products/detail/jst-sales-america-inc/XHP-2/555485

2-pin JST PH 2.00mm pitch Connector for motor terminals:
- Female 2 x https://www.digikey.fi/en/products/detail/jst-sales-america-inc/PHR-2/608607

