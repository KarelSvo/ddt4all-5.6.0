# DDT4all
This is a stable ddt4all version based on Python 2. Works well on Windows XP and later. 

This is the original Python 2 version of Cédric PAILLE with some updates. Also known from the [drive2.ru blog](https://www.drive2.ru/users/zmiterm/blog) by zmiterm (Dmitry Monich). 
The improvements are intended to simplify and facilitate the use of the software.

DDT4all is tool to connect to your Renault, Dacia and Nissan vehicle with an ELM327 cable.

This application is work in progress, so be very carful when using expert mode. If you're brave enough to use it and it's working (or not), please tell me so I can update the tested ECUs database.
Using the application in non expert mode should not be harmful for your vehicle (leave the expert mode button released).

## Disclaimer:  
## IF YOU ARE NOT SURE, DO NOT INSTALL THIS PROGRAM!!!
The possible uninhibited use of ddt4all can lead to work interruptions or failure, both of individual units and components of the car, as well as the car as a whole, they can also be a reason to reduce the level of vehicle safety and refuse warranty service.

If you decide to conduct experiments on one car, you must clearly understand all the risks and only accept them.

This Project is in no way affiliated with, authorized, maintained, sponsored or endorsed by ANYONE.

This is an independent and unofficial project for educational use ONLY. Do not use for any other purpose than education, testing and research.

Do not use this software if you don't have a strong knowledge of how a CAN network (or ECU) works, you can really do bad things with it, especially if you're working on a vehicle.

The author declines all responsibility about a bad use of this tool. You are the only responsible.

This tool is mainly aimed for CAN ISO_TP network study.

## Interface
Recommendations:
* OBDLink SX, MX, EX, LX
* vGate vLinker FS USB and Bluetooth
* Attention, if you want to buy a Chinese ELM327 clone, read this information: [Difference between good and bad ELM327 interface](https://cvtz50.info/en/elm327/)

It is not easy to find a good ELM copy,  that can configure the individual CAN addresses. Many of these Chinese offers are only specialized in, automatically connecting to the engine control unit, to read [OBD II parameters](https://en.wikipedia.org/wiki/OBD-II_PIDs).

Some radio and navigation control units are connected to the OBD socket pins 13 and 12.
To read these control units, OBD pin 13 must be redirected to interface pin 6 and OBD pin 12 to interface pin 14.
![can2](https://github.com/user-attachments/assets/829e5ea3-cc16-425d-bdcf-91597730fc3c)

This type of [OBD splitter cable](www.google.com/search?q=obd+splitter+cable) is ideal for building a Can 2 adapter.
![split](https://github.com/user-attachments/assets/cda24a0a-6f05-43eb-9a83-0b51f030f52d)



## Dependencies :
* Python 2.7
* PyQt 4.8
* The DDT2000 database (you must own it) - Copy the 'ecus' directory from your DDT2000 db (from C:\DDT2000data) to the ddt4all root directory

## Windows installer

Get the fully packaged installer here :
* [Release area](https://github.com/KarelSvo/ddt4all-5.6.0/releases/tag/5.6.0) 
* [Alternative area](https://s2.dosya.tc/server31/of18y5/ddt4all.exe.html) 
* [Older versions](https://www.drive2.ru/b/498093336985338243/) 

## Features :

* Read/Clear DTC
* Manual ECU request
* Log recorder
* Plugins system for automated functions
* CAN / KWP2000 supported bus protocols
* AutoScan ECUs and select the related files
* Internal JSON file format for high speed parsing
* Database zip compression of converted JSON files
* Can bus sniffing (Read/Decode non-ISOTP frames)

## How to install database ?

Copy the 'ecus' directory from your database to the root of the sources tree and launch ddt4all.py, you are now ready to use it

## How to launch the application ?

* Windows : [Windows Installer](https://github.com/KarelSvo/ddt4all-5.6.0#windows-installer) Just click on the desktop icon :-)


## How to compress XML files ?

* Go to menu 'File' > 'Zip database'
* remove 'ecus' directory

## Platforms

* Windows (XP+)
* Linux and MacOS [Download here](https://github.com/KarelSvo/ddt4all-5.6.0/archive/refs/heads/3.zip)

## Videos

* [Changing roof minimum speed operation on Megane II Cabriolet](https://www.youtube.com/watch?v=6oiXV1Srg7E)
* [Checking AirBag firing lines](https://www.youtube.com/watch?v=zTiqUaWeuT0)
* [Clearing Airbag DTC](https://www.youtube.com/watch?v=oQ3WcKlsvrw)
* [Can bus sniffing (Russian)](https://www.youtube.com/watch?v=SjDC7fUMWmg)
* [ECU Parameters changes](https://www.youtube.com/watch?v=i9VkErEpoDE)

## Troubleshootings

### No serial connection

* Linux : Check user rights to access serial port [Ubuntu](https://askubuntu.com/questions/58119/changing-permissions-on-serial-port)
* Windows :
  * Check serial drivers installation
  * Try to disable antivirus software

## Informations


Bugtracking here : [Issues](https://github.com/KarelSvo/ddt4all-5.6.0/issues)

Happy CAN-Hacking :)



