# IEEE-uOttawa-ECAW-Code
ECAW is the Embedded Coding Architecture Workshop

The code in this repository is intended to provide examples of working code that needs to be modified in order for it to be used in a larger project.


## Setting up Arduino IDE

1) Download Arduino IDE: https://www.arduino.cc/en/software

If you are using Raspberry Pi Pico, then once you have Arduino IDE installed, in Arduino IDE, go to:
> File -> Preferences  -> Additional Boards Manager URLs

and add paste the following link into the the Additional Boards Manager URLs:
> https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json


2) Hardware Specific Libraries

Hardware Specific Libraries are Listed as a comment in first line of the coresponding driver example.
To add the Library to Arduino IDE, go to the **Libraries Manager** and paste the name of the hardware device (ie: GY-521) in the library search bar, then find the library that matches the link in the comment.


## Components

### VR Controller
#### Scenario
> VRDreamerzzz.inc has commissioned you with developing the controller for their upcoming VR headset.
They want to be able to detect the controller's rotation and acceleration.
They also need a joystick, trigger, and bumper buttons. 
#### Task
> Retrieve linear and rotational acceleration, button, and joystick input from the controller and transmit it with serial print.

### VR Headset Tracking
#### Scenario
> VRDreamerzzz.inc has commissioned you with developing the tracking module for their upcoming VR headset.
They want to be able to detect the headset's rotation and acceleration.
They also need to detect how far the controller is from the headset to help with hand tracking. 
#### Task
> Retrieve linear and rotational acceleration, and distance input from the headset and transmit it with serial print.

### VR Headset Suspense and Power
#### Scenario
> VRDreamerzzz.inc has commissioned you with developing the suspense module for their upcoming VR headset.
They want to improve the timing of jump-scares in the games their headset will support by giving devs data on the relative heart rate of a person.
I guess it could be used to enhance a serene setting as well, but that's boring.
They also need a power button for the headset.
#### Task
> Retrieve heart rate input and transmit it with serial print.
Also, toggle the built-in LED with the button.

### System-on-Chip Upgrade
#### Scenario
> VRDreamerzzz.inc has found it in their hearts (budget) to improve the hardware in their next-gen headset.
The only problem is that it isn't well supported by their current IDE.
It's your job to set up the dev environment so that the Headset Tracking and Suspense modules can be easily integrated on it.
We will also need a status light on the headset.
#### Task
> Set up a project for the **STM32f3**.
Implement serial communication for debugging as a loosely-coupled communications driver.
Set up a hardware timer to blink the internal user LED.
Prioritize modularity and reusability in your design.
#### Advice
> [!TIP]
> Arduino IDE does not play nicely with this microcontroller. Time to use a grown-up IDE.
You will either have to use the Arduino framework or find libraries your choice of framework for the MPU6050 and MAX30102 sensors.
