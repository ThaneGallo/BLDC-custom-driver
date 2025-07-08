# BLDC-custom-driver
ATMEGA32E5-based bldc motor driver

## Abstract 
An [ATMEGA32E5](https://www.microchip.com/en-us/product/ATxmega32E5) is a MCU created by Microchip Technology and here is set up and used as an I2C slave to run and maintain a fixed point (does not contain FPU) PID loop to drive and control the speed of a brushless DC motor.

## Introduction 
This project will be an entirely custom system from hardware to software to firmware and the development will be seperated into parts and can be found in folders which are to be linked below. 

## Development 
First the hardware was created, it was created with a few things in mind. One of which is that there are 0 ohm jumper resistors to and from the on board MCU to the components as well as pin headers to test the hardware components using an external device if the MCU is not set up properly (This is my first time creating a custom embedded board)
