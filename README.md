Razer Hydra (Sixence) Driver to Linux (C++) with Python Interface using YARP communication.
by Dannier Castro L <danniercl@gmail.com>.

Part of code used in this project was taken from the SDK distribution of Sixense to control the Joystick RAZER HYDRA,
and distribuited as a Embedded Code under "End-User License Agreement For Use of Sixense Software" to a
End-User Product to help Developers of Python games can easily implement Razer Hydra controller.

This is from LINUX Operating System (Ubuntu/Debian) and implement a python application using YARP communication,
what allows to configure the handle-control to use the magnetic-position function.

Portions copyright © 2015 Sixense Entertainment, Inc. All rights reserved.

Instructions:

1) Download the Razer Hydra SDK Linux distribution from Sixence Official Web Page: http://sixense.com/linuxsdkdownload

2) Follow the instructions from "README.txt" file in SDK root directory to install the dependences so the program works on Linux OS.

3) Install YARP following this instructions https://wiki.arcoslab.eie.ucr.ac.cr/doku.php/installing_yarp_in_debian

4) Important Steps:

  4.a) Copy razer_linux_driver.cpp in directory ~/src/sixence_simple3d/progs/demos/sixense_simple3d

  4.b) Copy the 4 files in ~/src/sixence_simple3d/Eclipse/sixence_simple_3d_Release_x64
  
5) Enter the next commands:

   $ cd ~/src/sixence_simple3d/Eclipse/sixence_simple_3d_Release_x64

   $ make clean all
   
It may create a binary file called "razer_linux_driver" and enjoy to GAMES PROJECTS.

6) Give it execute properties:

   $ chmod +x ./razer_linux_driver

7) Run YARP: $ yarpserver3

8) Run binary file: $ ./razer_linux_driver

9) Run python file: $ python ./Razer.py

Obtain the position data in console first, later, implement and enjoy in your VIDEOGAME project.
