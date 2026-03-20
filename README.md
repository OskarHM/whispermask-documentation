# Documentation of the whisper mask project

The communication of the two raspberies should be based on avahi. 
The rapsberry controlling the User Interface is reachable under this address: 
whisperMask.local
password: swhiscool

The raspberry controlling the Translation is reachable under this address: 
siemens-display-whisper-mask.local
password: swh

## Starting the User Interface
We have the most recent version already built on the raspberry Pi. 
sudo ./demo -D13 --led-no-hardware-pulse --led-cols=96 --led-rows=48 --led-pwm-lsb-nanoseconds 130 --led-pwm-bits=11 --led-brightness=100 --led-slowdown-gpio=4 starts the demo session and the D13 is our program the moving mouth waiting for MQTT start command

We decided to integrate it inside the library so we can contribute it upstream because the mouth is a cool demo. D13 selects our demo case.


## Starting the controller and translation service
The siemens-display-whisper-mask.local has all dependencies already installed. You just need to source the virtual environment and run the python script.
