Opticks is an expandable remote sensing and imagery analysis software platform.


docker run -i -t \

-v $HOME/Data:/home/data \ <- mounts data directory to container

toddstavish/opticks

GUI Config:

Linux ->

-v /tmp/.X11-unix:/tmp/.X11-unix

-e DISPLAY=unix$DISPLAY

OSX ->

XQuartz

socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\” and

-e DISPLAY=192.168.99.100:0 <- this the default docker interface ip address
