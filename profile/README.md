## Hi there 👋

Mindstorms for Train Simulators is a system of devices that utilzies Lego Mindstorms EV3 bricks to control cab systems for Train Simulator Classic, Train Simulator World, and OpenBVE.

## Get Involved 🌈

Lego Mindstorms was discontinued in 2022, meaning that, although there are still a lot of systems still running, this system can be ported to newer Spike PRIME kits, if anyone is interested in joining.  
There is also a possibility of using Raspberry Pi HATS that utilizes the newer LPF2 ports, doing away with the technic hubs.  
Unfortunately, I do not have the money or interest in buying the Spike PRIME kit myself.

## How to Use 💻

> :warning: **A DISCLAIMER**: Unfortunately, the connection between the EV3 brick and the computer results in the loss of WiFi. There's not much I can do here. Luckily, you are driving a train that doesn't need WiFi. But this means that you can't play the game while watching a Youtube video. Not like you should do that anyways.  

This project requires:
* Lego Mindstorms EV3 Brick, with three motors, a color sensor, a touch sensor, an infared sensor, and a infared beacon.
* Raspberry Pi
* Computer running the Train Simulator

### Setting up the EV3 Brick 🧱:
* Although the EV3 brick doesn't take much processing power, it is power hungry. It is recommended that you use the EV3 brick with a Battery Pack, rechargable AA batteries, or [Battery Eliminator Kit](https://www.batteryeliminatorkits.com/product-p/6aa-eliminator-kit.htm) rated for 6 AA batteries with no more than 9 volts and 2 amps, but no less than 7 volts, rated for inside use only. You might burn through a significant number of traditional AA batteries otherwise.
* The EV3 brick utilizes Micropython. Please follow installation instructions [here](https://education.lego.com/en-us/product-resources/mindstorms-ev3/teacher-resources/python-for-ev3/) needed to install the operating system, as well as installing VSCode and the neccessary [Micropython extension](https://marketplace.visualstudio.com/items?itemName=lego-education.ev3-micropython) to connect to the EV3 brick. Transfer the files from the [EV3CabControl Repository](https://github.com/Mindstorms-for-Train-Simulators/EV3CabControl) into the EV3 Brick.
 * It is not neccessary to have VSCode to run the software, only to install and update! When not updating or installing, navigate to ``main.py`` and run the script.
* The system requires a plethora of motors and sensors. Three motors should be connected to port A, B, and C. Motor A will be the throttle, or throttle/brake. Motor B will be Automatic Brake. Motor C will be Independent Brake. However, the roles of these motors will shift depending on the type of train running, especially in trains that do not have such a braking system. The color sensor will need to be connected to port 2, touch sensor to port 3, and infared sensor to port 4.
  * The color sensor will need to read three colors (black, yellow, and white) and in that order. Feel free to implement this as a sliding lever.
* This is modular, and new train configurations can be added within the programs folder.
* If the motors does not match the values in the simulator, run "Callibration". It should be saved for future runs.
* **Connect to Computer:** Use the USB connecting cable to connect the EV3 brick to your computer. Ensure that your EV3 brick is in tethering mode by going to ``Wireless and Networks > Tethering`` and checking the ``Gadget`` option.

### Setting up the Computer - Bridge 💻:
* Download ``main.py`` from the [VirtualHID](https://github.com/Mindstorms-for-Train-Simulators/VirtualHID) repository.
* Install the latest Python program from the Microsoft Store. As of time of writing, it is [v3.13](https://apps.microsoft.com/detail/9PNRBTZXMB4Z?hl=en-us&gl=US&ocid=pdpshare).
* Open up Windows Command Prompt. Install the [keyboard](https://pypi.org/project/keyboard/) and [pyvjoy modules](https://pypi.org/project/pyvjoy/) with ``pip install keyboard pyvjoy``. If this doesn't work, try running Windows Command Prompt as an administrator.
* Install [vJoystick](https://sourceforge.net/projects/vjoystick/).
  * Open up the Configure vJoy application in the computer's search bar and add devices 2-6. Restart your computer when prompted.
  * Open up the Configure vJoy application again. Go through all six devices, unchecking everything except for slider. Set the amount of buttons to 0. 

### Setting up the Computer - CobraOne Driver ♥️:
* 
  
## To Do: 🗺️
Check out the projects located [here](https://github.com/orgs/Mindstorms-for-Train-Simulators/projects) for upcoming features and rolling stock support
