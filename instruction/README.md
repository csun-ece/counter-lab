# Clock and Sequential logic
**California State University, Northridge**  
**Department of Electrical and Computer Engineering**  

## Objective

After completing this assignment, students will be able to:
- Create sequential logic under clock
- Create asynchronous reset
- Implement different digital counters

## Requirements

- Vivado 2019.1
- Git

## Introduction
In this lab we will create different 4 bit counter using clock and sequential logic.

## General requirements:
- All counters will run under a simulated clock and will have asynchronous reset.
- For all the designs counters should be reset to "0000" on reset
- A 4 bit std_logic_vector should be used for the counter
- Make sure to incrementally push your changes to the remote repo with an informative commit message. Your entire Vivado project should be pushed to the remote repo.
- Testbench and report utilization after the implementation should be provided in the final report.

## Tasks

:point_right: **Task 1**: (25 points)  
Design a 4 bit shift right ring counter. Update your 4 bit std_logic_vector counter every clock cycle according to the following table:

| clock (sec) | State |
|:-----------:|:---------:|
| 0           | 1000      |
| 1           | 0100      |
| 2           | 0010      |
| 3           | 0001      |

Note 1: After the 4th clock cycle the values repeat from the start.  
Name your source file `shift_right_ring_counter.vhd`  
Create a simulation test bench to verify your design. Name your testbench `ring_counter_tb.vhd`  

:point_right: **Task 2**: (25 points)  
Design a 4 bit shift left ring counter. Update your 4 bit std_logic_vector counter every clock cycle according to the following table:

| clock (sec) | State |
|:-----------:|:---------:|
| 0           | 0001      |
| 1           | 0010      |
| 2           | 0100      |
| 3           | 1000      |

Note 1: After the 4th clock cycle the values repeat from the start.  
Note 2: You need to keep both shift_left and shift_right counter in the same testbench.  
Name your source file `shift_left_ring_counter.vhd`  
Use the `ring_counter_tb.vhd` you created in task 1 to simulate your design.  

:point_right: **Task 3**: (25 points)  
Design a 4 bit binary counter. Update your 4 bit std_logic_vector counter every clock cycle according to the following table:

| clock (sec) | State |
|:-----------:|:---------:|
| 0           | 0000      |
| 1           | 0001      |
| 2           | 0010      |
| 3           | 0011      |
| 4           | 0100      |
| 5           | 0101      |
| 6           | 0110      |
| 7           | 0111      |
| 8           | 1000      |
| 9           | 1001      |
| 10          | 1010      |
| 11          | 1011      |
| 12          | 1100      |
| 13          | 1101      |
| 14          | 1110      |
| 15          | 1111      |

Note: after the 16th clock cycle the values repeat from the start.  
Name your source file `binary_counter.vhd`  
Create a simulation test bench to verify your design. Name your test bench
`binary_counter_tb.vhd`  

:point_right: **Task 4**: (25 points)  
Design a 4 Johnson counter. Update your 4 bit std_logic_vector counter every clock cycle according to the following table:

Recall: In Johnson counter the output from the last flip flop is inverted and fed back as an input to the first. The Johnson counter circulates a stream of ones followed by zeroes around the ring. 

| clock (sec) | State |
|:-----------:|:---------:|
| 0           | 0000      |
| 1           | 1000      |
| 2           | 1100      |
| 3           | 1110      |
| 4           | 1111      |
| 5           | 0111      |
| 6           | 0011      |
| 7           | 0001      |

Note: after the 8th clock cycle the values repeat from the start.  
Name your source file `johnson_counter.vhd`   
Create a simulation test bench to verify your design. Name your test bench
`johnson_counter_tb.vhd`  
