
## Lucy Does DCS Loops

**This second video I am making connects motion to computing, harkening on what we learned in our dance, music, and computer integrating project. I will simplify one of the programs I used for our dance project and explain its intricacies. The YouTube Link for my video is [here](https://www.youtube.com/watch?v=hnMEqHT9BK4)**


## Firstly

****First, there is an “on start” block here. This shows that when the program begins, it identifies that a variable to start is the accelerometer on the “x-axis” which measures movements on the x-axis of a graph, moving side to side.****


## Secondly

Now, I will discuss the (arguably) easiest part of this program. Loops. The “forever” block shows that when this program begins, whatever is within the block will go on forever when those conditions are met. The CPx will regularly monitor the movement. Everyday it is true, it will continue to loop back around until the conditions aren’t met. In this case, the conditions of the first forever block is that whenever there is little to no movement on the x-axis, the CPx will show light purple colors.

## Thirdly

****Lastly, we can see that when this condition isn’t met we must remember I have established three total forever loops in total. This means that if the acceleration ranges are not small (and therefore not light purple) the program will automatically check where in which the acceleration falls to make the statement true.****

## Quiz!

Here’s a quick test to see if you've gotten a handle of this concept of loops measuring the x-axis. The answers are provides at the end of transcript written under the link to the video.

  

1.  If the acceleration is measured at 500 at what color will the pixels be set to? Light normal or dark purple? Normal purple
    
2.  If the acceleration is measured at zero at what color will the pixels be set to? Light normal or dark purple? Light purple
    
3.  If the y-axis is measured at 600 at what color will the pixels be set to? Light normal or dark purple? Trick question - our on start loop established us to measure the acceleration with the x-axis only
    

Bonus question - Which of these three loops will go on forever? All of them
