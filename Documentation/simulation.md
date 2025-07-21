# Simulation

## Intro
Originally I was deciding between Simulink and LabVIEW for testing and modelling the control system but I had decided to use Simulink as it gave me ample resources for learning and I had quickly completed the fundamentals course provided by Mathworks. As I am using a trial license I do not have access to all of the handy prebuilt blocks for components such as motors and motor drivers. This would lead me to model them myself using papers published about the subject matter as a reference for the mathmetcial models of the components (Can be found below)

## Important Considerations
This is modelling an IDEAL system as it makes certain assumptions in the modelling that would be untrue in the working model. For example, it assumes that mutual inductence between the coils within the motor is 0 and that energy transfer is perfect which are both not true. This was just used as a basis to begin modelling and creation of the PID control loop.

## Simulink Diagram

[System_Diagran](Documentation/photos/bldc_full_simulink_model.png)

### Blocks and Explainations
Below I will explain all of the block and a high level view of how they work and what they do. The overall file is downloadable and within this repo [here]().

#### PID Controller
Simple PID controller, I chose to make it a mask to just adjust the various gains and some characteristics of the motors max speed, it takes the reference or desired seed and the measured speed and spits out a duty for the controller PWM. 

#### Emf to Comm Signal
Takes the EMF signals from the Motor block as well as the duty cycle and converts it into command pulses for the transistors for further processing.

#### Inverter Driver
Is a mask which takes the voltage rail size and the command pulses and converts them to voltages for the stators a b and c coils. 

#### BLDC
Simulates the Brushless DC Motor given a mathmatical model found in the ackowledgements section.

The inputs to the mask are as follows:
* Inductance of stator 
* Resistance of stator 
* Torque Constant 
* Pole pairs 
* Torque Load 
* Back Emf Constant
* Motor Inertia
* Damping Constant

My simulations did not use any specific model or motor for their calculations so the parameters chosen are estimates given some research and adjusted to prevent any stability issues.

The outputs are as follows:
* Speed (RPM)
* Currents (size 3 vector for a,b and c)
* Back EMF (size 3 vector for a,b and c)
* Torque (N/m)
* Theta_M (mechanical angle in radians)
* Theta_E (electrical angle in radians)
* Hall Sensors (binay communication signal for hall sensor states)

## Analysis


## Acknowledgements
I am very grateful for all of the below open source papers I had used to refer to the mathmetical model. I will be doing this later with the stepper motor as well just so I can have more blocks to use for future projects.

* [How to Model Brushless Electric Motors for the
Design of Lightweight Robotic System](https://arxiv.org/pdf/2310.00080)
* [Mathematical Modeling of Brushless DC Motor
and its Speed Control using Pi Controller](https://www.ijert.org/research/mathematical-modeling-of-brushless-dc-motor-and-its-speed-control-using-pi-controller-IJERTV8IS050446.pdf)
