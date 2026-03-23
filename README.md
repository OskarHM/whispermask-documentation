# Documentation of the whisper mask project
This is the central documentation repository for the whisper mask.

## User Interface
The code for the user interface (mouth) can be found here: https://github.com/OskarHM/rpi-rgb-led-matrix . It is a fork of the open source library: https://github.com/hzeller/rpi-rgb-led-matrix .
We have the most recent version already built on the raspberry Pi. 
The command to start the visualisation is: 
sudo ./demo -D13 --led-no-hardware-pulse --led-cols=96 --led-rows=48 --led-pwm-lsb-nanoseconds 130 --led-pwm-bits=11 --led-brightness=100 --led-slowdown-gpio=4 

We decided to integrate it inside the library so we can contribute it upstream because the mouth is a cool demo. D13 selects our demo case.


## Translation pipeline
The source code for the translation pipeline can be found here: https://github.com/OskarHM/api-based-translation . There is also a branch for an improved local_text_to_speech which we did not use in our prototoype. 
The siemens-display-whisper-mask.local has all dependencies already installed. You just need to source the virtual environment and run the python script.
The high level view can be found in the presentation:
![High Level Overview](doc/high_level_overview.png)

This diagram shows an overview of the text to speech pipeline: 
![Component Diagram Overview](doc/component_digram_overview.png)
This is a more in depth representation which is for persons that do not like to read code but want all the details(might take the same amount of time tough.)
![Component Diagram Technical](doc/component_diagram_technical.png)





## Communication
The communication and the remote development of the two raspberies is based on avahi. 
The rapsberry controlling the User Interface is reachable under this address: 
whisperMask.local
password: swhiscool

The raspberry controlling the Translation is reachable under this address: 
siemens-display-whisper-mask.local
password: swh
