
Simple Code

![alttext](https://andrewsdcsblog.files.wordpress.com/2018/04/screen-shot-2018-04-12-at-9-21-12-pm.png)


In my first successful code on Python, I decided to translate a similar code from Makecode. The simple code begins with the statement “from dcs import.” This was created by our class earlier in the semester to allow Python to recognize that “red” is actually the color red. This may sound simple but it saves a lot of time for programmers. Ultimately, I can do this for any color as you can see that I used “blue” in my program and Python recognized it. Then, I incorporated light_Sensor=0 to initialize the light sensor as a variable for the light sensor. Essentially, this will elicit a response from the light sensor when the condition is true in the loop. In makecode, the “while true” loop has a condition that evaluates to a boolean value. Like other boolean functions, the loop runs on the “all or nothing” principle.” The condition will run before the code, if it is true the code inside will run, but if it is false, then it will not run. In the while true loop the “if else” statement says: if the light level is equal to 180 then the CPX will elicit a color response of blue. It is very interesting to see how Python can turn the blocks of makecode into real written code.

from dcs import *

#On Start

light_Sensor=0

#Forever

While True:

light_Sensor=getLight

print(light_Sensor_reading)

if light_Sensor=180

setAllPixelsTo(BLUE)

  
  

Slightly More complex

  ![alttext](https://andrewsdcsblog.files.wordpress.com/2018/04/screen-shot-2018-04-12-at-9-23-19-pm.png)

The slightly more complex code is fairly similar to my first code, however, this introduces a new concept into python known as the “if else statement.” The “if else statement” can be represented in the sense that if the condition is true then the “if code” will run,” while if it is false then the “else” code will run. In my program, a prime example of the “if code” is “ if light sensor=180” then the CPX will elicit a response setAllPixelsTo(BLUE). Basically, if these conditions are not met, then the CPX will remain Green, which is the CPX under its normal conditions without any manipulation.

  
  
  
  
  

from dcs import *

#On Start

light_Sensor=0

#Forever

While True:

light_Sensor=getLight

print(light_Sensor_reading)

if light_Sensor=180

setAllPixelsTo(BLUE)

else

setAllPixelsTo(GREEN)

  
  
  
  
  
  

More Complex
![alt text](https://andrewsdcsblog.files.wordpress.com/2018/04/screen-shot-2018-04-12-at-9-25-02-pm.png)
In the final and more complex code I decided to challenge myself and work with accel readings over the x-axis. Unlike my first two codes my variable here is accel_Reading. Again I initialized the variable by setting the accel_Readng equal to 0. Under the while true condition, the code reads accel_Reading=getAccel(XAXIS). Simply, as Python reads the acceleration values, it prints the acceleration reading as the acceleration increases. For instance, when the CPX reads “the acceleration and the acceleration reading is greater than 4” then the pixels are set to blue because of the if statement. If it is less than 4, then the else statement turns the pixels on the CPX to the pre-manipulation condition color of green. In reality, this code will control whether the CPX will change from a pixel color of green to blue when an individual moves the CPX from left to right or in the x-direction with an accel reading greater than 4.

  

from dcs import *

#On Start

accel_Reading=0

#Forever

While True:

accel_Reading=getAccel(XAXIS)

print(accel_x_reading)

if accel_x_reading>4

setAllPixelsTo(BLUE)

else

setAllPixelsTo(GREEN
