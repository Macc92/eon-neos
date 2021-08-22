NEOS
======

NEOS is the operating system for your [comma two](https://comma.ai/shop/products/comma-two-devkit) and [EON Gold Dashcam Development Kit](https://comma.ai/shop/products/eon-gold-dashcam-devkit).

Updates
------

When openpilot requires a NEOS update, you won't have to do anything. NEOS updates download in the background auotmatically, just like normal openpilot updates. This repo is for restoring or recovering your device.

**It is highly recomended that you use a Mac or usb installation of Ubuntu. You can do this using "Rufus", link below and downloading the Ubuntu .iso file. Windows has driver issues and sometimes wont pick up the comma 2 in Fast Boot Mode. Windows also has problems writing the image to the Comma 2**

Only some USB-C to USB-A cables will work, so you may have to try multiple. If an android device shows up in device manager(Windows) you have a good cable.

Ubuntu ISO - https://ubuntu.com/download/desktop

Rufus - https://rufus.ie/en/
1. Press "Select" and navigate to the Ubuntu ISO you donwloaded.  
*Click "Show Avanced Drive Properties" and click the checkbox for "List USB HardDrives.
2. Select the drive you want to install Ubuntu under the "Device" dropdown. **All data will be erased!**
3. Click start and say "Yes" to any promts.

Restoring on macOS & Linux
------

1. Connect your comma two (via a USB-C to USB-A cable) or EON Gold (via a USB-mini-B to USB-A cable) to your computer in **FastBoot Mode**
2. **FastBoot Mode** - Hold Volume down + power, when it vibrates elease the power button. Dont release the volume down button until you see fastboot mode.
3. Open a terminal 
4. Run 'sudo apt install git'
5. Install Python 3 if you havent already, link below.
6. Clone this repo `git clone https://github.com/commaai/eon-neos.git`, then `cd eon-neos`
7. Run `./download.py`
8. Put your device into fastboot mode by turning off your device, then holding volume down + power.
9. Run `./flash.sh` DO NOT DISCONNECT THE DEVICE!

You need to python 3 to run the 2 scripts involved. Follow this link for instructions:

Install Python Ubuntu: https://realpython.com/installing-python/#how-to-install-on-ubuntu-and-linux-mint


Restoring on Windows
------
1. Install the Google USB driver for ADB (Android Debug Bridge)... https://developer.android.com/studio/run/win-usb
2. Connect your comma two (via a USB-C to USB-A cable) or EON Gold (via a USB-mini-B to USB-A cable) to your computer
3. Download and extract this repository
4. Download & install Python 3
5. Run download.py to download NEOS and flashing tools
6. Put your device into fastboot mode by turning off your device, then holding volume down + power.
7. Run flash.ps1 (right click, run with powershell). DO NOT DISCONNECT THE DEVICE!
