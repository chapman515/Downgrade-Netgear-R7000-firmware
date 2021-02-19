# Downgrade R7000 firmware (for flashing 3rd party firmware)

The new bought R7000 with new firmware does not allow user flashing 3rd party firmware nor flashing old firmware. In order to flash 3rd firmware, we need to downgrade it to previous firmware. Thanks to @jcleher providing nmrpflash, we can first downgrade it and flash any 3rd party firmware you want.

------

## Required file:

Nmrpflash:
https://github.com/jclehner/nmrpflash/releases/tag/v0.9.14

Npcap:

https://nmap.org/npcap/

Old official firmware:

https://www.downloads.netgear.com/files/GDC/R7000/R7000-V1.0.3.56_1.1.25.zip

------



## Installation:

0. Make sure your computer is connected to the router using an ethernet cable and  it is **connected to the first LAN port**

1. Put the downloaded official firmware `R7000-V1.0.3.56_1.1.24.zip` into nmrpflash directory
2. Open cmd (Run as administrator) and go to nmrpflash directory
3. Type `nmrpflash -L` and find the name of your interface (in my case is `net3`)
4. Turn off your router

5. Type `nmrpflash.exe -i net* -a 192.168.1.1 -f R7000-V1.0.3.56_1.1.25.chk` (* equals to the number you have found previously)

6. Turn on your router

7. Press enter

8. If it shows `Timeout while waiting for TFTP_UL_REQ.` , press up arrow key and press enter again

9. You have flashed the old firmware successfully!

   ------

   ## Reference:

   https://koolshare.cn/forum.php?mod=viewthread&tid=142232