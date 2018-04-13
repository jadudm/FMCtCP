## [Three Programs Using Loops](https://nicklynch10.wordpress.com/2018/03/13/3-new-programs-and-how-to-make-them/)

We have been working hard in DCS and after we finished out performance we got right back to work. Our next assignment is to build three more programs on a concept we did not understand fully. I decided to pursue loops. A loop involves iterating through a process to change something. In this example, I use loops to interate through the different pixels and change the pixels color. 

### Basic Loops

The first program I decided to build was a basic loop that changes the active index light to red. This is a simple program that shows visually how a loop will work. It chooses an index, runs the action then goes to the next index until it is at the maximum value you chose. The program could be applicable to a child who wants to interact with a machine with simple buttons.

[https://makecode.com/_JjpFYt0X8ER8](https://makecode.com/_JjpFYt0X8ER8)

![capture.png](https://nicklynch10.files.wordpress.com/2018/03/capture.png)

### Advanced Loops

Next, I decided to add something a little more advanced. I noticed it was very easy to create a forward moving loop, however a backwards moving one required some extra effort. In order to make a backwards for loop I needed to start another variable at 10. Then each half second subtract 1 from the index and run the loop again. I needed the code to know when to stop, so I created a logic block for when a variable is greater than 0. This would mean the loop would stop at 0.

![capkture.png](https://nicklynch10.files.wordpress.com/2018/03/capkture.png)

 

### A Different Way

Lastly, to test my understanding of loops, I decided to create the exact same loop using a different method. This time however, I used a clever math trick to use the same basic for loop provided for us to get the same results as the backwards loop. I utilized the fact that I knew there are only 10 lights and by having a forward moving index (1,2,3…) I will get a backwards index by simply doing 10 – (1,2,3…) = 9,8,7… This is exactly the same as the program before but in a different way. This showed me that the program could be made using many different techniques and no two techniques are exactly the same.

 

![capturdde.png](https://nicklynch10.files.wordpress.com/2018/03/capturdde.png)

 
I believe the fact that the two methods are completly different yet contain the exact same result is interesting. Programming often has many roads that travel to same destination and this is a clear example of such.
Below is a video I made demonstrating how I built the final product. I am far from a film major so please be sparing with the harsh reviews.

[https://www.useloom.com/share/13a250e756254dceb93777e43255dd84](https://www.useloom.com/share/13a250e756254dceb93777e43255dd84)


# Python Mode
Next, I created the same program except this time it is using python. We begin with the simple program.
## Simple Program
First, in order to use the CPX functions I imported the dcs file.
~~~
from dcs import *
~~~
Next, I initialized the variables. I wanted to set up the pixels as the color red. 
~~~
setUpPixels()
setAllPixelsTo(RED)
~~~
The next part I needed to use an event. However, in Python this is done using a While True loop.
~~~
while True:
~~~
This while true loop runs until time itself runs out. So the next step would be to if at all during this time, was a button pressed?
~~~ 
if(isPressed(BUTTONA)):
~~~
Next, we want to run through a for loop that changes each pixel to green. 
~~~
for(i in range(0,10)):
~~~
This for loop causes the program to iterate through 10 times, from 0 to 9.  Now that we have a number that moves through 0 to 9, we can use that as our pixel index. 
~~~
setPixedRGB(i,0,255,0)
~~~
The numbers represent green. Lastly, this would change all of the lights to green instantly. This is because programs run in nanoseconds, so we would not be able to comprehend that it looped through. 
~~~
pause(500)
~~~
The pause simply pauses the program for half a second. 

## Advanced Program
The next program I built completely builds off the last program. Using the code from part one, we now decide to add under the while true loop. I wanted to have the CPX react to button B as well.
~~~
if(isPressed(BUTTONB)):
~~~
Now, below this I start with the same for loop as earlier. However, I want to run a loop that runs backwards. Instead of starting at zero, I want to start at 9. I looked into the literature and found that the range function allows reverse loops using the following syntax. 
~~~
for(i in range(9,0,-1)):
    setPixedRGB(i,0,0,255)
    pause(500)
~~~

This concludes the second part of the program. Both loops will react to a button press, but one will go forward with a loop and turn green. The other will go backwards turning blue. 

## A Different Method
The different method I used on makecode still can work in python. Instead of changing the for loop, I changed the index.
~~~
for(i in range(0,10)):
    setPixedRGB(10-i,0,0,255)
    pause(500)
~~~
This does the exact same thing as the above code, but it does it in a very different way.
