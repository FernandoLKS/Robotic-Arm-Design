# Development of a robotic arm and implementation of an application for control via bluetooth.

This repository contains the steps taken to implement a robotic arm.

## Robotic arm model

The model and parts used to make the robotic arm can be found at https://www.instructables.com/EEZYbotARM/.

## Mobile application

The flutter framework was used to create the mobile application. The implementation can be seen in more detail in `RoboticArmMobileApp\lib`.

## Microcontroller code and circuit

The microcontroller used in the project was the ATmega328P, whose code is found in `MicrocontrollerCode\src\main`. Electrical schematic and PCB template can be seen below. 
<p align="center">
<img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/08c7d99d-65fa-4570-92b9-b0e8893cceab"/>
</p>
<p align="center">
<img src=![Capturar2](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/575b5276-9920-4490-b5dc-23ee91dc96e4)/>
</p>

note: The source used for this project was 5V and 2A, to ensure power for the entire circuit.

## Installation

1. Record the code available in `MicrocontrollerCode\src\main`, and make sure the circuit and pins connected are correct.
2. Download and run the `app-release.apk` apk file on your phone.

## How to use

1. Before opening the application on the cell phone, pair it with the bluetooth module.
2. With the application open, click on the bluetooth icon and locate the robotic arm module and press on it. Wait to connect and you can go back to the home screen.
   
![WhatsApp Image 2023-06-26 at 20 34 30](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/3c1c3229-ff31-4038-a5e2-44fa35ace971) | ![WhatsApp Image 2023-06-26 at 20 34 30 (1)](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/b5cff57e-beba-4a0b-8a4b-40104a58a8de) | ![WhatsApp Image 2023-06-26 at 20 34 30 (2)](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/70a3f96a-2299-49fc-8d8e-3c4cbaaa04c5)


3. Connected to bluetooth, the initial interface features 4 sliders for manual control and 3 buttons with pre-programmed functions. Configure and calibrate the functions and angles for each motor in the files. 

To change the supported angles it is necessary to change within the application code in `RoboticArmMobileApp\lib\Servo`.

![Capturar3](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/48424106-be40-4c6a-835a-20bb36aa5ad5)

For the functions on the buttons change in the `MicrocontrollerCode\src\main` file.

![Capturar4](https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/b59ee277-8055-486f-8952-131f70d7135f)
