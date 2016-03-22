# Introduction #

This only applies to those of you that want to use OLEDs with the phi-panel LCD backpack. The difficulty of using OLEDs on the backpack is that standard LCD library doesn't use the R/W pin so all LCD shields have this pin grounded. But Adafruit's OLED library relies on this pin. This tutorial guides you through the steps.

# Cautions #
First make sure you have the right hardware. Your backpack PCB must say V1.9. This is the circuit board version, which is different from firmware version.

If you try to remove a backpack from its LCD, without proper desoldering tool, you may damage the backpack or the LCD. You are strongly suggested to practice desoldering before attempting. You need to remove all solder from LCD pins so you can insert the OLED, a difficult task, even for myself ;). Better, you can get a backpack kit without LCD at inmojo.com

# Steps #
When you assemble a new kit for your OLED, just omit the potentiometer and the back light resistor (150ohm or 47ohm). If you are modifying your existing backpack, remove the back light resistor on the left side of the back pack, opposite the side that has the connection header for serial and power. Make sure you leave enough length of wire of the resistor when you cut if you decide to cut and suck the solder. Now remove the resistor.

Next step is to make sure that R/W pin is not going to be grounded. Make sure you solder headers on the OLED like you would for an LCD. Then locate the OLED pin 5, which is R/W, snip off the bottom part of the pin so it won't contact the backpack.

Now solder a wire between the OLED pin 5 and the lower pin of the back light resistor.

Once done, you can go ahead and follow the instruction on firmware upgrade on the other wiki page, pick one of the two modified firmware that says 1.6.4 and OLED, depending on your display size. These firmwares are for matrix keypads.

Good luck and if you have questions or want to share success stories with photos, leave them here or on my blog:
liudr.wordpress.com/phi-panel/

Alternatively you can modify the V1.9 backpack PCB as Kenny G. did. See pictures here:

http://liudr.wordpress.com/2013/01/03/using-oled-displays-on-phi-panel/