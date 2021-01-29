
# OpenLANE-Sky130 Physical-Design-Workshop

This repository contains the RTL to GDSII flow implemention using the open-source tool OpenLANE and open-source Sky130 PDK provided by Skywater.

![](Images/eadvanced_physical_design.png)

# Table of Contents
- [About](#About)
- [RTL-GDSII Flow](#RTL-GDSII Flow)
- [Day-1 Opensource EDA, OpenLANE, Skywater130 PDK](#Day-1 Opensource EDA, OpenLANE, Skywater130 PDK)
	- [Skywater PDK Files](#Skywater PDK Files)
 	- [Invoking OpenLANE](#Invoking OpenLANE)
 	- [Package Importing](#Package Importing)
 	- [Design Folder](#tips-for-ip-design-using-sky130-technology)
 	- [Design Folder Hierarchy](#Design Folder Hierarchy) 
	- [Configuration Files](#Configuration Files)
	- [Prepare Design](#Prepare Design)
 	- [Synthesis](#Synthesis)
- [Day-2 Floorplanning and Standard Cells](#Day-2 Floorplanning and Standard Cells)
	- [Aspect Ratio and Utilization Factor](#Aspect Ratio and Utilization Factor)
 	- [Preplaced Cells](#Preplaced Cells)
 	- [Decouping Capacitors](#Decouping Capacitors)
  - [Power Planning](#Power Planning)
  - [Pin Placement](#Pin Placement)
  - [Floorplanning with OpenLANE](#Floorplanning with OpenLANE)
  - [Viewing Floorplan in Magic](#Viewing Floorplan in Magic)
 	- [Placement](#Placement)
  - [Viewing Placement in Magic](#Viewing Placement in Magic)
 	- [Standard Cell Design Flow](#Standard Cell Design Flow)
  - [Standard Cell Characterization](#Standard Cell Characterization)
  
- [Day 3 - Design Library Cell](#Day 3 - Design Library Cell)
 	- [Spice Simulations](#Spice Simulations)
  - [Switching Threshold of a CMOS Inverter](#Switching Threshold of a CMOS Inverter)
  - [16 Mask CMOS Process Steps](#16 Mask CMOS Process Steps)
  - [Magic Layout View of Inverter Standard Cell](#Magic Layout View of Inverter Standard Cell)
  - [Magic Key Features](#Magic Key Features)
  - [Device Inference](#Device Inference)
  - [DRC Errors](#DRC Errors)
  - [PEX Extraction with Magic](#PEX Extraction with Magic)
  - [Spice Wrapper for Simulation](#Spice Wrapper for Simulation)
- [Day-4 Layout Timing Analysis and CTS](#Day-4 Layout Timing Analysis and CTS)
  - [An Introduciton to LEF Files](#An Introduciton to LEF Files)
  - [LEF Generation in Magic](#LEF Generation in Magic)
  - [Including Custom Cells in OpenLANE](#Including Custom Cells in OpenLANE)
  - [Fixing Slack Violations](#Fixing Slack Violations)
  - [Clock Tree Synthesis](#SyntheClock Tree Synthesissis)
  - [Viewing Post-CTS Netlist](#Viewing Post-CTS Netlist)
  - [Post-CTS STA Analysis](#Post-CTS STA Analysis)
- [Day 5 Final Steps in RTL to GDSII](#Day 5 Final Steps in RTL to GDSII)    
  - [ Power Distribution Network Generation](# Power Distribution Network Generation)
  - [Global and Detailed Routing](#Global and Detailed Routing)
  - [SPEF Extraction](#SPEF Extraction)
- [Acknowledgement](#acknowledgement)
- [Contact Information](#contact-information)

![](Images/openlane_flow.png)

![](Images/day1_1.png)

![](Images/day1_2.png)

![](Images/day1_3.png)

![](Images/day1_4.png)

![](Images/day1_5.png)

![](Images/day1_6.PNG)

![](Images/day1_7.png)

![](Images/day1_8.png)

![](Images/day1_9.png)

![](Images/day1_10.png)

![](Images/day2_1.PNG)

![](Images/day2_5.png)

![](Images/day2_6.png)

![](Images/day2_7.png)

![](Images/day2_8.png)

![](Images/day2_9.png)

![](Images/day2_10.png)

![](Images/day3_1.PNG)

![](Images/day3_2.PNG)

![](Images/day3_3.PNG)

![](Images/day3_4.PNG)

![](Images/day3_5.PNG)

![](Images/day3_6.PNG)

![](Images/day3_7.PNG)

![](Images/day3_8.PNG)

![](Images/day3_9.PNG)

![](Images/day3_10.PNG)

![](Images/day3_11.PNG)

![](Images/day3_12.PNG)

![](Images/day3_12.PNG)

![](Images/day3_13.PNG)

![](Images/day3_14.PNG)

![](Images/day3_15.PNG)

![](day4_10INVCELL.PNG)

![](day4_11Expanded.PNG)

![](day4_12prestacxonf.PNG)

![](day4_13 fanout setting.PNG)

![](day4_14afterfanout slack.PNG)

![](day4_15the buffer was replaces.PNG)

![](day4_16after changing buffers.PNG)

![](day4_17after running again the floorplan and placement now cts.PNG)

![](day4_18new cts file after running cts.PNG)

![](day4_19 openroad inoke timing analysis.PNG)

![](day4_1tracks_info.PNG)

![](day4_20read lef and def file and then writing the db file.PNG)

![](day4_21after thatverilog file and other files were read.PNG)

![](day4_22 clocks and checks.PNG)

![](day4_23 post cts slack.PNG)

![](day4_2after grid command.PNG)

![](day4_3this shows that the input output are on intersection of tracks.PNG)

![](day4_4how to save custom mag file.PNG)

![](day4_5to extract lef file.PNG)

![](day4_6changes in the config file.PNG)

![](day4_7after prep add these two lines.PNG)

![](day4_8aftersuccesful synthesis.PNG)

![](day4_9 magic output after reduniong slack.PNG)

![](day5_1commandfor power distri network.PNG)

![](day5_2Routing command.PNG)

![](day5_3check weather routing strategy is 0 or niot.PNG)

![](day5_4Routing completed.PNG)

![](day5_5routing specs.PNG)

![](day5_6SPEFEXTRACTOR.PNG)

![](day5_7newspeffilewas created.PNG)

![](day5_8.PNG)
