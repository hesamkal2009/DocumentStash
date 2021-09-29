Bitwise operators are operators that work on a bit at a time.

AND is 1 only if both of its inputs are 1.

OR is 1 if one or more of its inputs are 1.

XOR is 1 only if exactly one of its inputs are 1.

NOT is 1 only if its input are 0.

These can be best described as truth tables. Inputs possibilities are on the top and left, the resultant bit is one of the four (two in the case of NOT since it only has one input) values shown at the intersection of the two inputs.

`
AND|0 1      OR|0 1
---+----    ---+----
  0|0 0       0|0 1
  1|0 1       1|1 1

XOR|0 1     NOT|0 1
---+----    ---+---
  0|0 1        |1 0
  1|1 0
  `
One example is if you only want the lower 4 bits of an integer, you AND it with 15 (binary 1111) so:
`
    203: 1100 1011
AND  15: 0000 1111
------------------
 IS  11: 0000 1011
`
