
Canon EOS Digital Info
________________________________________
The utility is for windows users, is free and will work on most recent Canon EOS Digital Cameras (models since 2010). Informations can be read from a USB-connected camera and it provides accurate data that cannot be attainable by for example reading the EXIF. This program can retrieve and edit if possible these infos:

•	Camera Model (read) + link if available to canon web site.
•	Shutter Count [Available in subversion sdk 2.14 only / not on sdk 3.5].
•	Serial Number (read).
•	Firmware Version (read) + link if available to canon web site.
•	Battery Level (read). (Fully charged battery will show 80%).
•	Owner (read & write).
•	Copyright (read & write).
•	Artist (read & write).
•	Device date/time (read & synchro within local PC date/time).
•	Generate a complete report as a small text file and Jpeg screenshot.

Canon doesn’t have shutter count included on the EXIF information of an image file, as opposed to Nikon and Pentax.
There’s no official Canon based application to find the shutter count for an EOS DSLR.
However, there are a few free tools that may help you to do this. They provide some details about the camera, including product Name, firmware version, battery level, shutter Counter, date/time, and owner/artist/copyright strings. But it does not support this features: Editing the owner/artist/copyright and synchronizing date/time within the local PC's date/time. 
For that, I wrote a new utility that includes all these features by integrating those that were missing. 
I uses an official Canon SDK (Canon ED-SDK) to retrieve and set all camera information (shutter count is retrieved via an undocumented function).
The Canon Digital Camera SDKs is freely available on this official link: https://www.didp.canon-europa.com

Important: 
I released tow subversion, one use the Canon SDK 2.14 is for camera with Digic IV, and 5/5+.  DIGIC II and dual DIGIC III cameras are not supported. EOS M (mirrorless) models are also not supported. Only Canon repair centres can provide accurate shutter readings for these models. This is a shame, buyers of older models in particular have a need to verify shutter count. 
The second subversion, using SDK 3.5, is for camera with digic6/6+ and newer, however it doesn't support retrieving the shutter actuations. Canon has removed some functions from there recent cameras DSLR like 80D and 5D mark IV. So, the shutter actuations reading is not supported any more due to firmware limitations. If someone want to know the number of actuation on a recent camera, he must send his camera to Canon service centre. Only Canon repair centres can provide shutter count for these models actually. It’s a shame canon won’t allow its customers an accurate way to read shutter count.
In this case, like for the Canon 5D Mark IV for example, you can try to use the second subversion using sdk 3.5 instead of sdk 2.14. You can edit and read some info but you can't read the shutter counts actuations.
 

________________________________________
AUTHOR
 Mourad MKHAKH <mkh.mourad@gmail.com>
________________________________________
COPYRIGHT
Copyright (C) 2016 Mourad MKHAKH.
This program may be used freely without fees, and you are welcome to redistribute it. It is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY. 
Use this program just for supported Cameras! Use it at your own risk!

________________________________________How to use:

1.	Download ZIP portable package and extract it to a folder of your choice. And launch CanonEosDigitalInfo.exe.
Using the portable version do not need of administrator privileges, allowing you to use this tool on any computer without affecting it.
The latest ZIP portable package release of CanonEosDigitalInfo are available from the Sourceforge project homepage: 
https://canon-eos-digital-info.sourceforge.io

2. Connect Camera to USB Port and Turn it ON
3. The interface of the program is very simple, it will read data from the first Canon EOS camera that is connected to your PC:
 - Click connect button in order to establish a communication session with the connected camera and read info from it. 
 - click save button to update changed owner/copyright or artist text into the camera. 
•	 - click Time synch button to update the date-time on your camera. It will be synchronized within the local date-time of your PC.
- You can generate a complete report as a text file and create a Jpeg screenshot in the same folder containing detail info about your camera. You could send this files easily by email or save them in one place instead of searching for all time you need info.


4. If done, Close Canon EOS digital info tool.
5. Enjoy :)

I'll be very pleased if my application is interesting and helpful.


________________________________________
Supported Cameras:

The following models should be supported (not all tested):
EOS 40D
EOS DIGITAL REBEL Xsi/450D/ Kiss X2
EOS DIGITAL REBEL XS/ 1000D/ KISS F
EOS 50D
EOS 5D Mark II
EOS Kiss X3/EOS REBEL T1i /EOS 500D
EOS 7D
EOS-1D Mark IV
EOS Kiss X4/EOS REBEL T2i /EOS 550D
EOS 60D
EOS Kiss X5/EOS REBEL T3i /EOS 600D
EOS Kiss X50/EOS REBEL T3 /EOS 1100D
EOS 5D Mark III
EOS 1D X
EOS Kiss X6i/EOS 650D/EOS REBEL T4i
EOS M
EOS 6D
EOS-1D C
EOS Kiss X7i/EOS 700D /EOS REBEL T5i
EOS Kiss X7/EOS 100D/EOS REBEL SL1
EOS 70D
EOS M2
EOS Kiss X70/EOS 1200D/EOS REBEL T5/EOS Hi

