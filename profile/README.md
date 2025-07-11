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
 * It is not neccessary to have VSCode to run the software, only to install and update!
 * Only run main.py
* The system requires a plethora of motors and sensors. Three motors should be connected to port A, B, and C. Motor A will be the throttle, or throttle/brake. Motor B will be Automatic Brake. Motor C will be Independent Brake. However, the roles of these motors will shift depending on the type of train running, especially in trains that do not have such a braking system. The color sensor will need to be connected to port 2, touch sensor to port 3, and infared sensor to port 4.
  * The color sensor will need to read three colors (black, yellow, and white) and in that order. Feel free to implement this as a sliding lever.
* This is modular, and new train configurations can be added within the programs folder.
* If the motors does not match the values in the simulator, run "Callibration". It should be saved for future runs.
* **Connect to Raspberry Pi:** Use the USB connecting cable to connect the EV3 brick to the Raspberry Pi, the next step of the process.

### Notes about the Raspberry Pi 🥧:



<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
