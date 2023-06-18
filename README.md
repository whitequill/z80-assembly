# z80-assembly
This is a language file for pulsar-edit (atom) for Z80 assembly.  It fixed a lot of issues with the original z80 language file from https://github.com/faithanalog/language-z80/blob/master/grammars/z80-assembly.cson.

The fainthanalog language file has an issue where the quoted text is mulit-line and ends up quoteing a lot text because there is a Z80 instruction called af'. This instruction then quotes hundreds of lines of assembly code.  There is also an attempt to make both comments with '#' and ';'.
'#' full line comment and must be started at the start of a line and ';' being able to be placed after some code.
The problem being that '#' is also used in assigning numbers so what happened was all the numbers became commented out. 
That has been fixed.
The 'comment.line' is also a lot shorter and isn't as convoluted.

I'm still having some issues with proper highlighting of regisers vs flags because of there being duplicate symbols for both registers and conditonal flags.  So some code still isn't that easy to read but, I don't know enough about Z80 assembly to know what is and isn't a conditional flag but I have made all instructions very readable.

As an example "c" is both used as a register and a conditional flag. I couldn't find a way to get the highlighting to tell which is which.

Input is welcome.
