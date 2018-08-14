:Author: Justin Perona

================
ECS 154A - Lab 2
================

Due by 08:59 on Sunday, 2018-08-26.
Turn in for the Logisim portion is on Canvas.
Submit two files, named lab2a.circ and lab2b.circ.
Include your name and your partner's name (if necessary) either as a submission comment on Canvas, or in the text entry box when submitting.
Only one partner needs to submit.

Partners are suggested, but not mandatory for the Logisim portion of each lab.
Sharing ideas between groups is fine, but sharing .circ files is not.
Since the written portion is "optional," feel free to do those alone or with your partner.

Written Problems
----------------

Since this lab spans multiple weeks, both the written portion and Logisim portions are divided into their representative weeks.

Week 2
~~~~~~

1. What is the difference between a hard failure and a soft error?
2. Use the 4-bit error correcting circuit that we discussed in class to determine the valid code words associated with the data values *1100* and *0101*.
3. Using the 4-bit error correcting circuit that we discussed in class, are the following code words valid: *1100110* and *0001111*? If not, what bit was flipped, and what is the valid code word associated with the invalid one?
4. What is the minimum Hamming distance between valid code words required to be able to detect 4 errors? What is the minimum Hamming distance between valid code words required to be able to correct 4 errors?
6. What is the difference between a latch and a flip flop?

.. TO DO

The remaining questions will be posted Tuesday night.

Week 3
~~~~~~

Under construction.
It should be posted at the beginning of Week 3.

.. TO DO

Logisim Problems [50]
---------------------

The given files for this lab are split into two files, lab2a.circ and lab2b.circ.
lab2a.circ will be released sometime during week 2 (most likely Tuesday) and encompasses problems 1 - 3.
lab2b.circ will be released sometime at the beginning of week 3 and encompasses problems 4 - 7.

Unless otherwise specified, you may not use any components from the Logisim Arithmetic nor Plexer libraries for any of the following circuits.
In addition, unless otherwise specified, you may only use the AND, OR, and NOT gates from the Gates library.

Week 2
~~~~~~

1. Error correcting [7]
"""""""""""""""""""""""

Implement the 4-bit error-correcting circuit that we discussed in class.
We have 4 data bits, and 3 check bits to cover said data bits.
You will need to recalculate the check bits, and use those to determine which bit has been flipped, if any.

Errors will only be of size 1, if there are any at all.
You do not need to worry about undetectable errors.

Hint: you'll want to use a decoder to correctly route to the bit you want to invert, if any.

*Input Pins*

Your input pins are the data bits **D3**, **D2**, **D1**, and **D0**, as well as the check bits **C2**, **C1**, and **C0**.

*Output Pins*

Your output pins are the output data bits **Z3**, **Z2**, **Z1**, and **Z0**.

*Component Exceptions*

You may use XOR gates, MUXes, and decoders for this problem.

2. Register implementation [5]
""""""""""""""""""""""""""""""

Design a four-bit register implementation that uses T flip flops to store its values.
This implementation differs from the one talked about in lecture, which used D flip flops.
The register starts out with 0000 (all zeroes) as its first value.

*Input Pins*

Your input pins are the four input bits **I3**, **I2**, **I1**, and **I0**

*Output Pins*

Your output pins are the four output values **D3**, **D2**, **D1**, and **D0**.

*Component Exceptions*

You may use XOR gates and MUXes for this problem.

3. FSM implementation [7]
"""""""""""""""""""""""""

Derive a circuit that realizes the FSM defined by the state transition table below.

Table under construction.

.. TO DO

*Input Pins*

Your input pins are the input **v** and the clock **Clock**.

*Output Pins*

Your output pin is the output of the FSM **N**.

Week 3
~~~~~~

For all of the following problems, you must use Karnaugh maps to minimize the number of gates and inputs used.

4. Bit sequence checker [6]
"""""""""""""""""""""""""""

Derive a minimal state table for an FSM that acts as a sequence checker.
During four consecutive clock pulses, a sequence of four values of the signal **w** is applied.
The FSM will output **Q = 1** when it detects that the previous 4 bit sequence was either 1101 or 0110.
At all other times, including when the previous sequence was not those described previously, **Q = 0**.

After the fourth clock pulse, the circuit resets itself and is ready to take in the next 4 bit sequence.

*Input Pins*

Your input pins are the input into the FSM **w**, and the clock **Clock**.

*Output Pins*

Your output pin is the output of the FSM **Q**.

5. Sliding window bit checker [6]
"""""""""""""""""""""""""""""""""

Derive a minimal state table for an FSM that acts as a sequence checker on a sliding window.
The FSM will output **R = 1** when it detects that at least two of the last four bits were 1s.
At all other times, including when the previous sequence was not that described previously, **R = 0**.

Unlike the previous problem, this circuit does not reset itself.
It discards the oldest bit, brings in the newest bit, and uses those most recent 4 bits to make its determination on whether or not it outputs a 0 or 1.

*Input Pins*

Your input pins are the input into the FSM **x**, and the clock **Clock**.

*Output Pins*

Your output pin is the output of the FSM **R**.


6. Parity generator [9]
"""""""""""""""""""""""

Derive a minimal state table for a Moore model FSM that acts as a five-bit parity generator.
For every five bits that are observed on the input *w* during five consecutive clock cycles, the FSM generates the parity bit **p = 1** if and only if the number of 1s in the five-bit sequence is odd.
Thus, this is an even parity generator.

Implement the circuit in Logisim.
Note that this is not a sliding window.
Once you take your five bits in, you reset and start looking at the next 5 bits.

*Input Pins*

**w** is your main input.
You will also need the clock pin **Clock**.

*Output Pins*

**p** is your output, the parity bit.

7. Vending machine FSM [10]
"""""""""""""""""""""""""""

Consider a coin-operated vending machine.
Assume that the machine accepts only quarters, dimes, and nickels.
Coins are inserted until a total of 25 cents or more is deposited.
Only one coin is deposited at a time.

The output signal OM should indicate that merchandise should be provided.
OM = 0 indicates no merchandise.
At the same time as the last coin input (that makes the total amount 20 cents or higher), the change outputs are to be set.
Assume that the machine can give a dime (O10 = 1) and/or a nickel (O5 = 1).
Use the binary outputs O5 and O10 to represent the 4 distinct change possibilities: no change, 1 nickel, 1 dime, 1 nickel and 1 dime.

If a customer does something unwise (such as put in a dime and a nickel followed by a quarter), correct change does not need to be given, but the maximum amount of change must be provided.

*Input Pins*

Your input pins are the relevant coin signals, **I5**, **I10**, and **I25**.
You will also need the clock pin **Clock**.

*Output Pins*

Your output pins are the merchandise output **OM**, and the change outputs **O5** and **O10**.
