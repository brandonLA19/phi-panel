# Introduction #

This page contains information regarding how to update your phi-panel firmware in order to take advantage of the latest development of the phi-panel.

# Update #

12/16/2012
I have developed a simple firmware erase code so you can load this code with the XLoader and then load a new firmware.

# How to start #

First, power your panel to find out what version of firmware you have. Please don't connect the panel to anything except for 5V and gnd.

Next, browse the downloads section to see if a newer version of firmware for your panel is available. Make sure you download the file for the right size of LCD.

Take you arduino UNO, remove the ATMEGA328 chip so the rest is just support chips and the TTL serial converter.

Connect the panel to the power and ground, TX to TX, and RX to RX, reset to reset.

Please disconnect the keypads/rotary encoders or other button arrangement when uploading new firmware that uses a DIFFERENT keypad layout to prevent shorting. If you are going from say matrix keypad to rotary encoders, you will likely short your pins if you forget to remove your keypad.

Open up arduino and open the serial monitor to 19200 bps (or your panel's current baud rate).

Type in something on the serial monitor to see if the panel will display it on the LCD. This makes sure you got the right connection. If not, you may have swapped the RX and TX.

Download the XLoader software from http://xloader.russemotto.com/ and extract it to your hard drive.

Make sure your arduino serial monitor is closed.

Using the XLoader, choose UNO, 115200 upload speed and the correct serial port for your UNO, first load the firmware erase to erase the original firmware. Here is the link to firmware erase:

http://code.google.com/p/phi-panel/downloads/detail?name=firmware_erase.hex&can=2&q=

After seeing "Firmware erased" message on the LCD, choose the firmware from download area, and upload with XLoader again.

If the panel restarts in about a minute with new firmware version on its LCD, congratulations, you have just updated your panel firmware.

If you keep having trouble with a new firmware, leave some comments, check whether you got the correct firmware for your hardware and key layout. If the above didn't work, try to upload a past version of the firmware, make sure it works, and try to upload the new firmware again.