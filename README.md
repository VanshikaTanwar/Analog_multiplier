# Four-Quadrant Analog Multiplier
This repository presents the design of Four-Quadrant Analog Multiplier implemented using Synopsys Custom Compiler on 28nm Technology .

# Table of Contents
 * [Abstract](#Abstract)
 * [Introduction](#Introduction)
 * [Analog Multiplier](#Analog-Multiplier)
 * [Four-Quadrant Analog Multiplier](#Four-Quadrant-Analog-Multiplier)
 * [Tools Used](#Tools-Used)
 * [Pre-Layout Schematics and Simulations](#Pre-Layout-Schematics-and-Simulations)
 * [Netlist of the Circuit](#Netlist-of-the-Circuit)
 * [Observations](#Observations)
 * [Author](#Author)
 * [Acknowledgements](#Acknowledgements)
 * [References](#References)

# Abstract
   Multiplication of two analog input signals is one of the most important factors which we need while working or performing operations in Analog Signal Processing. As, the multiplier is such type of a basic circuit that is used as a subcircuit in many of the other circuits, for example, it is used in analog computers, analog signal processing, etc. Up to now there are so many analog multipliers are designed with the reduction of power supply voltages, there are many CMOS existing analog multipliers are designed but they are generally designed to be operated at higher supply voltages, which are unfortunately not suitable to be applied to battery-powered systems such as portable communications systems equipment, some radio receivers, etc. 
   
   Therefore, in this paper, we are going to design a Low power consumption CMOS Analog Multiplier. The technique which we are going to use to make this design is a four-quadrant technique. We are going to design CMOS Analog Comparator using 28nm technology. Design and Implementation of this circuit will be done in Synopsys Custom design platform that is Synopsys custom design compiler tool.


# Introduction:

   An analog multiplier is basically a non-linear circuit. It is a device that contains two analog input signal and gives the product of both the input signal in its output. It is a circuit which basically gives the linear product of two continuous input signals in its output. If both the input and output signals are voltages let us say “V1” and “V2” be the input signal then in the output let’s say “Vout” it gives the product of both the input voltages divided by a scaling factor (say k). where k is the scaling factor that is any multiplication constant or a gain of suitable dimension.


           Vout = (v1*v2)/k

   It is used widely in the field of telecommunication, analog signal processing, Instrument systems etc. Analog multiplier is categorized as single quadrant which means that when both the input is positive/negative (i.e., same unipolar), two-quadrant means when one input has a positive voltage and other input could have positive or negative voltage (i.e., x is bipolar and y is unipolar), four-quadrant multiplier means when both the input is either positive or negative (i.e., when x is bipolar and y is also bipolar). 
So, in this paper, we are going to make the CMOS low power consumption analog multiplier of four-quadrant multiplier. As, four-quadrant analog multiplier is a very useful basic building block in many circuits like adaptive filters, phase-frequency detection, frequency double, function generator, frequency shifters, etc. It is also used in modulation, pll (phase-locked loop), frequency mixer, etc.

# Analog Multiplier:

<p align="center">
  

  Fig. 1: Analog Multipier 
</p>



	   	Vdd = Supply voltage of the circuit
	   	GND = Ground


# Four-Quadrant Analog Multiplier:

   The main purpose of designing a four-quadrant analog multiplier is to eliminate extra voltage reference to make a compact circuit design. By implementing and simulating this circuit in Synopsys Custom compiler tool using CMOS 28nm Technology, the device performance, density and low power consumption will be improved and achieved. The proposed design consists of a pair of common source amplifier with input transistors and the output that it gives is the square function of its input voltages v1 and v2. It contains a total of 10 transistors in which 8 are PMOS and 2 are comprised of NMOS including two resistors R1 and R2 to make the transistor to work in the proper region and the value of resistors has to be taken accordingly at the time of the simulation.  Transistor m1 to m8 acts as a non-linear cancellation path in a square root circuit. The output which comes from transistors m9 and m10 are directly going into the square root circuit block to produce differential output voltage or current which is just the product of the input signal v12 and v34. Here, v12 is the difference between v1 and v2 signal while v34 is the difference between v3 and v4 input signal and the resultant output signal Vout will be the differential output of vout1 and vout2. 

<p align="center">
	
 ![analog multipier](https://user-images.githubusercontent.com/90523478/155011823-c72c46ea-1cf8-4c27-8211-9dcab0887217.jpg)
                            Fig. 2: Four-Quadrant Analog Multiplier
	
</p>
<p>
   Hence, on observing the output waveform we conclude that the given circuit become capable to operate with the input voltage and also the requirement of low power consumption for operating the circuit is also achieved.  (And also, the requirement of achieving low power consumption also met). So, a new square root circuit can be used to realize a CMOS four-quadrant analog multiplier has been given. For the verification purpose of the multiplier circuit, a performance simulation result has been given.

# Tools Used:

<b>• Synopsys Custom Compiler:</b></br>
&emsp;The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.

<b>• Synopsys 28nm PDK:</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Synopsys Custom Compiler Tool Details
The [Synopsys Custom Compiler™](https://www.synopsys.com/implementation-and-signoff/custom-design-platform/custom-compiler.html) design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. It delivers industry-leading productivity, performance, and ease-of-use while remaining easy to adopt for users of legacy tools.
<p align="center">
  ![image](https://user-images.githubusercontent.com/90523478/155770297-e0be9ae9-d146-4e1c-9e08-57e5b71b455f.png)

</p>

<p align="center">
![image](https://user-images.githubusercontent.com/90523478/155771943-0d7497e0-e352-4623-bbb0-d33448571970.png)

</p>


# Pre-Layout Schematics and Simulations:

## Schematics:

### Four-Quadrant Analog Multiplier:


<p align="center">
	![circuit](https://user-images.githubusercontent.com/90523478/155775323-d113e1ff-bc7e-4bd2-add4-8f8df8b0c9c7.png)
  Fig. 3: Four-Quadrant Analog Multiplier
</p>

<p align="center">
  ![symbol](https://user-images.githubusercontent.com/90523478/155775543-3cb9910c-7a04-40ff-a5e3-fd2020bb4735.png)

  Fig. 4:Four-Quadrant Analog Multiplier Symbol
</p>


### Buffer:
This component is used to convert the generated sine wave to a proper square pulse and is placed at the output of the VCO. This is nothing but a couple of inverters placed in series. 
<p align="center">

  Fig. 5: Buffer Schematic
</p>
<p align="center">
 
  Fig. 6: Buffer Symbol
</p>

### Four-Quadrant Analog Multiplier:
The schematic of Four-Quadrant Analog Multiplier has been created using the above cells and a few transistors as shown in the below figure.

<p align="center">
	![symbol schmatic(a)](https://user-images.githubusercontent.com/90523478/155775620-3c79913f-1d1c-4251-9cec-ea532f07b130.png)

  Fig. 5: Symbol Schematic(a)
</p>

<p align="center">
	![symbol schmatic](https://user-images.githubusercontent.com/90523478/155775683-aaf5bafd-788e-4da7-9c5d-5acd710f59de.png)
  Fig. 5: Symbol Schematic(b)
</p>
## Simulations:
### Transient Analysis:
   After creating and saving the schematic go to 'Tools' and open 'Primewave' to start the simulation. In the Primewave select the 'model file' i.e the '28nm PDK's .lib file presentin the HSPICE folder. After this select the 'tran' analysis in the analysis window and give the 'Start', 'Stop', and 'Step Size' parameters and save it. Then add the outputs which needs to be plotted by selecting the nets on the schematic.</br>
One other thing we need to keep in mind is that here we have loop for which an initial condition needs to be declared. For that, we have to go to 'Setup -> Convergance aids' and select the net for which we want to set an initial condition.Then go to 'Simulations -> Netlist and Run' to generate a netlist and run the simulation to get the below output.
<p align="center">
  
  Fig. 8: Four-Quadrant Analog Multiplier Transient Analysis
</p>

# Netlist of the Circuit:


# Observations:


# Author:
• Vanshika Tanwar, B.Tech(ECE), Dronacharya Group of Institutions, Greater Nodia, Uttar Pradesh.

# Acknowledgements:

- [Synopsys India](https://www.synopsys.com/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Indian Institute Of Technology (IIT) Hyderabad](https://iith.ac.in/)
- [Kunal Ghosh](https://github.com/kunalg123), Founder, VSD Corp. Pvt. Ltd
-   [VLSI System Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)

# References:
