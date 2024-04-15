# Micro Invaders - Hardware
This repository contains the hardware-related files of Robot Uprising Micro Invaders. The folder structure is as follows
* Root: Contains 3D printable basic robot parts
	* Accessories: Contains 3D printable accessories designed by Robot Uprising
	* Advanced: Contains design files
	* Images: Contains images mainly for README files
	* Misc: Contains miscellaneous 3D printable files related to the design, but not needed for the competition

The Micro Invaders robot is designed with simplicity in mind. It has very little amount of mechanical parts, and all the parts are 3D-printable. Moreover, it is designed to be assembled or disassembled without using any tools. 

If you need a 3D-printing guide, here is our guide: [3D-Printing Guide - Ultimaker 3](https://docs.google.com/document/d/1BAfrNYozn9PcpJIatZrwz-if5QTi_UQTAYi0SMTYilM/).

## Robot Parts
![Robot Parts Explanation](https://raw.githubusercontent.com/robot-uprising-hq/ai-robot-hardware/master/Images/Robot%20Parts%20Explanation.png)

**Drive wheel:** This part drives the track, and the robot hence the name "drive wheel". The clearances are adjusted so that it fits nicely on the motor shaft, but it features a screw hole in case it doesn't.

**Idler:** This is the non-driving wheel for the tracks, but it also doubles as a tensioner. Thanks to its eccentric shaft, it can be used to adjust the slack on the chain.

**Idler retainer:** Idler retainer retains the idler :)

**Body:** This is the chassis of the robot. It houses all the parts. There are two versions of body. One is accessorizable and the other one is plain (located in Misc folder). As the name implies, accessorizable body is designed to fit accessories utilizing standard accessory connector.

**Top cover:** This part basically prevents things from falling off. It keeps the batteries in place, it prevents circuit board to fall off, and it even acts as the idler retainer retainer. All these functions in one single part. It attaches to the body by one rigid attachment point in the back, and one flexible attachment point in the front. This part also has two versions, accessorizable and plain (located in Misc folder).

**Track:** This is the part that moves the robot. It is basically a chain with 20 links.

## Printing Checklist
You will need to print the following parts for the competition. 
* 1 x Body (accessorizable)
* 1 x Top cover (accessorizable)
* 1 x Aruco marker holder
* 2 x Drive wheel
* 2 x Idler retainer
* 2 x Track
* 2 x Idler

You can design and print your own front accessory as long as it complies with the [rules](https://github.com/robot-uprising-hq/ai-rules-mi2020).

We recommend printing the parts in the given order as the latter parts are more advanced, and you might benefit from the experience. 
 
Also, feel free to design and print your own super exotic accessories or custom robot bodies for showing off between the matches, although you might not be allowed to use them in the competition. 

## PCB Gerber files and Bill of Materials

You can find Gerber files for the PCB in the folder "Gerber Files". You can upload the compressed file to a PCB manufacturers website (e.g. JLCPCB)

Here's a Bill of materials and links to Digikey parts:
* 1 x https://www.digikey.fi/en/products/detail/jst-sales-america-inc/S3B-XH-A/1651048
* 2 x https://www.digikey.fi/en/products/detail/jst-sales-america-inc/S2B-XH-A/1651055
* 1 x https://www.digikey.fi/en/products/detail/stmicroelectronics/L293D/634700
* 1 x https://www.digikey.fi/en/products/detail/bel-fuse-inc/0ZCF0250FF2C/4156185
* 1 x https://www.digikey.fi/en/products/detail/onsemi/MC7805CD2TR4G/919332
* 2 x https://www.digikey.fi/en/products/detail/panasonic-electronic-components/ECA-1EM101B/268461
* 1 x https://www.digikey.fi/en/products/detail/c-k/OS102011MA1QN1/1981430
* 4 x https://www.digikey.fi/en/products/detail/liteon/LTST-C171KRKT/386801
* 4 x https://www.digikey.fi/en/products/detail/stackpole-electronics-inc/RMCF0805FT330R/1760484
* 1 x https://www.digikey.fi/en/products/detail/stackpole-electronics-inc/RMCF0805JT1K00/1757881
* 1 x https://www.digikey.fi/en/products/detail/stackpole-electronics-inc/RMCF0805JT2K20/1757894



