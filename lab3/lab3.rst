:Author: Justin Perona

================
ECS 154A - Lab 3
================

Due by 08:59 on Tuesday, 2018-09-03.
Turn in for the Logisim portion is on Canvas.
Submit one file named lab3.circ.
Include your name and your partner's name (if necessary) either as a submission comment on Canvas, or in the text entry box when submitting.
Only one partner needs to submit.

Partners are suggested, but not mandatory for the Logisim portion of each lab.
Sharing ideas between groups is fine, but sharing .circ files is not.
Since the written portion is "optional," feel free to do those alone or with your partner.

Written Problems
----------------

1. We benefit by going from one bus to two, and two buses to three. Would we benefit if we start adding significantly more and more buses, say, 300? What would the drawback of having that many buses be?
2. Assume that you have a 64-bit microprocessor, with a 48-bit external data bus, driven by a 4.0 GHz input clock. This microprocessor has a bus cycle whose minimum duration equals 100 input clock cycles. What is the maximum data transfer rate that this microprocessor can sustain?

The rest will be added later this week.

Logisim Problem [50]
-------------------

Your assignment is to build a simple processor that is 9 bits wide, and can do various register transfers and ALU operations over a common bus.
Below is an outline of the overall CPU design.
It does not address the circuitry that you may need to implement the HALT instruction.

The diagram is under construction.

Allowed Logisim Components
~~~~~~~~~~~~~~~~~~~~~~~~~~

You may use MUXes, a decoder, a RAM, gates, and flip flops.

CPU Components
~~~~~~~~~~~~~~

You can break the CPU circuit down into the following components:

**1. ALU**

You have already designed a 3-bit ALU in Lab 1.
You should be able to use that as a starting point for this lab's ALU, though you will need to expand it significantly.
Make sure to perform operations bitwise in this lab's ALU.

**2. Register File**

The register bank will contain seven 9-bit registers.
On the rising edge of the clock, if the signal Write Enable is asserted, the register corresponding to the appropriate one-hot input will be written with the input data value.

You will want to create a separate subcircuit for a register, which will consist of 9 flip flops.
Your register file will contain 9 of these subcircuits inside it.

Although a CPU would normally store output in memory (RAM), we will not be dealing with memory in this lab.
We will be treating the register values as the "output" of this CPU.

**3. Decoder**

The decoder will determine the destination register of any output from the ALU by specifying a single high value on one of eight decoder outputs.

**4. Multiplexers**

Two multiplexers are used to select between the different registers, or the immediate data input into the ALU.

**5. RAM**

You will have one 32 x 22 RAM module with separate load and store ports.
We will only use the RAM as a source of instructions, so we will not use the store port.
Associated with the RAM will be a PC register that will have a pin input. When the pin input is set to one, the PC should be reset to zero.

Instruction Format
~~~~~~~~~~~~~~~~~~

This section is under construction.

Operation Description
~~~~~~~~~~~~~~~~~~~~~

This section is under construction.

Testing Your CPU
~~~~~~~~~~~~~~~~

You will find the binary file assembler.out in this repository soon.
You can use to write your own testing programs.
The assembler uses MIPS-like formats, and generates files that can be loaded directly into a Logisim RAM module.
The testall.txt file, which will be uploaded soon, does a fairly thorough test of your circuit.
Here is a short program:

    MOVI R1, #1 (load 1 into R1)
    MOVI R2, #2 (load 2 into R2)
    ADD R3, R2, R1 (add R2 and R1, store result in R3)
    HALT

Run the simulation, and check that the correct registers change to the correct values at the correct times.
For this example, this means that R1 becomes 1, then R2 becomes 2, then R3 becomes 3, then the program halts and no further changes to the CPU state are made.