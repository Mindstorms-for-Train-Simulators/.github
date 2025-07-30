## Hi there 👋

Mindstorms for Train Simulators is a system of devices that utilzies Lego Mindstorms EV3 bricks to control cab systems for Train Simulator Classic, Train Simulator World, and OpenBVE.

## Get Involved 🌈

Lego Mindstorms was discontinued in 2022, meaning that, although there are still a lot of systems still running, this system can be ported to newer Spike PRIME kits, if anyone is interested in joining.  
There is also a possibility of using Raspberry Pi HATS that utilizes the newer LPF2 ports, doing away with the technic hubs alltogether.  
Unfortunately, I do not have the money or interest in buying the Spike PRIME kit myself.

## How to Use 💻

This project requires:
* Lego Mindstorms EV3 Brick, with three motors, a color sensor, a touch sensor, an infared sensor, and a infared beacon.
* Raspberry Pi
* Computer running the Train Simulator

### Notes about the EV3 Brick 🧱:
* Although the EV3 brick doesn't take much processing power, it is power hungry. It is recommended that you use the EV3 brick with a Battery Pack, rechargable AA batteries, or [Battery Eliminator Kit](https://www.batteryeliminatorkits.com/product-p/6aa-eliminator-kit.htm) rated for 6 AA batteries with no more than 9 volts and 2 amps, but no less than 7 volts, rated for inside use only. You might burn through a significant number of traditional AA batteries otherwise.
* The EV3 brick utilizes Micropython. Please follow installation instructions [here](https://education.lego.com/en-us/product-resources/mindstorms-ev3/teacher-resources/python-for-ev3/) needed to install the operating system, as well as installing VSCode and the neccessary [Micropython extension](https://marketplace.visualstudio.com/items?itemName=lego-education.ev3-micropython) to connect to the EV3 brick. Transfer the files from the [EV3CabControl Repository](https://github.com/Mindstorms-for-Train-Simulators/EV3CabControl) into the EV3 Brick.
 * It is not neccessary to have VSCode to run the software, only to install and update! When not updating or installing, navigate to ``main.py`` and run the script.
* The system requires a plethora of motors and sensors. Three motors should be connected to port A, B, and C. Motor A will be the throttle, or throttle/brake. Motor B will be Automatic Brake. Motor C will be Independent Brake. However, the roles of these motors will shift depending on the type of train running, especially in trains that do not have such a braking system. The color sensor will need to be connected to port 2, touch sensor to port 3, and infared sensor to port 4.
  * The color sensor will need to read three colors (black, yellow, and white) and in that order. Feel free to implement this as a sliding lever.
* This is modular, and new train configurations can be added within the programs folder.
* If the motors does not match the values in the simulator, run "Callibration". It should be saved for future runs.
* **Connect to Raspberry Pi:** Use the USB connecting cable to connect the EV3 brick to the Raspberry Pi, the next step of the process. Connect the the EV3 to the Raspberry Pi with a USB cable.

### Notes about the Raspberry Pi 🥧:
* Devices that should work are, in which checked devices are confirmed to work:
  - [ ] Raspberry Pi Zero
  - [ ] Raspberry Pi Zero 2W
  - [x] Raspberry Pi 4
  - [ ] Raspberry Pi 5
* Download the [Raspberry Pi Imager](https://www.raspberrypi.com/software/), and select the appropiate model. For the OS, select Raspberry Pi OS (other) and choose ``Raspberry Pi OS Lite (32-bit)``. The 64-bit operating system will not work for this setup procedure, but the 32-bit can run on 8GB systems without negatively impacting performance.
* Setup the Raspberry Pi appropiately, if not already.
* For setup purposes only, the Raspberry Pi will need to be connected to Wi-Fi.
  * It is likely that the Raspberry Pi will block by rf-kill. Type ``sudo raspi-config`` and select ``5 - Localization Options`` using your arrow keys. Select ``L4 WLAN Country`` and choose the country from which your Raspberry Pi is being used. Please restart the Raspberry pi with ``sudo reboot``.
  * To set the Wi-Fi, type ``sudo raspi-config`` if not already, and select ``1 System Options``. Select ``S1 Wireless LAN`` and enter your Wi-Fi network's name and password.
  * Restart your Raspberry Pi with ``sudo reboot``.
* We need to set the Raspberry Pi in gadget mode. Type ``wget https://raw.githubusercontent.com/kmpm/rpi-usb-gadget/master/rpi4-usb.sh`` and then ``bash rpi4-usb.sh``. Commands courtesy of [kmpm](https://github.com/kmpm/rpi-usb-gadget)!
  * "Continue with modifications?", type ``y`` for YES
  * "Do you want to use a DHCP server for the USB network?", type ``N`` for NO
  * "Add the line modules-load=dwc2 to /boot/firmware/cmdline.txt", type ``y`` for YES
  * "Add the line 'libcomposite' to '/etc/modules', type ``y`` for YES
  * "Select network device type", type ``1`` for RNDIS, which is best for Windows computers.
  * Restart for changes to take effect with ``sudo reboot``.

  Instructions not complete.

## To Do: 🗺️
Check out the projects located [here](https://github.com/orgs/Mindstorms-for-Train-Simulators/projects) for upcoming features and rolling stock support
