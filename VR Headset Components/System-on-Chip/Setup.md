### System-on-Chip Upgrade
#### Scenario:
VRDreamerzzz.inc has found it in their hearts (budget) to improve the hardware in their next-gen headset.
The only problem is that it isn't well supported by their current IDE. 
It's your job to set up the dev environment so that the Headset Tracking and Suspense modules can be easily integrated on it.
We will also need a status light on the headset.
#### Task 
Setup a project for the STM32f3.
Implement serial communication for debugging as a loosely-coupled communications driver.
Setup a hardware timer to blink the internal user LED.
Prioritize modularity and reusability in your design.
#### Advice:
Arduino IDE does not play nicely with this microcontroller. Time to use a grown-up IDE.
You will either have to use the Arduino framework or find libraries your choice of framework for the MPU6050 and MAX30102 sensors.
#### Hardware
- 1 STM32f3
- 1 micro USB-A cable
- 1 small breadboard