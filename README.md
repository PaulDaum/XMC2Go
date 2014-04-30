# Developing for XMC2Go on Debian Unstable

This repository is for software-development for the XMC2Go development board by Infineon with Debian unstable (x64).

Details: www.infineon.com/xmc-dev
Order number: KIT_XMC_2GO_XMC1100_V1
MC: xmc1100-0064

----------------------------------------------------

To start development, first install JLink \n
JLink is used to flash, erase, .., and communicate with the XMC1100 via USB

Download jlink_4.84.5_x86_64.deb
Go to http://www.segger.com/jlink-software.html
Scroll down and download "Software and documentation pack for Linux V4.84e, DEB Installer 64-bit version [6,328 kb]"

Go to /home/Download
dpkg -i jlink_4.84.5_x86_64.deb

Run JLink
JLinkExe -device xmc1100-0064 -speed 4000

use "erase" to delete flash memory
use "loadbin xxx.bin 0x10001000" to load a program into flash memory 
use "g" to start the program
