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
