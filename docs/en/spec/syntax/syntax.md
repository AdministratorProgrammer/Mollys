# Mollys Language Syntax

**The syntax is described according to the standard: EBNF (ISO/IEC 14977:1996 Extended BNF).**

This file (**syntax.md**) uses the **Markdown** markup language. \
The syntax description in plain text using the **EBNF** meta-language can be found in: **[syntax.ebnf](syntax.ebnf)**
___

### Lexical elements
```ebnf
letter  =   "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M"
          | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z"
          | "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m"
          | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z";
```
```ebnf
dec digit  =  "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9";
```
```ebnf
hex digit  =  dec digit | "A" | "B" | "C" | "D" | "E" | "F"
                                             | "a" | "b" | "c" | "d" | "e" | "f";
```

### Basic tokens
```ebnf
identifier = letter, { letter | dec digit | "_" };
```
```ebnf
integer decimal literal = dec digit, { dec digit };
```
```ebnf
integer hex literal = hex digit, { hex digit }, "h";
```