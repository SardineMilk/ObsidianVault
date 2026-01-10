
Strings are *reference variables*
but they are also *immutable*

Leads to a common bug

```
myString.replace("i", "I");
```
returns a *new* string, does not happen in-place


*WRONG*
```
myStringA == myStringB;
```
*RIGHT*
```
myStringA.equals(myStringB1);
``