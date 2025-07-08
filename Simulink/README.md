# Introduction

I have decided to use simulink in order to graphically organize and simulate the kinematics for the motor driver. This consists of a simple PID loop as well as some small transformations to change the commands into ones processable by the bldc motor.

## Diagram 

### PID Controller
Takes in a desired speed in the form of a step as well as a noisy sesor reading which in this simulation and outputs a desired speed command. The parameters are simply the gain settings and should be adjusted on a device by device basis.

### RPM to Duty Cycle
Converts the desired RPM to the corresponding duty cycle through a simple gain calculation

### BLDC Driver
Takes in direction and duty cycle from the previous block and simulates the control signals for powering on and off of the half bridges for output to drive the motor.

### BLDC Motor
Takes the driver pulses and simulates the spin of the motor and outputs the hall sensor readings as a vector of three boolean values


### Sensor
Not modelled after any sensor in particular however the parameters for edit are the mean and varience of the noise as well as the max speed of the motor.

## Known Issues
Limited tools for simulation availible. This is because I do not have the full version and I only have access to a trial membership for Simulink


## Conclusion 
