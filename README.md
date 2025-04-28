# ee271-lab-5-useful-components-solved
**TO GET THIS SOLUTION VISIT:** [EE271 Lab 5-Useful Components Solved](https://www.ankitcodinghub.com/product/ee271-lab-5-useful-components-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;99228&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE271 Lab 5-Useful Components Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Useful Components

</div>
</div>
<div class="layoutArea">
<div class="column">
Over the last 4 labs we’ve learned how to do most kinds of basic logic, but there are some standard elements that tend to come up over and over again. This lab will help you get some experience with them now, and add them to your toolkit in advance of the final project.

Design Problem – CyberWar

In the last lab we built a simple Tug of War game, and by now you’ve already crushed your room-mate into submission. Now it’s the hardware’s turn. Your goal is to develop a computer opponent to play against, as well as a scorekeeper that can show exactly how badly it beats you…

Counters

First off, take your lab #4 and replace the “winner” system with counters. Specifically, develop a 3-bit counter (holds values 0..7). It starts at 0, and whenever a “win” comes in to it, it increments its current value by 1. This is a simple FSM. Note that we assume once one player gets to 7 the game is over, so it doesn’t matter what happens when a player with 7 points gets one more.

Now, alter your lab #4 so that there is a counter for each player, which drives a per-player 7segment display with the current score for that player. Whenever someone wins, you increment the appropriate player’s score, then restart the game (i.e. automatically reset the playfield). Resetting the entire game will reset the playfield and score, while winning only resets the playfield.

LFSRs

To build a cyber-player, we need to create a random number generator to simulate the button presses. In hardware, the simplest way to do this is generally an LFSR (linear feedback shift register). It consists of a set of N D-flip-flops (DFF1…DFFN), where the output of DFFi is the input of DFFi+1. The magic comes in on the input of DFF1. It is the XNOR of 2 or more outputs of the DFF. By picking the bits to XNOR carefully, you get an FSM that goes through a fairly random pattern, but with very simple hardware (note that these LFSRs can never go into the state with all 1’s, but reach all others). Two examples are given below.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Figure 1. 3-bit LFSR

</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 2. 4-bit LFSR

First, draw the state diagram for these two circuits. It will show every possible state for the machine (8 for the 3-bit, 16 for the 4-bit), with arrows showing the next state they enter after that state.

Next, create a 10-bit LFSR in Quartus II and simulate it. You can find the list of bits to XNOR together in the table at the end of this lab (do NOT make up your own – most choices don’t work well, so the table shows the “best” connections to make).

ModelSim Tip: now that you are working with multi-bit signals, it can be helpful in ModelSim to display signals as decimal or hex values. To do this, right-click on a multi-bit signal in ModelSim, and select “Radix”.

Comparator

Develop a 10-bit comparator. The unit takes in two unsigned 10-bit numbers, called A and B, and returns TRUE if A&gt;B, FALSE otherwise. You can think about this as a subtraction problem, or just by considering the individual bits of the number themselves. CyberPlayer

We now have most of the components to implement a tunable cyber-player. First, let’s slow things down so you have a chance – run your entire Tug of War game off of the clock divider’s divided_clocks[15] (about 768Hz). To generate the computer’s button presses, compared the LFSR output (a value from 0…1024) to the value on SW[8:0] (a value from 0…511) – you can extend the SW[8:0] with a 0 at the top bit to make it a 10-bit unsigned value. If the SW value is greater than the LFSR value, consider this a computer button-press (i.e. the light should move one space toward the computer player’s end, assuming the human doesn’t make a move at the same instant). You can speed up or slow down the system by simply playing with the user switches, to see how fast you can go. If the clock is too fast, feel free to adjust to a different divided_clock output (for the ENTIRE design). Note: be sure that EVERYTHING that is clocked in your design (except for the clock_divider circuit) uses the same clock. If you use any other clock then strange things can happen.

ModelSim Tip: Yes, run EVERYTHING on the same clock. The big confusion you can have is running the testbench on the clk you provide to the DE-1 board (aka CLOCK_50), and run the logic design on the output of the clock divider. DURING TESTING OF THE WHOLE DESIGN, RUN THE USER DESIGN on CLOCK_50.

This will ensure the testbench and the circuit use exactly the same clock for testing.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
You will be graded on correctness, style, testing, testbenches, etc. Your bonus goal is developing the smallest circuit possible, measured in the same way as the previous labs.

Lab Demonstration/Turn-In Requirements

</div>
</div>
<div class="layoutArea">
<div class="column">
•

</div>
</div>
<div class="layoutArea">
<div class="column">
• •

</div>
<div class="column">
Demonstrate the lab on the DE1_SoC board in a video that shows the functionality of your project. Submit a short lab report that should include 3 main sections, detailed below.

Procedure

<ul>
<li>– &nbsp;Describe how you approached the problem and include state diagrams for all FSMs.</li>
<li>– &nbsp;Include a top-level block diagram for your entire design, showing the major modules andhow they are interconnected.
Results
</li>
</ul>
<ul>
<li>– &nbsp;Include screenshots of ModelSim simulation for all modules. You must have a testbenchfor every module in the project.</li>
<li>– &nbsp;Turn in a screen shot of the “Resource Utilization by Entity” page. Write the computedsize for your design.</li>
<li>– &nbsp;Describe what you tested in the simulation, and what the results in the screenshot show</li>
<li>– &nbsp;Give a brief overview of the finished project, compared to what was askedAppendix</li>
</ul>
– Include screen shots of your code

On Padlet, write about a problem you had in the lab and the fix to it, share a tip or trick you learned while working on the lab. You can also share an aha moment that you discovered while working on the lab. Avoid duplicating comments made by your classmates. NO videos for this padlet task, please use textual comments. The link to the padlet is here

Submit the SystemVerilog files (files with extension .sv). Make sure to follow the commenting guide provided. A significant amount of grade will depend on the commenting style.

Submit your report, video and programs to Canvas.

</div>
</div>
<div class="layoutArea">
<div class="column">
–

•

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Figure 3. LFSR taps [XAPP 052 July 7, 1996 (Version 1.1), Peter Alfke, Xilinx Inc].

</div>
</div>
</div>
