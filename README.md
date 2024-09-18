# IOT Smart Helmet for the safety of Heavy industries

## Introduction

*  Wall following robot is a robot that follows a wall and travels keeping a constant distance from the wall. 
*  Wall following is a common task in many robotics competitions.
*  But the interesting point is our project was to build a robot that travels on the centerline between two walls using only analog electronics.
*  That means we couldn’t use microcontrollers according to the [guidelines](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Project_Guidelines.pdf).

![IMG-20231206-WA0097](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/241e426e-1c0c-4cf3-a58a-3e9705a20f41)

## Working Concept

*  Two sharp IR sensors measure the distance from the robot to the side walls.
*  The difference between the sharp IR sensor values is taken as the error signal and fed into a PID control circuit.
*  The PID output signal is fed to the adder and subtractor circuits.
*  The PID output and a comparator circuit generate two PWM signals with varying duty cycles.
*  Then using the motor driver, PWM signals are fed to the left and right wheels.
*  The robot tracks the walls and travels on the centerline between walls.
*  Additionally we added another sharp IR sensor to the front of the robot to control the speed of the robot.
*  The measured distance is compared with a predefined distance and the difference is taken as the error signal.
*  The error signal is fed to a PID control circuit.
*  A PWM signal is generated using the PID output and a comparator circuit.
*  This PWM signal acts as the Base speed of the robot.
*  Consequently the additional sharp IR sensor will vary the car's speed accordingly.
*  Therefore the car will accelerate and deaccelerate according to the distance of the wall infront it.

![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/49f70bd2-af03-46a3-9955-452a3b607f5d)

## Sub Circuits and Tasks

* [Instrumentation Amplifier](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Instrumentation%20Amplifier.jpg)- Reduce noise in Sharp IR sensor outputs and amplify signals
* [PID circuit](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/PID.jpg)- Control the error signal smoothly using feedback
* [Adder & Subtractor](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Adder%20%26%20Substractor.jpg)- Generate two PWM signals with varying duty cycles according to PID output
	* Motor 1= base speed + PID output
	* Motor 2= base speed - PID output
* [PWM circuit](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/PWM.jpg)- Generate two different comparator voltages for the two motors
	* Motor 1 duty cycle ∝ base speed + PID output
	* Motor 2 duty cycle ∝ base speed - PID output
* [Voltage Regulator](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Voltage%20Regulator.png)- To get 3.3V and 5V for required parts accordingly
* [Speed Selector](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Speed%20Selector.png)- Manually control the base speed

## Hardware Specifications

* [TL084CN ICs](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/TL084CN_GeneralPurposeAmplifier.pdf)
* Two [Sharp IR Sensors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/Sharp%20IR%20Sensor.pdf) 
* Two [N20 Motors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/GA12-N20%20Motor.pdf)
* [L298N Motor Driver](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/L298%20Motor%20Driver.PDF)
* Wheels
* [Surface Mount Resistors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/resistors.png)
* [Surface Mount Capacitors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/capacitors.png)
* [Other Components](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/other%20components.png)

## Software Specifications

* Solid Works
* Altium Designer
* Multisim

![Solidworks](https://img.shields.io/badge/Solid_Works_-red)
![Altium](https://img.shields.io/badge/Altium_Designer_-%23A5915F?logo=altiumdesigner&logoColor=white)
![Multisim](https://img.shields.io/badge/Multisim_-%2357B685?logo=multisim&logoColor=white)


## Enclosure Design

![image](https://github.com/user-attachments/assets/859e3e3a-c81e-4d4e-bf23-b281d6f836fb)
![image](https://github.com/user-attachments/assets/9e67753b-6cdb-4d69-95b7-6aa5378a7395)



## PCB Design
![image](https://github.com/user-attachments/assets/1022c5a3-2b48-423b-8139-74494e7ad5d8)
![image](https://github.com/user-attachments/assets/e3b09cb9-d402-47a3-ae37-9054a9bc7e0b)


## PCB

![image](https://github.com/user-attachments/assets/d3f6123d-e865-4687-8ea2-3b273e6baa3c)
![image](https://github.com/user-attachments/assets/6380bb89-f305-4a0e-b524-c0cadfde9ed6)


## Team Members

* Ruchira Abeywardhane
* Dinujaya Wijewickrama
* Lasitha Amarasinghe
* Sahan Abeyrathna


## License
 
 * This project is licensed under the MIT License. See the [LICENSE](MIT-LICENSE.txt) file for details.
   
## For More Information - [Project Report](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Project_Report.pdf)
