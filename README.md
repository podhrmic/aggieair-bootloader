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
