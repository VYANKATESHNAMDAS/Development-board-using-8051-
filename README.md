# 8051 Microcontroller Development Board Project

## Overview
This project demonstrates the interfacing of an 8051 microcontroller with an LCD display, a DC motor, and a Digital-to-Analog Converter (DAC). The project is implemented using Keil uVision for programming the 8051 microcontroller. The main features of the project include displaying messages on the LCD, controlling the direction of a DC motor, and generating an analog output using the DAC.

## Components Used :-
- AT89C51 Microcontroller
- 16x2 LCD Display
- L293D Motor Driver
- DC Motor
- DAC0808
- 11.0592 MHz Crystal Oscillator
- Capacitors (33pF)
- Resistors (10kΩ for pull-ups, 1kΩ for LCD)
- Potentiometer (10kΩ) for LCD contrast
- Power Supply (+5V and +12V)

## Circuit Description

### LCD Interface :-
- The 16x2 LCD is connected to Port 2 of the microcontroller. The data pins D4-D7 are connected to P2.4-P2.7, RS to P2.0, RW to P2.1, and EN to P2.2.
- A 10kΩ potentiometer is used to adjust the contrast of the LCD.

### DC Motor Control
- The DC motor is controlled using the L293D motor driver. The motor driver’s inputs IN1 and IN2 are connected to P1.0 and P1.1, respectively.
- The motor can rotate in both clockwise and counterclockwise directions based on the signals sent from the microcontroller.

### DAC Interface
- The DAC0808 is connected to Port 0 of the microcontroller. The microcontroller outputs an 8-bit value to Port 0, which is converted into an analog voltage by the DAC.

### Code Description

#### Main Functions
- LCD_Init(): Initializes the LCD in 4-bit mode, setting up the required display configuration.
- LCD_Command(unsigned char command): Sends a command to the LCD to control its operations (e.g., clearing the screen, setting cursor position).
- LCD_Data(unsigned char data): Sends data to the LCD to be displayed on the screen.
- LCD_String(char *str): Displays a string on the LCD.
- DAC_Output(unsigned char value): Sends an 8-bit value to the DAC to produce an analog output voltage.
- Motor_Clockwise(): Rotates the motor in a clockwise direction.
- Motor_CounterClockwise(): Rotates the motor in a counterclockwise direction.
- Motor_Stop(): Stops the motor.
- delay_ms(unsigned int ms): Introduces a delay in milliseconds.

#### Workflow
- The microcontroller initializes the LCD and displays a welcome message.
- The DC motor is then rotated clockwise for 5 seconds and stopped.
- The microcontroller outputs an increasing voltage using the DAC.
- The LCD displays the "Program End" message, and the program terminates.

#### How to Use
- Hardware Setup: Build the circuit as per the schematic. Ensure that all connections are correct and secure.

#### Software Setup:
- Install Keil uVision and Proteus for development and simulation.
- Compile the provided code in Keil to generate the HEX file.
- Load the HEX file into Proteus for simulation, or program it into the microcontroller for real hardware implementation.

#### Run the Simulation/Program:
- In Proteus, run the simulation to see the motor control, LCD messages, and DAC output.
- On actual hardware, observe the LCD messages, motor rotation, and DAC output on an oscilloscope or similar device.

#### Files Included
- main.c: Source code for the 8051 microcontroller.
- schematic.pdf: Circuit diagram for the project.
- HEX File: Compiled HEX file for use in simulations.

#### Contact

##### If you have any questions, suggestions, or need further assistance with this project, feel free to reach out:
- Email: vyankateshnamdas0@gmail.com
- LinkedIn: https://www.linkedin.com/in/vyankateshnamdas/
