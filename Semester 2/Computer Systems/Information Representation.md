### Number Systems
#### Binary
Bits - 1 or 0
8 bits is a byte
In modern systems, 0 and 5 volts are often used
- 2-5 is considered as on
- 0.8-0 is considered as off
$n$ bits can represent values up to $2^n -1$

#### Octal
Base 8
Pretty much obsolete
#### Hexadecimal
Base 16
1 2 3 4 5 6 7 8 9 A B C D E F
Direct conversion between binary and hex
Take pairs of 2 hex digits, that's one byte



### Character Representation
Ascii
- 7 bits per character
	- 128 characters
	- Old, not yet obsolete
- 8 in extended ASCII
	- 256
- Lower and upper case characters are separated by exactly 32 bits
	- a single bit shift changes case
Unicode 
- Very large character set
- 32 bits per character
- UTF-8 / UTF-16
	- A subset of unicode is used to improve memory efficiency