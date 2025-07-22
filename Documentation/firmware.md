# Firmware

## Intro
This is a basic HAL for the ATMEGA32E5 MCU. It will include GPIO, PWMs, I2C, and UART communications 

## How To

### GPIO

This is set up to have 6 total GPIO pins set up and can be used as follows:

PA7 is for verification that the firmware is working as expected and is only connected to a single LED.

PD5 and PD6 are true GPIO and have appropriate jumper pins

PA1, PA2, and PA3 are set up for reading hall communcation triggers as this overall is intended to be a motor driver board but will have a zero ohm jumper spot  so it could be added used for other purposes if desired.

### PWM
The chip has a build in waveform extension called WeX aand internally is able to generate H and L waveforms for gate driving of mosfets including internal deadtime to prevent any blowout. I chose to use the D, C, and B, set of waveforms so I would be able to set up multiple other peripherals

### I2C
Todo

### UART
Todo


## Development
Nautrally my first task was to set up the GPIO as it is extremely easy to check with the LED that I had set up.
