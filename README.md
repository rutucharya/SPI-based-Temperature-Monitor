# SPI-based Temperature Monitor
## Overview
This project will aim at design and implemention of a SPI-based temperature monitor. The students will design a controller in Verilog to read the data from the sensor [LM70](https://github.com/rutucharya/SPI-based-Temperature-Monitor/files/11198677/datasheet-LM70-TI-tempSensor.pdf)
 using the industry-standard SPI protocol, convert the data to a human readable format (deg-C) and drive a set of 7-segment display to display the data. In order to test the Verilog code in real-time application, the Verilog code will be synthesized into a Xilinx's Spartan FPGA board. This will allow the students to test their Verilog code in real time.
 

![tempMonitor-blockDiag-v1-0322](https://user-images.githubusercontent.com/98079644/231081754-86ca6e32-0ec8-4e98-8781-10b4726a049a.png)

## Installation of Xilinx Design Suite and Ahmy Software
-	For downloading and installing the Xilinx Design Suite and AHMY Software click on the [link]( https://drive.google.com/drive/folders/11K3pKGRTGL41oUaIt80uNTADWgc_MmPZ).
-	Follow the document in the given drive link to install the software required.

## Steps for creating a new project in Xilinx Design Suite
### Step 1:
- Open Xilinx and create a "New Project" from the file menu.
- Specify the name and location of the project you want to create and set the "Top level source type: HDL".
- Under the **New Project Wizard** window, change the project specifications according to the board.
- Some of the general specifications are:
  - Property Name: Value
  - Evaluation Development Board: None Specified
  - Product Category: All
  - Family: Spartan6
  - Device: XC6SLX9
  - Package: TQG144
  - Speed: -3
  - Top-Level Source Type: HDL
  - Synthesis Tool: XST(VHDL/Verilog)  
  - Simulator: ISim(VHDL/Verilog)
  - Preferred Language: Verilog
  - Property Specification in Project File: Store all values
  - VHDL Source Analysis Standards: VHDL-93
 
### Step 2:
- A new project navigation window will appear with desired file name.
- In project navigation window, right click on the hierarchy code (e.g., xc6slx9-2tqg144) and click on "New Source" and specify the name of the program.
- After clicking next a **New source wizard** window will appear. 
- In **New source wizard** window, click on "Verilog Module". Provide the file name and location and then click on "Next"
- In the next window provide the input, output or bus ports required in the code(optional).
- In "New Source" window, write the respective verilog code and click on "Save".
- Right click on the source file and click on "Set as Top Module". This enables us to test and synthesize the code completely, otherwise only syntax check is possible.   
- Click on "yes and continue".
- Click on "Check Syntax" in **Process Window** below and run other simulation options.

### Step 3: 
- After syntax check, right click on the Verilog file name and click on "New Source".
- Click on "Implementation Constraints File". This enables us to create a new User Constraint File(.ucf).
- Provide a name for the ucf file and click on "Next".  
- Under **Process Window**, click on "Edit Constraints" to edit the UCF.
- Edit the ucf providing all the required inputs and outputs providing the respective ports and "Save" the file.

### Step 4:
- Under **Process Window**, right click on "Generate Programming File" and click on "Rerun all". This will lead to the synthesis of the code. 
- Now click on "Configure Target Device".
- A dialogue box will appear click on "ok".
- An **ISE Impact** window will appear.
- On the top-left corner click on the "IMPACT Flows".
- Now click on "Boundary Scan".
- Right click on the center of the window and click on "Initialize Chain". This will establish a relation between the PC and the FPGA board.

### Step 5:
- Open the AHMY software from the task bar. 
  - Click on "Connect".
  - Click on "Browse" and open the .bit file created in the specified location.
  - Click on "Show".
  - Then click on "Download".
