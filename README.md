# OpenBCI_Bluetooth2adapter

![alt tag](https://github.com/BigCorvus/OpenBCI_Bluetooth2adapter/blob/master/OpenBCI%20Cyton%2032bit%20bluetooth%202%20adapter.jpg)

Eagle files for an adapter board for the OpenBCI 32bit V3 board (Cyton) that enables higher data/sampling rates and eliminates the need for a USB dongle. Reliable operation is possible with 500Hz and 8 channels or 250Hz and 16 Channels. The OpenBCI GUI 2.0 is able to keep up with that.
The bluetooth module used is the common HC-05. Programming the board is still accomplished via dongle/RFduino.


In order for this board to work you have to implement WinslowStrong's changes in firmware (https://github.com/WinslowStrong/OpenBCI_Wired_USB) and you have to set up a baud rate of 230400baud on your bluetooth module (this is the highest rate I've been able to acheive reliably with the HC05). 
I've modified my Cyton board by putting the RFduino module on headers so that it can be removed after flashing the modified firmware. 

A solder jumper is included on the bottom side of the board to enter programming mode. You can short it temporarily using some metal object. In command mode (the LED is blinking slowly) you have to set a baud rate of 38400baud 8N1 and send after each command \r\n. If you enter AT the module should respond with OK.
To set the baud rate just enter AT+UART=230400,0,0 and to set the name type in AT+NAME=OpenBCI32 or whatever name you like. 

Edit: I also created a version for the RN42 module (http://www.digikey.com/product-detail/en/microchip-technology/RN42-I-RM630/RN42-I-RM630-ND/6009311) which can acheive speeds at up to 460800 baud in the system. 
