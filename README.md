Download Link: https://assignmentchef.com/product/solved-cs224-lab-5-mips-lite-pipelined-processor
<br>
Preliminary Report/Preliminary Design Report: Pipeline hazards evaluation and preparing test modules in MIPS (Due date of this part is the same for all).

Implementation and simulation of the MIPS-lite pipelined processor.

<ol>

 <li>Please drop your written Preliminary Design Report into the box provided in front of the lab by 10:40 am. No late submission!</li>

</ol>

<strong>DUE TIME OF PART 2—DIFFERENT FOR EACH SECTION:</strong>

<ol>

 <li>You have to demonstrate your Part 2 lab work to the TA for grade by <strong>12:15</strong> in the morning lab and by <strong>17:15</strong> in the afternoon lab. Your TAs may give further instructions on this. If you wait idly and show your work last minute, 20 points may be taken off from your grade.</li>

 <li>At the conclusion of the demo for getting your grade, you will <strong>upload your lab work</strong> to the Unilica Assignment, for similarity testing by MOSS. Please see the related section below for further instructions on MOSS submission.</li>

</ol>

<strong> Preliminary Work / Preliminary Design Report </strong>

At the end of this lab, you will have implemented the pipelined MIPS architecture that can be seen in the file that is provided as <strong><em>PipelineDatapath.PNG</em></strong> (Notice that there is no early branch prediction in this pipeline. Hence, the branch resolution is done in the <span style="text-decoration: line-through;">Execute</span> Decode stage.). Note also that there is no jump instruction implemented as well. Be sure to have a printout of the pipelined processor with you, to use during the lab. Your PDR should contain the following items:

<ol>

 <li>a) Cover page, with university name, department name, and course name and number at the top, “Preliminary Design Report”, Lab # (e.g. 5), Section #, and your name and ID# in the middle, and the date of your lab at the bottom.</li>

 <li>b) <strong> </strong>The list of all hazards that can occur in this pipeline. For each hazard, give its type (data or control), its specific name (“compute-use” “load-use”, “load-store” <span style="text-decoration: line-through;">“J-type jump”</span>, “branch” etc.), the pipeline stages that are affected.</li>

 <li>c) For each hazard, give the solution (forwarding, stalling, flushing, combination of these), and explanation of what, when, how.</li>

 <li>d) <strong> </strong>The logic equations for each signal output by the hazard unit, as a function of the input signals that come to the hazard unit. This hazard unit should handle all the data and control hazards that can occur in your pipeline (listed in b) so that your pipelined processor computes correctly.</li>

 <li>e) <strong> </strong>Write small test programs, in MIPS assembly, that will show whether the pipelined processor is working or not. Each of your test programs should be designed to catch problems, if there are any, in the execution of MIPS instructions in your pipelined machine. Write:</li>

</ol>

<ul>

 <li>A test program with no hazards (to verify that there are no problems with the connections in your pipeline etc.)</li>

 <li>A test program that has one type of hazard, and another, and another…</li>

</ul>

In the end, have at least 4 test programs (testing at least 3 hazards) with their machine code (in hex).

<em>You can use the student-written assembler tool available online to help you quickly implement your test programs<a href="#_ftn1" name="_ftnref1"><strong>[1]</strong></a>.  Remember that the goal of testing is to verify that all the instructions are fully working, <u>and</u> that all the instructions are working even in the presence of hazards.</em>

<strong>Part 2:  Implementation and Simulation</strong>

<ol>

 <li>a) You are given a skeleton System Verilog code for your pipelined MIPS processor in the file <strong><em>txt</em></strong>. The places in the code that needs to be modified are shown with comment blocks above them. Fill them to implement Pipelined Processor. You don’t need to follow the skeleton code point by point. If you think your design is better, you are welcome to try it in your code, as long as your version of the code works, too.</li>

 <li>b) Now make a System Verilog testbench file and using Xilinx Vivado, simulate your Pipeline Processor by executing the test programs you wrote at Prelim e). Implement a new top module in order to see memwrite, regwrite, writedata, pc, instruction and resultw signals. Study the results given in the simulation window. Find each instruction, and understand its values. Do this step for each of the test programs you wrote.</li>

 <li>c) When you have integrated all the System Verilog modules together and your whole pipelined MIPS is working in simulation with the test programs you wrote, call<u> the TA and show it for grade</u>. To get full points from this part, you must know and understand everything about what you have done.</li>

</ol>

<a href="#_ftnref1" name="_ftn1">[1]</a> <a href="https://github.com/bilkentCraps/mips">https://github.com/bilkentCraps/mips</a>