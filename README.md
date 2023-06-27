# Development of a robotic arm and implementation of an application for control via bluetooth.

This repository contains the steps taken to implement a robotic arm.

## Robotic arm model

The model and parts used to make the robotic arm can be found at https://www.instructables.com/EEZYbotARM/.

## Mobile application

The flutter framework was used to create the mobile application. The implementation can be seen in more detail in `RoboticArmMobileApp\lib`.

## Microcontroller code and circuit

The microcontroller used in the project was the ATmega328P, whose code is found in `MicrocontrollerCode\src\main`. Electrical schematic and PCB template can be seen below. 

<p align="center">
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/6113f6c5-d720-48cb-b7bf-7d04be756f8a"
/>
<p align="center">
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/41cbd6b2-505e-4b58-9cbb-b90246b63d2d"
/>

note: The source used for this project was 5V and 2A, to ensure power for the entire circuit.

## Installation

1. Record the code available in `MicrocontrollerCode\src\main`, and make sure the circuit and pins connected are correct.
2. Download and run the `app-release.apk` apk file on your phone.

## How to use

1. Before opening the application on the cell phone, pair it with the bluetooth module.
2. With the application open, click on the bluetooth icon and locate the robotic arm module and press on it. Wait to connect and you can go back to the home screen.
3. 
<p align="center">
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/aacf7fd2-3a82-403e-b6f8-0c7c4bda952c"/>
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/adb19ff1-3173-46f3-8f62-70e1f5bc3616" />
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/d5f1a376-5fb5-4b7d-9eea-e00faf2de2d5"/>

3. Connected to bluetooth, the initial interface features 4 sliders for manual control and 3 buttons with pre-programmed functions. Configure and calibrate the functions and angles for each motor in the files. 

To change the supported angles it is necessary to change within the application code in `RoboticArmMobileApp\lib\Servo`.

<p align="center">
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/48424106-be40-4c6a-835a-20bb36aa5ad5"
/>)

For the functions on the buttons change in the `MicrocontrollerCode\src\main` file.

<p align="center">
  <img src="https://github.com/FernandoLKS/Robotic-Arm-Design/assets/114883109/b59ee277-8055-486f-8952-131f70d7135f"
/>)
