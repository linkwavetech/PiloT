## The purpose 
Document a method of automatically managing the wwanX interface provided by the PiloT 
HAT board when used with a Raspberry PI and Raspian

## The method
Use Linux NetworkManager to provide automatation of the Pilot cellular modules 
IP interface bringup in Linux

For some documentation on NetworkManager --- https://wiki.debian.org/NetworkManager

## To install
[Read this](./instructions_howToInstall_AutoPiloT.md)

## Connection start 
If the connection configuration has setting   
```
autoconnect=true
```
Then the module just needs to be turned on with *pilotOn.sh* for NetworkManager to 
automatically connect the PiloT to wwanX

## To Configure and Play
Either via the graphical interface or using the command line nmcli and nmtui  

Note that the graphical interface has a database of general cellular networks.  
But to configure manually use nmcli or manually edit the files on the RPi system - 
for example to change the APN / add PAP / CHAP / USER / PASSWORD ...  

Note that the interface can be set to auto connect  

## Actual connection data looks like this
```
root@raspberrypi:/etc/NetworkManager# ls system-connections
'3 Internet.nmconnection'
```

[see](./exampleNetworkManagerConfigFile.md)

## Tested on 
(uname -a)
Module HL7692
RPi4 -- Buster -- Linux raspberrypi 4.19.58-v7l+ #1245 SMP Fri Jul 12 17:31:45 BST 2019 armv7l GNU/Linux
