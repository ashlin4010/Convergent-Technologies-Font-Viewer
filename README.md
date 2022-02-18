# Convergent-Technologies-Font-Viewer

This is a tool for viewing fonts for the Burroughs B20 series of machines.
Also known as the Convergent Technologies AWS, IWS or NGEN.

The specific implementation details of the font formats used by the B22 and B25 machines can be
found in the [B20 Systems Font Reference Manual](http://bitsavers.org/pdf/convergent/manuals_b20/1166204_B20_Font_Reference_R3.0_Mar84.pdf)
and [AWS Hardware Manual Volume 1](http://bitsavers.org/pdf/convergent/aws_iws/A-09-00111-01-A_AWS-2x0_HardwareManual_Vol1_Apr1982.pdf) for the B21.

## Formats

#### AWS (B21)
The AWS used 9x11 character cells generated from a character ROM and hardware to create the characters which are displayed
on the screen. The character ROM used was a typical 4Kb x 8 ROM with 12 address lines, A0-A11, and 8 data lines Q0-Q7.

A detailed explanation of the character ROM's layout can be found on page 230 of the [AWS Hardware Manual Volume 1](http://bitsavers.org/pdf/convergent/aws_iws/A-09-00111-01-A_AWS-2x0_HardwareManual_Vol1_Apr1982.pdf)

#### IWS (B22)
The IWS used 10x15 character cells mapped directly from memory. When not in memory fonts are saved in a `.font` file with a size of 8192 bytes.
This file contains 256 characters each stored as a 16 by 16 pixel array.

#### NGEN (B25)
The NGEN used 9x12 character cells mapped from memory with some additional hardware to provide a half-pixel-shift, improving the visual quality of the characters.
Like the IWS the font format used by the NGEN contains 256 characters with each character stored as a 16 by 16 pixel array.