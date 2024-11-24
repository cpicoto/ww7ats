# ww7ats
Instructions on how to receive the Western Washington Amateur Television Society with a USB Dongle

You can use an Astrometa RTL based dongle, as the one available at the following links.

https://www.amazon.com/Dongle-DVB-T2-DVB-T-Digital-Receiver/dp/B07TY5L32G

https://www.aliexpress.us/item/3256801626129865.html

https://www.aliexpress.us/item/3256806959029656.html



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


Alternatively you can use VLC as the viewer application after you installed the driver and application above.
    Download the latest version of VLC from https://www.videolan.org/vlc/

    Option 1-Command line option: vlc dvb-t://frequency=1255000000 :dvb-bandwidth=6 :dvb-adapter=0

    Option 2-You can also download the WWATS.xspf file in this repo, save it do the desktop and use 
            it as a shortcut to launch the repeater viewer

    Option 3-Start a session directly from VLC
        From the Media menu use Open Capture Device, 
        select TV - digital instead of Direcshow, 
        leave Tuner card as 0, 
        select DVB-T if not selected already 
        enter 1255000 into Transponder/multiplex frequency (only 3 zeros not 6)
        Select 6Mhz for Bandwidth
        Press the Play Button to start receiving



