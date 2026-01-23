
### Upcasting
A type that can fit a class can also fit any descendants of it
A subclass can fit in any type of a superclass
This lets you define array of Fruit, and put Apple and Orange in it

This is also allowed:
```
Apple myApple = new Apple();

Fruit myFruit;
myFruit = myApple;

myFruit.eat();
```
It does the same as:
```
Fruit myFruit;
myFruit = (Fruit) myApple;
```


When you *cast* an object in java
Java views it as an instance of the superclass
This means you *cannot* use subclass features after casting
However, if you cast it back into the subclass ` myFruit = (Apple) myFruit;`, 
you *can* use the subclass features again

You can use any overridden methods,
Just not any new methods

You can cast any class as Object


```
Apple myApple = new Apple();

Object myObject;
myObject = myApple;

myObject.toString;
```
Output: file.Apple@memorylocation123

You can use `if (myObject instanceof Apple)` or similar to differentiate between subclasses cast to a superclass, and run different code depending on the class
