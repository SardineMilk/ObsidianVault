
Could use fixed point:
- 32 bit number
- 32 bit after decimal point
- Restricted range: only 32 bit max

Use *scientific notation*


Floating point is not exact
$1+2 \neq 3$


**Multiplication**
Multiply mantissa, add exponent


**32 bit IEEE**
1 bit sign
8 bit exponent
- bias 127 format
- The bits represent the exponent with 127 added
23 bit fraction

**Decimal to binary**
17.625

17 -> 10001
.625 -> .1010

10001.1010
1.00011010 * 2^4

Exponent -> 127+4 -> 10000011
Mantissa -> 00011010...0 (23 bits)
Sign -> 0
Result -> 0 10000011 00011010...0