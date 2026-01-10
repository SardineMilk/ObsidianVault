#java

Use camelCase for variable names
Use ALL_CAPS for constants
Use PascalCase for Classes

**Primitive types**
- int -
	- 4 bytes
	- -2^31 to 2^31 -1
- double
	- roughly 15 decimal places accuracy
	- less efficient than ints
- long
	- 64 bit int

**Object types**
- String
	- this means you can call methods of the string class
		- int stringLength = myString.length();

**Casting**
- Change type of variable
- implicit/explicit
	- implicit - java will cast int to double if needed
	- explicit - manually cast double to int

**Implicit Type Casting**
- int + string
	- "int" + string

**Explicit Type Casting**
- double x = 5.0;
- int n = (int) (x / 2);

#### Examples

**Integer Division**
int/int = integer division
int n = 10/4;
n == 2
- Truncates any decimals - always an int

**Float Multiplying**
double * double = double
double n = 10.0 * 10.0 
n == 100.0
int n = 10.0 * 10.0 *ERROR*
- Always a double, even if result is .0

**Pre- and Post- Increment**
pre- and post- increment only work on variables, not numbers
n++
int n = 100++ *ERROR*

**Example Code**
float x = (-b + Math.sqrt(b * b - (4 * a * c))) / (2 * a);
- Math has a capital because its a class with the method sqrt
