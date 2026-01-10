No return type
Same name as class
Can have parameters
Must have unique signature
- All constructors have unique parameter list

Java generates a default constructor
- ONLY if you have no other constructors

Constructors are invoked with the "new" keyword
```
// Calls the Apple() constructor
Apple myApple = new Apple();

// Calls the Apple(String colour) constructor
Apple ripeApple = new Apple("Red);
```

myApple and ripeApple are [[Reference Variables]]

Primitive types
- int, boolean, double etc
- very small, are copied into new memory when passed into a function

Reference Variables are a reference to an object.
When you pass into a function, it passes a pointer or reference to the object
If a reference variable is empty, it is assigned **null** by [[Default Variables | default]]
- Null is a literal like **true** or **false**

The above code
- Creates an empty reference variable
- Calls the constructor of the Apple class
- Puts the resulting Object in the reference variable


 


**this** keyword
- refers to object itself
- often used in constructor
- 