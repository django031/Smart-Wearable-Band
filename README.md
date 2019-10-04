# Smart-Wearable-Band

* Worked on a Soft Project of Designing of Smart Band Heart Rate Sensor Using Photoplethysmography and Bluetooth Low Energy (BLE) Technology.

## Getting Started

* The purpose of this soft project was to design a wireless heart rate monitoring device based on the principle of Photoplethysmography and using the Bluetooth Low Energy (BLE) technology. The emphasis here was mainly on the features used and to implement the firmware/RTOS development. 

## Pre-requisites  

* Knowledge of healthcare products and thier functining along with the concepts of Embedded systems, Hardware Desigining, Microprocessors/Microcontrollers, Prior Basics of Electronics, Firmware/RTOS development

## Principles and Technologies Involved 

* This soft project involves two principles and technologies used. One - "Photoplethysmography" and the other is "Bluetooth Low Energy (BLE)".

## Materials Used - 

* The main materials used in this project include nRF51822 system-on-chip (SoC) from Nordic Semiconductors, which serves both as the controller and BLE communication unit, MAX30100 i.e. Pulse oximeter, which served as the sensor unit. 

## Methods Invloved - 

* Two methods were involved to achieve the desired results. They are described below - 

* Break Out Sensor Unit 

* Hardware Setup for the break out sensor - 

## Firmware Development Environment Setup - 

* The first step in the firmware development was to set up the development environment. Linux OS was used for the same. The tools required were gcc cross compiler for ARM processors, required to compile the source code written for nRF51822 on a Linux machine.  
 
## Firmware Implementation - 

* The basic logic of the firmware is found in the main routine : 

* Main functions of the firmware - 

* int main (void)  
  { 
    twi_master_init(); init _sensor(); 
    ble_stack_init(); timer_init(); 
    gpio_init(); gap_params_init(); 
    services_init(); advertising_init(); 
    conn_params_init(); sec_params_init(); 
    advertising_start();    
    while (true) 
      {  
      power_manage(); 
      } 
   }

* Initialize I2C master 
 
* Initialize sensor function

* Intialize timers function 
 
* Initializing GPIO pins

* Sensor security paramteres intialization function 
   
 * Heart rate calculation - 
 
 * In PPG-based heart rate measurement, heart rate is determined by the number of peaks detected in the PPG signal per minute. Thus each peak in the signal represents one heart beat. The application calculates the heart rate for every 1000 samples. Since the sampling rate of the sensor is set at 100 samples per second, the application calculates the heart rate every 10 seconds. 
   
## Conclusion - 

* The main goal of this soft project was to work with MAX30100 for sensing PPG (Photoplethysmogram) signal. For this I have used nRF5822 for sensor-side control and BLE communication. The emphasis in this assignment was working mostly on the circuit diagrams and the basic functionality of the complete set-up.  
 
