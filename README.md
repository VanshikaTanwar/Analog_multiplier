# Four-Quadrant Analog Multiplier
This repository presents the design of Four-Quadrant Analog Multiplier implemented using Synopsys Custom Compiler on 28nm Technology .

# Abstract
   Multiplication of two analog input signals is one of the most important factors which we need while working or performing operations in Analog Signal Processing. As, the
   multiplier is such type of a basic circuit that is used as a subcircuit in many of the other circuits, for example, it is used in analog computers, analog signal processing,
   etc. Up to now there are so many analog multipliers are designed with the reduction of power supply voltages, there are many CMOS existing analog multipliers are designed but 
   they are generally designed to be operated at higher supply voltages, which are unfortunately not suitable to be applied to battery-powered systems such as portable  
   communications systems equipment, some radio receivers, etc. 
   
   Therefore, in this paper, we are going to design a Low power consumption CMOS Analog Multiplier. The technique which we are going to use to make this design is a four-quadrant 
   technique. We are going to design CMOS Analog Comparator using 28nm technology. Design and Implementation of this circuit will be done in Synopsys Custom design platform that 
   is Synopsys custom design compiler tool.
   
# Introduction:
    An analog multiplier is basically a non-linear circuit. It is a device that contains two analog input signal and gives the product of both the input signal in its output. It is a circuit which basically gives the linear product of two continuous input signals in its output. If both the input and output signals are voltages let us say “V1” and “V2” be
the input signal then in the output let’s say “Vout” it gives the product of both the input voltages divided by a scaling factor (say k). where k is the scaling factor that is 
any multiplication constant or a gain of suitable dimension.


           Vout = (v1*v2)/k

   It is used widely in the field of telecommunication, analog signal processing, Instrument systems etc. Analog multiplier is categorized as single quadrant which means that when
both the input is positive/negative (i.e., same unipolar), two-quadrant means when one input has a positive voltage and other input could have positive or negative voltage (i.e., 
x is bipolar and y is unipolar), four-quadrant multiplier means when both the input is either positive or negative (i.e., when x is bipolar and y is also bipolar). 
So, in this paper, we are going to make the CMOS low power consumption analog multiplier of four-quadrant multiplier. As, four-quadrant analog multiplier is a very useful basic
building block in many circuits like adaptive filters, phase-frequency detection, frequency double, function generator, frequency shifters, etc. It is also used in modulation, pll
(phase-locked loop), frequency mixer, etc.

# Four-Quadrant Analog Multiplier:

   The main purpose of designing a four-quadrant analog multiplier is to eliminate extra voltage reference to make a compact circuit design. By implementing and simulating this
circuit in Synopsys Custom compiler tool using CMOS 28nm Technology, the device performance, density and low power consumption will be improved and achieved. The proposed design
consists of a pair of common source amplifier with input transistors and the output that it gives is the square function of its input voltages v1 and v2. It contains a total of
10 transistors in which 8 are PMOS and 2 are comprised of NMOS including two resistors R1 and R2 to make the transistor to work in the proper region and the value of resistors
has to be taken accordingly at the time of the simulation.  Transistor m1 to m8 acts as a non-linear cancellation path in a square root circuit. The output which comes from
transistors m9 and m10 are directly going into the square root circuit block to produce differential output voltage or current which is just the product of the input signal v12
and v34. Here, v12 is the difference between v1 and v2 signal while v34 is the difference between v3 and v4 input signal and the resultant output signal Vout will be the
differential output of vout1 and vout2.

<p align="center">
  ![analog multipier](https://user-images.githubusercontent.com/90523478/155011823-c72c46ea-1cf8-4c27-8211-9dcab0887217.jpg)
  Fig. 2: Differential Delay Cell
</p>
<p>



