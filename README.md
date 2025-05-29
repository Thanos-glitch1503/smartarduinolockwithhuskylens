# smartarduinolockwithhuskylens

Overview

This project implements a smart door lock system that uses facial recognition to grant access. The system integrates an Arduino Uno with a HuskyLens camera module, which detects and recognizes pre-registered face IDs to control a servo-driven lock mechanism. When an authorized face is detected, the servo unlocks the door.

Hardware Requirements





Arduino Uno: The microcontroller that processes data and controls the servo.



HuskyLens Camera: A smart vision sensor with built-in face recognition capabilities.



Servo Motor: Used to actuate the door lock mechanism (e.g., SG90 or similar).



Jumper Wires: For connecting the components.



Power Supply: 5V for Arduino and HuskyLens, with sufficient current for the servo.



Door and Lock Mechanism: A physical setup where the servo can engage/disengage the lock.



Optional: Breadboard or prototyping board for connections.

Software Requirements





Arduino IDE: For programming the Arduino Uno.



HuskyLens Library: Install the HUSKYLENS library via the Arduino Library Manager.



Servo Library: Included with the Arduino IDE for controlling the servo motor.

Setup Instructions

Hardware Setup





Connect the HuskyLens to Arduino Uno:





HuskyLens VCC → Arduino 5V



HuskyLens GND → Arduino GND



HuskyLens TX (pin 0) → Arduino RX (pin 0)



HuskyLens RX (pin 1) → Arduino TX (pin 1)



Note: Use SoftwareSerial if pins 0 and 1 are occupied.



Connect the Servo Motor:





Servo Signal (orange) → Arduino Pin 9 (or any PWM pin)



Servo VCC (red) → Arduino 5V



Servo GND (brown) → Arduino GND



Mount the Hardware:





Attach the HuskyLens camera to face the area where users will stand.



Secure the servo to the door lock mechanism, ensuring it can move the lock.

Software Setup





Install Arduino IDE:





Download and install from arduino.cc.



Install HuskyLens Library:





Open Arduino IDE, go to Sketch > Include Library > Manage Libraries, search for HUSKYLENS, and install.



Upload the Code:





Copy the sample code (provided in code/ folder or below) to the Arduino IDE.



Update the face IDs in the code to match those registered on the HuskyLens.



Upload the code to the Arduino Uno.



Configure HuskyLens:





Power on the HuskyLens and set it to Face Recognition mode using its built-in interface.



Register authorized faces by following the HuskyLens manual to assign face IDs.

Sample Code
