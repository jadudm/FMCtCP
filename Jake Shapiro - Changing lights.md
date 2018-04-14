---


---

<p>Jake Shapiro</p>
<h2 id="exploring-with-input-commands-in-makecodepython-chapter-1">Exploring with Input Commands in MakeCode/Python: Chapter 1</h2>
<p>As an assignment for DCS 102, I chose to explore the Input commands in MakeCode, and again in Python. This assignment, which had two parts, required me to create two different sets of code and record two videos–one for each platform.</p>
<p>In the first video, covered in this chapter, I demonstrate how to create a code that changes the color display on the CPx dependent on the level of light detected by the light sensor on the CPx.</p>
<p>Here is a quick demo video describing three programs I have created in MakeCode, each of which shows a different way to control the lights on my CPx.</p>
<iframe width="560" height="315" src="https://www.youtube.com/embed/384QIi6YuY0?ecver=1" allowfullscreen=""></iframe></p>
<p>The first program is a pretty basic command that alternates the colors on my CPx between all red and red/blue. This was creating using a “forever” loop, a show ring (all red), and a show ring (red/blue) with pause commands placed between the two “show ring” commands. The second program is more complex and utilizes additional features within the MakeCode program. </p>
<p>My second program is designed to alternate the colors displayed on my CPx based on the level of light that is being picked up by my CPx’s light sensors. For this iteration, I used an “On button A press” loop to start. In the loop I used an “if/else” logic command to indicate that for light values less than 100, the CPS would set pixels to red, and for light values greater than 100, the CPx would set pixels to blue.</p>
<p>My last command achieves essentially this same result in a slightly different fashion. This time, I went back to using a “forever” loop, like in my first program and set all pixels to red. Instead of an “if/else” logic command, like in my second program, I just used an “if” command that would set all pixels to blue after button A was pressed.</p>

