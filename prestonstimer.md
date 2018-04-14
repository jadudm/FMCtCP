# Here’s What We’ve Been Up To



Written by  [PRESTONHAUGH](https://prestonsblog2021.wordpress.com/author/prestonhaugh/)

Despite variable blog posts, DCS has gone on! We recently completed a project in which we (the programmers) collaborated with musical groups and composers as well as a dancer to create a dance performance that integrates our CPX as well as the other group’s dance and musical components. Here I’ll show you some of the things that I’ve learned.

[Here](https://makecode.com/_8qY23jKk49Fx) I have a simple code aimed at changing colors when the “roll” of the CPX changes. This same code can be used with “pitch” as well but this one in-particular specifies in only controlling the lights as the CPX “rolls” left and right on its axis. At the start I set all of my pixels to white just to signal that the CPX is on and the code is running. I then used the “on tilt right” and “on tilt left” inputs to change the colors. When my CPX tilts right the pixels turn blue and when it tilts left it turns yellow.

My next code is a timer that I originally stole from the tutorials on makecode but have become proficient in making myself. The timer sets a proton to move forward one pixel on the CPX whenever the A button is pressed. On a “loud sound” the photon flips directions and begins counting down. At the end, flashy lights go off.

You can watch how I make this  [basic timer](https://www.useloom.com/share/185aa3763df74d5093debf706922042d) on makecode through this link.

Since I originally made the timer [I have added](https://makecode.com/_1t4ED5hXtKX2)  a function to clear all previous animations, created a song, made a tune play on the start, changed the brightness of some of the lights and changed the pixel color at the beginning.

ADDING ON!!!

Following my last code that worked but was not functional I created a code in which I imagine would work if my CPX had not crashed one me. This code is set to potentially find the acceleration of each of the axis and then find the sum of all three from which it assigns specific lights to be used with specific colors as well. If I were to add to this program I would add a timer function so that the sum function I use will be used every 30 seconds or so as to allow for interaction with the CPX in between. 



from dcs import *
import math *

# set variables equal to 0
accel_reading_x = 0 
accel_reading_y = 0
accel_reading_z = 0


def find_readingX(accel_reading_x):
    accel_reading_x = getAccel(XAXIS)
    return accel_reading_x
    
def find_readingY(accel_reading_y):
    accel_reading_y = getAccel(YAXIS)
    return accel_reading_y
    
def find_readingZ(accel_reading_z):
    accel_reading_z = getAccel(ZAXIS)
    return accel_reading_z)
    
def dolights(sum):
    sum = str(accel_reading_x + accel_reading_y + accel_reading_z)


# on start 
while True:
    
    # reading for AXIS
    accel_reading_x = getAccel(XAXIS)
    accel_reading_y = getAccel(YAXIS)
    accel_reading_z = getAccel(ZAXIS)
    print(accel_reading_z) 
    
# set lights to colors based on sensor reading  
# set lights 1-4 for XAXIS
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
        
        # lights 7-10 YAXIS 
    if accel_reading_y < 5:
        setPixelRGB(7, 0, 0, 255) 
        setPixelRGB(8, 0, 0, 255)
        setPixelRGB(9, 0, 0, 175)
        setPixelRGB(10, 0, 0, 175)
        
    elif accel_reading_y < -5:
        for i in range (0, 5):
            setPixelRGB(i, GREEN)
    else:
        setBrightness(5)
        setPixelRGB(i, BLUE)
     # if the sume of the axis readings is less than 25 set lights  
    if dolights < 25:
        setPixelRGB(0, 255, 0, 0)
        setPixelRGB(1, 255, 0, 0)
        setPixelRGB(2, 175, 0 ,0)
        setPixelRGB(3, 175, 0, 0)
        setPixelRGB(4, 150, 0, 0)
        setPixelRGB(5, 0, 200, 0)
        setPixelRGB(6, 0, 200, 0)
        setPixelRGB(7, 0, 0, 255) 
        setPixelRGB(8, 0, 0, 255)
        setPixelRGB(9, 0, 0, 175)
        setPixelRGB(10, 0, 0, 175)
     # if the sume of the axis readings is less than 30 change lights    
    if dolights < 30:
        setPixelRGB(7, 255, 0, 0)
        setPixelRGB(8, 255, 0, 0)
        setPixelRGB(9, 175, 0 ,0)
        setPixelRGB(10, 175, 0, 0)
        setPixelRGB(1, 150, 0, 0)
        setPixelRGB(2, 0, 200, 0)
        setPixelRGB(3, 0, 200, 0)
        setPixelRGB(4, 0, 0, 255) 
        setPixelRGB(5, 0, 0, 255)
        setPixelRGB(6, 0, 0, 175)
    # if the sume of the axis readings is greater than 30 rotate the lights    
    if dolights > 30:
        setPixelRGB(3, 255, 0, 0)
        setPixelRGB(4, 255, 0, 0)
        setPixelRGB(5, 175, 0 ,0)
        setPixelRGB(6, 175, 0, 0)
        setPixelRGB(7, 150, 0, 0)
        setPixelRGB(8, 0, 200, 0)
        setPixelRGB(9, 0, 200, 0)
        setPixelRGB(10, 0, 0, 255) 
        setPixelRGB(1, 0, 0, 255)
        setPixelRGB(2, 0, 0, 175)
