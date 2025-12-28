```dcox
IEEE-32Bits Single Precision Method...
Conversion from decimal number to IEEE-32bits binary floating-point number:
1. Take the integer part of the number and generate its binary equivalent.
2. Take the fractional part and generate its binary equivalent.
3. Put the two parts together with radix point in the middle between them.
4. Normalise the whole binary number to the form (1.f) by moving the radix point whether to the left or
to the right.
5. Calculate the decimal exponent as the number of radix point movements.
6. Represent the decimal exponent into binary in excess-127 by adding it to 127, and then convert the
addition result as unsigned integer to binary.
7. Fill in the sign bit with 0 if the decimal number is positive; otherwise with 1.
8. Fill in exponent part with the binary exponent in excess-127.
9. Fill in the fraction (mantissa) part with (.f) normalized binary bits.
Code the decimal  +.001275 as IEEE-32bits binary floating-point pattern.
Solution:
     1- Sign +(.001275) is a positive number then the sign bit is 0.
     2- Convert decimal number to binary
                 + (.001275)  = +(.000000000101)
     3- Put the resulted binary number in the normalized form s (1.f) *2e
                  + (1.01) X 2-10

     4- The fraction part ‘f’ is  (01)
     5- The exponent part ‘e’ is  (-10) in excess-127
                     -10+127=117= 01110101

2 X .001275
.00255 0
.0051 0
.0102 0
.0204 0
.0408 0
.0816 0
.1632 0
.3264 0
.6528 0
.3056 1
.6112 0
.2224 1
1-bit Sign of Fraction (s) 8-bits Exponent (e) 23-bit Fraction (f)
0 01110101 01000000000000000000000
The binary pattern of floating-point format of (+.001275)10 is
(0 011 1010 1 010 0000 0000 0000 0000 0000)2 = (3AA00000)16
```