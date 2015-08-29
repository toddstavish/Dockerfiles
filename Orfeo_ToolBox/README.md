Orfeo Toolbox(OTB) is an open-source C++ library for remote sensing images processing.


docker run -i -t \

-v $HOME/Data:/home/data \ <- mounts data directory to container

toddstavish/orfeo_toolbox \

otb_cli_gui executable <- otb command and parameters [defaults to shell]

GUI Config:

Linux ->

-v /tmp/.X11-unix:/tmp/.X11-unix

-e DISPLAY=unix$DISPLAY

OSX ->

XQuartz

socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\” and

-e DISPLAY=192.168.99.1:0 <- this the default virtualbox interface ip address

Example CLI (with parameters):

docker run -i -t \

-v $HOME/Data:/home/data \

toddstavish/orfeo_toolbox \

otbcli_ComputeImagesStatistics \

-il /home/data/OIRDS_v1_0/DataSet_1/22042086_1531_256_1786_511.tif \

-out /home/data/out.xml
