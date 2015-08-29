Monteverdi is a GUI application on Orfeo Toolbox(OTB), an open-source C++ library for remote sensing images processing.


docker run -i -t \

-v $HOME/Data:/home/data \ <- mounts data directory to container

toddstavish/monteverdi

GUI Config:

Linux ->

-v /tmp/.X11-unix:/tmp/.X11-unix

-e DISPLAY=unix$DISPLAY

OSX ->

XQuartz

socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\” and

-e DISPLAY=192.168.99.1:0 <- this the default virtualbox interface ip address
