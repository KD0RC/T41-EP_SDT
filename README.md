# T41-EP_SDT
This repository is for my version of the T41-EP Software Defined Transceiver designed by Al Peter, AC8GY and Jack Purdum, W8TEE.
There is a companion book written by Jack and Al available on Amazon that I highly recommend reading before tackling this project.  Even if you don't intend
on building the transceiver but want to learn more about SDRs, the book is a great way to go.

https://www.amazon.com/Software-Defined-Radio-Transceiver-Construction/dp/B09WYP1ST8/ref=sr_1_3?crid=1I6NF5AXTJZUT&keywords=jack+purdum+t41+books&qid=1679844712&sprefix=jack+purdum%2Caps%2C123&sr=8-3

There are also two groups.io forums with tons of good discussion as well as the software for the T41.
https://groups.io/g/SoftwareControlledHamRadio

https://groups.io/g/AmateurRadioBuilders

This code is a derivative of Jack and Al's code, and will carry the same version number as the original, but with "RC" appended.
If I post multiple versions within an "official" version, I will use lower case letters, for example: "V42aRC".

I mark all of my changes one of two ways.
1. A block of code being changed will start with "// KD0RC start" and end with "// KD0RC end".
2. Individual statements will be appended with "// KD0RC".

I leave the original code in place, but commented out to make it feasibile to find the original code for replacement.  
As of this writing, it takes a couple of hours to make all the changes.  It is not trivial to move to a new version, but it is not a terrible task either.

So far, I have made three hardware changes that require different software.
1. I replaced the Fine Tune encoder with a 600 PPR optical encoder.
2. I replaced the analog buttons with an Adafruit MCP23017 I2C addressed MUX and individual buttons.  This reduces the buttons from 18 to 16, but allows for long and short presses, yielding 32 functions.  This change keeps the buttons in the digital domain.  I was having problems with mis-reads of the analog line (probably due to the crappy buttons I used).
3. I connected the I2C and interrupt lines from the touch controller in my 7 inch display to the Teensy board.  No functions are planned for the touch screen that aren't already covered by some other control.

If you use this code or portions of it, please ask any questions about it on the groups.io forum.  If you have a question or issue, you can bet that someone else does too.  All will benefit from any ensuing discussion.  I check it every day that I am not skiing, fishing or taking a nap...

73,

Len, KD0RC
