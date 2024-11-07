# ww7ats
Instructions on how to receive the Western Washington Amateur Television Society with a USB Dongle

You can use an Astrometa RTL based dongle, as the one available at the following link.

https://www.amazon.com/Dongle-DVB-T2-DVB-T-Digital-Receiver/dp/B07TY5L32G

Install the drivers and application from the Astrometa website

http://www.astrometa.com.tw/integrated_en.html

Specifically the driver AMDVBT2_Setup_200917 and the application TVR_Setup_5.0.0

Once both are installed in your systems go to the application folder, located in your system drive, in this example C:
and edit the file FreqInfo.ini.

Before you are able to save the file as a regular user you will need to change the permissions in file explorer to allow users to write this file.

C:\Program Files (x86)\Astrometa\TVR\FreqInfo.ini


Locate the line under the DVB-T/T2 section that looks like
44=UK,Antenna,UHF,474,858,8

And replace with
44=WWATS,Antenna,UHF,1255,1261,6

Save the file.

Now launch the TVRplayer application from your desktop.

Select scan from the menu and select WWATS to scan the 1255Mhz repeater output.

If You have a good signal you should be able to see the repeater image.
