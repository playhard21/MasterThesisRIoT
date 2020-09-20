# This Repository is to manage code for my MasterThesis
## Code Generation and Management
### RIoT basics

[RIoT os](https://www.riot-os.org/) HomePage \
RIoT os [Tutorials](https://github.com/RIOT-OS/Tutorials/blob/master/README.md) \
Boards Used for work
```
arduino-mega2560
nucleo-f767zi
ESP8285

```
working machine details
```
System:    Host: aki-linux Kernel: 4.15.0-52-generic x86_64 (64 bit) Desktop: Unity 7.4.5
           Distro: Ubuntu 18.04.5
Machine:   System: LENOVO (portable) product: 20354 v: Lenovo Z50-70
           Mobo: LENOVO model: Lancer 5A5 v: NANANANANO DPK Bios: LENOVO v: 9BCN25WW date: 04/10/2014
CPU:       Dual core Intel Core i5-4210U (-HT-MCP-) cache: 3072 KB
           clock speeds: max: 2700 MHz 1: 1712 MHz 2: 1589 MHz 3: 1396 MHz 4: 1630 MHz
```


### Steps


```
mkdir RIoTCode
git clone https://github.com/playhard21/MasterThesisRIoT
```

### Shortcuts
#### RIoT os

```
make term BOARD=nucleo-f767zi \\ goes into the board
make all flash term  \\ flash the code into board
make all term - \\ compile the code and makes a dic in bin/

```

#### linux and Tools used
##### Pyterm
This is an interface between linux terminal and software installed on board
```
reboot //reboots the Board System
/exit  // exists form board
```
Arguments \
-p Port which is connected to BOARD\
-b baud Rate

##### avrdude
This install .hex files on arduino Boards \
Arguments\
-c programmer-id\
-C config-file \
-D Disable auto erase for flash\
-p arduino product part number \
-P port to which board is connected \
-U flash: // path to .hex file

```

lsusb  //to list all the connected poarts

PathForPyterm -- RIoT/dist/tools/pyterm/pyterm -p Port'/dev/ttyACM0' -b BaudRate '9600'

avrdude -c stk500v2 -p m2560 -P /dev/ttyUSB0 -D -U flash:w:/home/aki/Desktop/Tutorials/task-01/bin/arduino-mega2560/Task01.hex


```
