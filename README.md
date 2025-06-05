

# smartarduinolockwithhuskylens

Overview

This project implements a smart door lock system that uses facial recognition to grant access. The system integrates an Arduino Uno with a HuskyLens camera module, which detects and recognizes pre-registered face IDs to control a servo-driven lock mechanism. When an authorized face is detected, the servo unlocks the door.
![IMG_20250529_183939](https://github.com/user-attachments/assets/ed08540e-bd8f-4765-a641-43477a283034)
Hardware Requirements:

1.Arduino Uno: The microcontroller that processes data and controls the servo.

2.HuskyLens Camera: A smart vision sensor with built-in face recognition capabilities.

3.Servo Motor: Used to actuate the door lock mechanism (e.g., SG90 or similar).

4.Jumper Wires: For connecting the components.

5.Power Supply: 5V for Arduino and HuskyLens, with sufficient current for the servo.

6.Door and Lock Mechanism: A physical setup where the servo can engage/disengage the lock.

7.Optional: Breadboard or prototyping board for connections.
![IMG_20250529_183933](https://github.com/user-attachments/assets/85e4c643-a2de-4111-ad9d-665cef95de03)

Software Requirements:

1.Arduino IDE: For programming the Arduino Uno.

2.HuskyLens Library: Install the HUSKYLENS library via the Arduino Library Manager.

3.servo Library: Included with the Arduino IDE for controlling the servo motor.

Setup Instructions:

1.Hardware Setup

2.Connect the HuskyLens to Arduino Uno:

3.HuskyLens VCC → Arduino 5V



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

[IMG_20250529_183933](https://github.com/user-attachments/assets/85e4c643-a2de-4111-ad9d-665cef95de03)

