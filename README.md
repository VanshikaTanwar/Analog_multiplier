# Four-Quadrant Analog Multiplier
This repository presents the design of Four-Quadrant Analog Multiplier implemented using Synopsys Custom Compiler on 28nm Technology .

# Table of Contents
 * [Abstract](#Abstract)
 * [INTRODUCTION](#INTRODUCTION)
 * [Four-Quadrant Analog Multiplier](#Four-Quadrant-Analog-Multiplier)
 * [Tools Used](#Tools-Used)
 * [Pre-Layout Schematics and Simulations](#Pre-Layout-Schematics-and-Simulations)
 * [Netlist of the Circuit](#Netlist-of-the-Circuit)
 * [Observations](#Observations)
 * [Author](#Author)
 * [Acknowledgements](#Acknowledgements)
 * [References](#References)


# Abstract
   Multiplication of two analog input signals is one of the most important factors which we need while working or performing operations in Analog Signal Processing. As, the
   multiplier is such type of a basic circuit that is used as a subcircuit in many of the other circuits, for example, it is used in analog computers, analog signal processing,
   etc. Up to now there are so many analog multipliers are designed with the reduction of power supply voltages, there are many CMOS existing analog multipliers are designed but
   they are generally designed to be operated at higher supply voltages, which are unfortunately not suitable to be applied to battery-powered systems such as portable
   communications systems equipment, some radio receivers, etc.  
   
   Therefore, in this paper, we are going to design a Low power consumption CMOS Analog Multiplier. The technique which we are going to use to make this design is a four
-quadrant technique. We are going to design CMOS Analog multiplier using 28nm technology. Design and Implementation of this circuit will be done in Synopsys Custom design
platform tool that is Synopsys custom design compiler tool

# Introduction

  An analog multiplier is basically a non-linear circuit. It is a device that contains two analog input signal and gives the product of both the input signal in its output. It
  is a circuit that basically gives the linear product of two continuous input signals in its output. If both the input and output signals are voltages let us say “V1” and “V2”
  be the input signal then in the output let’s say “Vout” it gives the product of both the input voltages divided by a scaling factor (say k). where k is the scaling factor that
  is any multiplication constant or a gain of suitable dimension.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155834028-68561b84-48b4-4d71-9efa-fc9ea182a549.jpg"></br>
  Fig.1: Symbol of multiplier
</p>

           Vout = (v1*v2)/k
           

   It is used widely in the field of telecommunication, analog signal processing, Instrument systems etc. Analog multiplier is categorized as single quadrant which means that
when both the input is positive/negative (i.e., same unipolar), two-quadrant means when one input has a positive voltage and other input could have positive or negative
voltage (i.e., x is bipolar and y is unipolar), four-quadrant multiplier means when both the input is either positive or negative (i.e., when x is bipolar and y is also
bipolar). So, in this paper, we are going to make the CMOS low power consumption four-quadrant analog multiplier. As, four-quadrant analog multiplier is a very useful basic
building block in many circuits like adaptive filters, phase-frequency detection, frequency double, function generator, frequency shifters, etc. It is also used in modulation,
pll (phase-locked loop), frequency mixer, frequency doubler, etc.


# Four-Quadrant Analog Multiplier:

  The main purpose of designing a four-quadrant analog multiplier is to eliminate extra voltage reference to make a compact circuit design. By implementing and simulating this
circuit in Synopsys Custom compiler tool using CMOS 28nm Technology, the device performance, density and low power consumption will be improved and achieved. The proposed
design consists of a pair of common source amplifier with input transistors and the output that it gives is the square function of its input voltages v1 and v2. It contains a
total of 8 transistors in which all 8 are PMOS including two resistors R1 and R2 to make the transistor to work in the proper region and the value of resistors has to be
takenaccordingly at the time of the simulation. Transistor m1 to m8 acts as a non-linear cancellation path in a square root circuit. The output which comes from transistors
are directly going into the square root circuit block to produce differential output voltage or current which is just the product of the input signal v12 and v34. Here, v12
is the difference between v1 and v2 signal while v34 is the difference between v3 and v4 input signal and the resultant output signal Vout will be the differential output of
vout1 and vout2. 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155011823-c72c46ea-1cf8-4c27-8211-9dcab0887217.jpg"></br>
  Fig.2: REFERENCE Four-Quadrant Analog Multiplier CIRCUIT
</p>

Hence, on observing the output waveform we conclude that the given circuit become capable to operate with the input voltage and also the requirement of low power consumption for
operating the circuit is also achieved. So, a new square root circuit can be used to realize a CMOS four-quadrant analog multiplier has been given. For the verification purpose
of the multiplier circuit, a performance simulation result has been given.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155834728-73382097-31f0-4462-9ee6-4cf3d8d6e2fe.jpg"></br>
  Fig.3: REFERENCE CIRCUIT WAVEFORMS
</p>

# Tools Used:

## Synopsys Custom Compiler:
 The [Synopsys Custom Compiler™](https://www.synopsys.com/implementation-and-signoff/custom-design-platform/custom-compiler.html)design environment is a modern solution for
 full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation
 management and analysis, and custom layout editing features. This tool is used to design the circuit on a transistor level.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155798629-823e7866-48e3-4f3b-a955-8f02852f69e8.png"></br>
  Fig.3: Synopsys Custom Compiler
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155771943-0d7497e0-e352-4623-bbb0-d33448571970.png"></br>
  Fig.4: Custom compilier
</p>


<b>• Synopsys 28nm PDK:</b></br>
&emsp;The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.


# Pre-Layout Schematics and Simulations:

## Schematics:

### Four-Quadrant Analog Multiplier:

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155770297-e0be9ae9-d146-4e1c-9e08-57e5b71b455f.png"></br>
  Fig.5: Four-Quadrant Analog Multiplier cell Schematic
</p>

## Symbol:

This is the symbol of Four Quadrant Analog Multiplier as in this symbol the four circles which are shown indicates that there are 4 inputs sine signal which I have given (named
v1,v2,v3 and v4) and the cross sign which is given in between the loop it means that it is the sign of multiplier indicating that it is multiplying the input signal and the
output which comes as the multiplication of both the input is the resultant one which is going into the FQ_AM (Four Quadrant Analog Multiplier)  . So, the whole symbol indicates
that as this is the symbol of FOUR QUADRANT ANALOG MULTIPLIER which takes 4 signals as input and here In this I have given the 4 sine wave input signals which are going to
multiply (Two sine wave input signals are multiplied with each other[v1 and v3] and the other two sine wave input signal [v2 and v4] are multiplied giving the respective
output.) by the multiplier and giving the result of the multiplication of sine wave input signal.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155834879-fd4f8e46-7c81-4039-bf2a-e86c65c9d191.png"></br>
  Fig.6: Four-Quadrant Analog Multiplier cell Symbol
</p>

## Testbench of cell Symbol

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155788676-3f714c91-ea80-4f09-965f-174ea696c155.png"></br>
  Fig.6: Testbench of cell Symbol(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155789012-41046e05-21bf-48cd-a8b3-f718045e742f.png"></br>
  Fig.7: Testbench of cell Symbol(b)
</p>


## Simulations:
### Synopsys Primewave:
PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory
designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155835329-abe72b37-5b74-44b2-823c-92a77c3c90f5.jpg"></br>
  Fig.7: Primewave
</p>

### Transient Analysis:
   After creating and saving the schematic go to 'Tools' and open 'Primewave' to start the simulation. In the Primewave select the 'model file' i.e the '28nm PDK's .lib file
presentin the HSPICE folder. After this select the 'tran' analysis in the analysis window and give the 'Start', 'Stop', and 'Step Size' parameters and save it. Then add the
outputs which needs to be plotted by selecting the nets on the schematic.
One other thing we need to keep in mind is that here we have loop for which an initial condition needs to be declared. For that, we have to go to 'Setup -> Convergance aids' and
select the net for which we want to set an initial condition.Then go to 'Simulations -> Netlist and Run' to generate a netlist and run the simulation to get the below output.

Now you see that model file has been included, now the next step which we need to do now is to include the analysis 

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155800668-ec14c672-31f7-4888-9d79-2fd74a7c1e27.png"></br>
  Fig.8: Model file
</p>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155800180-c6f8e2e6-10e9-41b1-b4c4-0980034b6ff4.png"></br>
  Fig.9: Analysis
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155801132-972f490a-b6c5-4279-a818-3c71af949878.png"></br>

  Fig.10: Save Testbench State
</p>

### Waveform

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802149-3372f566-1d4a-4381-899b-bd4edae1d0db.jpg"></br>
  Fig.11: waveform(a)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802297-d6916d54-e9a9-44ba-82d6-e9fab75654ea.jpg"></br>
  Fig.12: waveform(b)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802359-14423188-b5a5-4d94-a63e-070b4dc606e2.jpg"></br>
  Fig.13: waveform(c)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802414-058b2962-f7f7-41e1-bb98-cc49cb357037.jpg"></br>
  Fig.14: waveform(d)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802473-6ef496ff-d052-44a0-a5a7-6aba56d09b8b.jpg"></br>
  Fig.15: waveform(e)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802536-caa6390d-d361-4041-aa0d-e8a8e41d2cf2.jpg"></br>
  Fig.16: waveform(f)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802571-3fce33c3-c36a-423b-970a-5100c1dfe20d.jpg"></br>
  Fig.17: waveform(g)
</p>

</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/90523478/155802630-78a8b78b-da3f-4540-95f5-87da4064c27b.jpg"></br>
  Fig.18: waveform(h)
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
- [VLSI System Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)

# References:
[1]. https://www.ijaiem.org/volume2issue7/IJAIEM-2013-07-16-049.pdf
[2]. https://aircconline.com/vlsics/V3N5/3512vlsics08.pdf
[3]. https://www.researchgate.net/publication/261076064_CMOS_Design_of_a_Multi-input_Analog_Multiplier_and_Divider_Circuit
