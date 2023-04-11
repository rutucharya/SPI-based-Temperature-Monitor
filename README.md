# SPI-based Temperature Monitor
## Overview
This project will aim at design and immplemention of a SPI-based temperature monitor. The students will design a controller in Verilog to read the data from the sensor ([LM70][datasheetLM70]) using the industry-standard SPI protocol, convert the data to a human readable format (deg-C) and drive a set of 7-segment display to display the data. In order to test the Verilog code in realtime application, the Verilog code will be synthesized into a Xilinx's Spartan FPGA board. This will allow the students to test their Verilog code in real time.

![tempMonitor-blockDiag-v1-0322](https://user-images.githubusercontent.com/98079644/231081754-86ca6e32-0ec8-4e98-8781-10b4726a049a.png)

## Installation of Xilinx Design Suite and Ahmy Software
-	For downloading and installing the Xilinx Design Suite and AHMY Software click on the [link]( https://drive.google.com/drive/folders/11K3pKGRTGL41oUaIt80uNTADWgc_MmPZ).
-	Follow the document in the given drive link to install the softwares required.

## Steps for creating a new project in Xilinx Design Suite
- Open Xilinx and create a new project from the file menu.
- Specify the name and location of the project you want to create.