****Use the SDK 3.5 instead of SDK 2.14 for this cameras
(The shutter Count is Not Available):
EOS 5DS / EOS 5DS R / EOS REBEL T6s / EOS 760D / EOS 8000D / EOS REBEL T6i / EOS 750D / EOS Kiss
X8i / EOS M3 / EOS 7D Mark II
EOS-1D X Mark II / EOS 80D / EOS Rebel T6 / EOS 1300D / EOS Kiss X80 / EOS M10.


________________________________________
Frequently Asked Questions:
•	Why my camera is not supported?
There are technical limitations that prevent supporting some cameras:
Older DIGIC II and Pre-DIGIC III Canon cameras like 1-series Canons (such as the 1D Mark III and 1Ds Mark III) do not provide shutter count information through the USB port. The EOS M operates in mass storage mode only, and does not allow PTP remote control which is needed for the reading.
Recent Cameras with DIGIC 6/6+ like the EOS-1D X Mark II, EOS 5DS, 5DS R, 80D, 750D / Rebel T6i / Kiss X8i and 760D / Rebel T6s / 8000D do not provide too actuation count information. It seems that Canon has removed the shutter count functionality from the firmware. As far as we know, Canon service centers can still tell you the shutter count for a fee. You should consult your service center for details.
•	My Camera supposed be supported by the application, but it does not recognize it: 
If the camera cannot be connected with the PC, The application cannot recognize the camera. 
Check the following:
-	Check that the camera’s power switch is < ON >.
-	If you have a Wi-Fi capable camera (such as the EOS 6D and 70D), check If [Wi-Fi/NFC], or [Wi-Fi only] is not set to [Enable] under the camera’s control menu tab. Be sure to set [Wi-Fi/NFC] to [Disable].
-	The USB connection is working: Launch Canon's EOS Utility to check this. Some USB plugs do not work correctly with Canon camera USB sockets. It is recommended to connected the camera properly to the computer with the supplied USB cable
-	Your camera is used by another application: if the camera establish a communication session withe like EOS Utility or another third party application you have to disconnect and close all these applications.
-	You should update to the latest available firmware.

•	Serial number not displayed correctly! 
Instead of the correct serial number, the tool displays a small or wrong negative number. There is a bug in older Canon camera firmware revisions, thus returning an incorrect short string. You should update to the latest available firmware. ( bug fixed in the latest version v1.3 build) 
•	What is Owner, artist’s name and copyright? What’s the difference between Owner and artist name? 
A more non-obtrusive way that images can be identified is if the original photographer’s name and copyright notice can be attached to the EXIF text (information) data that accompanies an image file. You can set two different entries names for your Canon EOS camera: an owner's name and an author/artist name. The author/artist name can be set in-camera, but to set or change the owner name you must use Canon's EOS Utility. This tool provide you access to change all this entries including the owner’s name. You can enter and set up to 31 characters as the camera owner’s name, 63 characters or symbols, including a prefix, as the author’s name and the photo creation’s copyright holder (copyright information). For more info: http://www.learn.usa.canon.com/resources/articles/2013/adding_copyright_information.shtml.
•	What is the expected shutter life of my camera?
There are a few things you'll want to know about the life of your shutter. First of all, the camera manufacturers publicize the shutter rating of the camera. Most entry-level DSLR cameras are only rated at 100,000 shutter actuations. Mid and high-end cameras have more durable shutters that are rated up to between 150,000 and 300,000 actuations.
The following list summarizes the expected shutter life for some supported professional and mid-range cameras.
-	400000 actuations for Canon EOS-1D X and EOS-1D C
-	300000 actuations for Canon EOS-1D Mark IV
-	200000 actuations for Canon EOS 7D Mark II
-	150000 actuations for Canon EOS 5D Mark II, EOS 5D Mark III and EOS 7D
-	100000 actuations for Canon EOS 6D, EOS 50D, EOS 60D and EOS 70D
It should be noted that shutter actuation is a statistical value, and there always be flukes in statistics. Your camera may last only half as long or twice as long as its rated lifetime, depending on your usage, a shutter count of say 100,000 or 150,000 can either be too high or too low. Your camera will not stop working after reaching these numbers. There are cameras with much more actuations than the expected figure. So treat these numbers as a rough guideline.

Mourad MKHAKH © 2017
