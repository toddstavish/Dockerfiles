QGIS is a free and open source Geographic Information System.

docker run -i -t \

-v $HOME/Data:/home/data \ <- mounts data directory to container

toddstavish/qgis

GUI Config:

Linux ->

-v /tmp/.X11-unix:/tmp/.X11-unix

-e DISPLAY=unix$DISPLAY

OSX ->

XQuartz

socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\” and

-e DISPLAY=192.168.99.1:0 <- this the default virtualbox interface ip address
