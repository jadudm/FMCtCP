# Lateness is Greatness: Midnight Runs with Code

So today I programmed a couple of things. I’ll take you through a few, pretty monotonous codes that I’ve done in the past day or so and describe my vision of how I can use them later. My first code involves the CPX and its use of sound and the second two are from the website trinket in which I draw two different types of Bates Bs.

The sound code I did for the CPX in make code is pretty easy. I take a “while true” loop and say that when the sound level reaches above a certain threshold, proceed with the command inside of that function. Inside the function I show a ring of blue lights , followed by a pause, then a light ring of blue lights, and then finally and increase in brightness. Now, when a loud sound is heard the CPX should light up in bright blue lights!

My next code is on a website called trinket which I’ve been messing around with recently. In this code I make a turtle which will serve as my drawing tool. I set the color to red… because why not. I use codes to draw circles and semicircles and other straight lines off of position I set. in the end I turn out with an outline of a fairly good looking Bates B.

My [final code](https://trinket.io/library/trinkets/185952ddc1) was the most complex. It was similar to the outline of the first Bates B but I take it and make thicker pens, different colors, start and end to fillings, a second turtle and different speeds. Although unsuccessful, I tried to use a position function to start a second turtle at the same position as my first turtle at a specific time. This could be useful in different ways of using the CPX. In the end, I turn out with an even better looking Bates B while using many more lines and ideas.

[Here I’ll show you how I did it!](https://www.useloom.com/share/df9464389018456080776b7097bd3f3c)


ADDING ON

 All was going smoothly! Or so I thought...🤦



Written by  [PRESTONHAUGH]
All was goinG smoothly, or so I thought. I started off working on this program but was unable to work on in throughout the day because of a clerical error in which the "lib" folder  displayed "lib-5." Who knew a simple 5 could stop an entire program from working.
	Thereafter, I took off! I took inspiration from Matt's YouTube post about acceleration and went to work. After setting all three of the axis variables equalled to zero I concentrated on one of them. I took the X axis and, after retrieving the acceleration from it, set each half of the lights on the CPX to different colors. I provided two different ways to do this. First, I used a range and an index to choose my colors specifically. Another, I named out all 10 pixels and set them to a certain color and a certain brightness (in this case RED.)
	My ultimate goal was to take each of the axis (X, Y, Z) and collect their measurements incrementally. At this point the 3 numbers would be summed. According to the sum the CPX would light up in different arrays or combinations.
	Alas, my CPX took a turn for the worst. It delivered one mighty beam of light. It shone one last awesome spectacle before dying out to  permanently shine a dull, lifeless red that Xbox fanatics might equate to the feared Red Ring of Death. My computer showed one daunting message "unplug USB device using to much power."
	I tried in vain to save it. After going through the process of erasing everything from the CPX it still did not work. The red light did not persist, however the CPX failed to use any actionable functions drawing from the DCS Rosetta Stone platform or any others (including the example program). 
	
Here is the program that was successfully working before it crashed for some reason. I figured it better to turn in the code that I know will actually run then submit the code that is, while more in depth, more uncertain due to aforementioned circumstances... I will add the next python code to my next post.

from dcs import *

#set variables equal to 0
accel_reading_x = 0 
accel_reading_y = 0
accel_reading_z = 0

#on start 
while True:
    
    # reading for AXIS
    accel_reading_x = getAccel(XAXIS)
    accel_reading_y = getAccel(YAXIS)
    accel_reading_z = getAccel(ZAXIS)
    print(accel_reading_z) 
    
#set lights to colors based on sensor reading  
#set lights 1-4 for XAXIS
    if accel_reading_x < 5:
        """for i in range(0, 5):
            setPixelRGB(i, GREEN)
        for i in range(5, 10):
            setPixelRGB(i, BLUE)"""
        setPixelRGB(0, 255, 0, 0)
        setPixelRGB(1, 255, 0, 0)
        setPixelRGB(2, 175, 0 ,0)
        setPixelRGB(3, 175, 0, 0)
        setPixelRGB(4, 150, 0, 0)
        
    elif accel_reading_x < -5:
        for i in range(0, 5):
            setPixelRGB(i, GREEN)
    else:
        setBrightness(5)
        setPixelRGB(i, BLUE)
        #
        #
        #
        # lights 5-6  ZAXIS
    if accel_reading_z < 5:
        for i in (5, 6):
            setPixelRGB(i, WHITE)
        setPixelRGB(5, 0, 200, 0)
        setPixelRGB(6, 0, 200, 0)
        
    elif accel_reading_z < -5:
        setBrightness(25)
        setPixelRGB(5, 0, 200, 0)
        setPixelRGB(6, 0, 200, 0)
        
    else:
        setBrightness(5)
        setPixelsRGB(i, RED)
        #
        #
        #
        # lights 7-10 YAXIS 
    if accel_reading_y < 5:
        setPixelRGB(7, 0, 0, 255)
        setPixelRGB(1, 0, 0, 255)
        setPixelRGB(2, 0, 0, 175)
        setPixelRGB(3, 0, 0, 175)
        setPixelRGB(4, 0, 0, 150)
    elif accel_reading_y < -5:
        for i in range (0, 5):
            setPixelRGB(i, GREEN)
    else:
        setBrightness(5)
        setPixelRGB(i, BLUE)
