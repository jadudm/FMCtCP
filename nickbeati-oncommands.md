## [Three Programs Three Paragraphs](https://nickbeati5.wordpress.com/2018/03/13/three-programs-three-paragraphs/)

I decided to look further into specific “on” commands in makecode. These are specific actions made by the user to affect the CPx. Coming up with some of these “on” commands was a big challenge in our interdisciplinary group the last couple weeks, so I wanted to look deeper into these topics to increase my limited programming knowledge.

-   **Clap Light**

The simplest program I could think of for this topic is a clap light. Even though this is a very simple program, the concept of clapping to turn something on has become a popular phenomenon. The Clapper, Clap on! Clap off! is an invention made to turn lamps on and off with the clap of your hands. The block that I used for the clap light was “on loud sound”. I chose to use white as the color for the light and set brightness to the max value of 255. This is illustrated in the screenshot below and I will talk about it in my video demonstration as well.

[https://makecode.com/_27P5DHT9r89s](https://makecode.com/_27P5DHT9r89s)

![Screen Shot 2018-03-12 at 7.05.38 PM.png](https://nickbeati5.files.wordpress.com/2018/03/screen-shot-2018-03-12-at-7-05-38-pm.png?w=660)

-   **Clap Light that automatically turns off**

For my slightly more complex program, I decided to create a clap light that turns off after 2000 ms. However, you can still get the light to come back on if you clap again. To do this, I used a pause loop in makecode inside the original "on loud sound" event. After the pause loop, I set all pixels to black to turn the lights off. Since there is a forever loop in the program, the clap light will continue to turn on if you clap but will turn off after 2000 ms every time.

[https://makecode.com/_gKJDvF6gxRDL](https://makecode.com/_gKJDvF6gxRDL)

![Screen Shot 2018-03-12 at 7.21.42 PM](https://nickbeati5.files.wordpress.com/2018/03/screen-shot-2018-03-12-at-7-21-42-pm.png?w=660)

-   **Clap On! Clap Off!**

For my third program, I tried to see if I could come up with a code to duplicate The Clapper as seen on TV. To do this, I had to incorporate a couple more complicated topics in makecode. I used some of my same code from the previous two codes, but used an “if, then” statement and an “on start” event block. I also created a new variable, which I called "light." I set this variable to have a value of either 0 or 1. As shown below, I was able to successfully turn the lights on and off the CPx!

[https://makecode.com/_LDrHyPAxjVdV](https://makecode.com/_LDrHyPAxjVdV)

![Screen Shot 2018-03-12 at 7.38.29 PM.png](https://nickbeati5.files.wordpress.com/2018/03/screen-shot-2018-03-12-at-7-38-29-pm.png?w=660)

Lastly, I decided to include my Loom video that I created for all three of my programs. Hope you enjoy watching and learn some about makecode!!

[https://www.useloom.com/share/ac57f27dc9bf4a1d95f1a1d5646dd6de](https://www.useloom.com/share/ac57f27dc9bf4a1d95f1a1d5646dd6de)

# **From Makecode to Python**

In order to convert this file from make code to python, I needed to change on loud sound to if button A was pressed. This is due to the fact that python is unable to account for a loud sound. 

## Clap Light
First, in order to use the CPX functions I imported the dcs file.
~~~
from dcs import* 
~~~
Next,  I needed to use an event. In python, this is accomplished by using a while true loop. 
~~~
while True:
~~~
Since we are inside a while true loop, it is important to add whether or not a button was pressed during this time. For my initial program in make code, this program was designed for a clap light, so I used the "on loud sound" command, but in python, clicking a button is an alternative. 
~~~
if(isPressed(BUTTONA)):
~~~
Finally, I wanted to include an extremely bright white light for this clapper, so I set brightness to the max value of 100 and all the red, green, and blue pixels to 255, making the light white.
~~~
setBrightness(100)
setAllPixelsToRGB(255,255,255) 
~~~
This completes my basic program for the clap light.

## Clap Light that automatically turns off

For this slightly adapted version of the clap light that conserves energy by automatically turning off, I used much of the same code in python. The only exception is I added a pause after the bright white light illuminates. I set this to 2000 ms. 
~~~
pause(2000)
~~~
Next, I had to set the red, green, and blue pixels to zero in order to turn off the light.
~~~
setAllPixelsToRGB(0,0,0)
~~~

## Clap On! Clap Off!
First, I needed to have the button act like a toggle. In order to do this, I created a variable named "light" and placed it at the top.
~~~
light = 1
~~~
Next, after the if(isPressed(BUTTONA)), I included:
~~~
if(light):
	setBrightness(100)
	setAllPixelsToRGB(255,255,255)
	light = 0
~~~
This changed the brightness and set the pixels to white like before. However, at the end, I toggled light to zero. Now, I can include an else statement.
~~~
else:
	setAllPixelsToRGB(0,0,0)
	light = 1
~~~
Therefore, the light will react to the button, then check to see if the light is already on, and either turn on or off.

