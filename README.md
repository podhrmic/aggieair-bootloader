------------------------------------------------------------------------------
# README
------------------------------------------------------------------------------
This project provides Luftboot bootloader for Lisa MX (STM32F4 chip).


## HOWTO
--------------
From the root directory hit ``make``
That will compile all files you need. Then go to ``examples/stm32/f4/krooz/usb_dfu`` 
and flash usbdfu.bin to the autopilot using Eclipse or arm-none-eabi from command line.

Voila, then you can flash code on your autopilot via DFU!

## Using arm-none-eabi-gdb
```make
cd examples/stm32/f4/krooz/usb_dfu
arm-none-eabi-gdb usbdfu.bin
target extended-remote /dev/ttyACM0
monitor swdp_scan
attach 1
monitor vector_catch disable hard
set mem inaccessible-by-default off
monitor option erase
set print pretty
load
```

And then it should blink...
