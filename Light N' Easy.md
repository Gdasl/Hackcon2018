# Light N' Easy

My DIM-WIT no good half-brother gave me this binary text. Lead the way and help me show him who the B055 is.
Note: enclose the flag in d4rk{}c0de before submitting.
```
01001110-00100000-00111010-00001100-11011110-00011110-00000000-01100000-00101010-01111010-00100000-11110110-00111010-00000000-11111110-00001100-00111000-11011110-00000000-10111100-00001010-11011110-11011110-00101010-00000000-01110110-11011110-00001100-00001100-00111010-01010110-00000000-11111100-00001010-11111010-00101010-11110110-11011110-00000000-11101110-11011110-01111011-00000000-10001110-00001100-11111010-11110110-00000000-00100000-10110110-00000000-00011101-10011111-01111011-10110111-11111110-00001010-00100000-00101010-11110111-01111000-00111010-01100111-10001100-00111011-10101010-11011110
```

## The Basics

Basically we have 64 binary strings of length 8. First I tried the obvious, just translating into ascii or hex. This led nowhere. I noticed that there were null strings at regular intervals which made me think of spaces. By that logic, I assumed that each binary string was going to be a character.

At some point I had a flashback to one of my olf CS labs about MIPS pprogramming and remembered the way you control a 7 segment display: 7 segments and a dot. When I saw the hint shortly after I realized this had to be it.

## The solving

Basically the way it will work is the display looks like this:
```
   b
  ===
a| g |c
  ===
f|   |d
  ===   .h (the dot)
   e
```
The input is mapped in sequence, first bit maps to a, second to b etc etc. Quite frankly there might be a better way but in the end I simply printed a set of the list and used excel to accept a 8 digit input and automatically display it by coloring cells... Very primitive but did the job. Finally we get:

```
vioIet lndigo BIue Green yeIIow Orange Aed. fIag iS L.E.d.s.Bring.Joy.To.me
```
