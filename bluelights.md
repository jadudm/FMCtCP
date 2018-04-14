# Simple Python Program
I originally tried to translate my claplight program into python but after countless attempts I was still unable to get it to work. After this failure I decided to take a step back and attempted something easier. I just wanted to use python to turn the CPX lights a certain color and brightness. While this code is extremely simple, I still managed to have technical difficulties. It seems like every time I leave Python or unplug my CPX I mess something up and have to start from scratch, the codes I make only working on the CPX 50% of the time. Here is my attempt to make the CPX to show blue lights. 

## Makecode version
On makecode this program is easy and it definitely [works](https://makecode.adafruit.com/#editor).
The on start block signals the CPX when to begin the code. Within the on start block is a set brightness function to set the brightness of the pixels. I set it very low, at 4. Following this is a logic function in which the "if true" command is replaced with "button A is pressed". Within the logic function is the set all pixels to blue command which, of course, sets all the pixels to the color blue. 

## Python translation
On python this simple code is far more complex. Syntax matters, punctuation matters, spacing matters; it is truly a language. I did my best to translate it, but again had many technical difficulties which prevented me from seeing if it actually works on the CPX. This is what I came up with by going through the dcs library and the library on the adafruit website and trying to weave together bits and pieces. I also looked at the java script translation of my makecode creation and tried to translate that into python since it is more similar. 

	> from dcs import *
	# On Start 
	setup_pixels(brightness = 4)
	if was_pressed(BUTTONA):
    set_pixel(red = 0, green = 0, blue = 4)
