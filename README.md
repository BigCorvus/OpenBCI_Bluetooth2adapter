# OpenBCI_Bluetooth2adapter
Eagle files for an adapter board for the OpenBCI 32bit V3 board (Cyton) that enables higher data/sampling rates and eliminates the need for a USB dongle. The bluetooth module used is the common HC-05. Programming the board is still accomplished via dongle/RFduino.


In order for this board to work you have to implement WinslowStrong's changes in firmware (https://github.com/WinslowStrong/OpenBCI_Wired_USB) and you have to set up a baud rate of 230400baud on your bluetooth module (this is the highest rate I've been able to acheive reliably with the HC05). 
I've modified my Cyton board by putting the RFduino module on headers so that it can be removed after flashing the modified firmware. 

A solder jumper is included on the bottom side of the board to enter programming mode. You can short it temporarily using some metal object. Check out the HC-05 datasheet to find out about the commands.
