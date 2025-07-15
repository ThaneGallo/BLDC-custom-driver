# BLDC-custom-driver
ATMEGA32E5-based bldc motor driver

## Abstract 
An [ATMEGA32E5](https://www.microchip.com/en-us/product/ATxmega32E5) is a MCU created by Microchip Technology and here is set up and used as an I2C slave to run and maintain a fixed point (does not contain FPU) PID loop to drive and control the speed of a brushless DC motor.

## Introduction 
This project will be an entirely custom system from hardware to software to firmware and the development will be seperated into parts and can be found in folders which are to be linked below. 


As this system contains custom hardware and software I decided to split up into other files for ease of reading with the links below:

# Table of Contents
* [Skills Utilized](#Skills-Utilized)
* [System Diagram](#System-Diagram)
* [Hardware Design](#Hardware-Design)
* [Software Design](#Software-Design)
* [Known Issues](#Known-Issues)
* [Conclusion](#Conclusion)
* [Acknowledgements](#Acknowledgements)

# Skills Utilized
Hardware:
* KiCAD
* MCU Integration
* Motor Controls
* BLDC
* Power system design
* 4-Layer-PCB

Software:
* C++/C
* HAL / Device Drivers
* Control Systems
* Matlab/Simulink

# System Diagram


![System Diagram](Documentation/Images/System_Diagram_Guitar_Pedal.png "System Diagram")

# Hardware Deisgn

The hardware development at a top level essentially boils down to creating an ATMEGA32E5 Development board. This includes GPIO, I2C buses, Timer peripherals as well as gate driver circuitry for the BLDCs Mosfets. 

Click [here]() for the in-depth development.


# Software Design

The software is mainly firmware for getting the MCU to interface with the motor driver but I had used Simulink in order to test and figure out timings and how to structure my control loop and test it before it is made. 

Click one of the following to see the in-depth development

* [Simulation]()
* [Firmware]()

# Known Issues

# Conclusion

# Acknowledgements

