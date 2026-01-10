# Week 7
### Methods
"A block of code we can run from elsewhere in the code"

camelCase names

Running a method is called **invoking**
- When you invoke a method, you can use **parameters**
	- Parameters can be used like variables inside the body of a method
#### Method Body
Code you want the method to execute
e.g. what you write in the main method

#### Method Signature
Made up of a **method name** and a **parameter list**
Must be unique
- Unique combination of name and parameters
- This means a method with the same name can do something completely different if it gets an int or double
Return type is **not** part of the signature

#### Returning
Put the type before the method signature
If you want to return nothing, use type **void**
- With void, you can use "return;" to end the method early
### Scope
Defines what variables parts of your program can see
"Code can only see what is defined in the same {} block it is in" 

You can literally just put random {} blocks around if you want fine control over scope

Variable scope is **hierarchical** 
- Code inside inner {} blocks can see any variables above it in the hierarchy

### Random Stuff
**public** and **private**
- public can be seen anywhere
- private can be seen locally
	- (only inside the class)

**static** 
- Lets you call a method without creating a class

# Week 8

### Objects
Everything is an object
- in java
- sometimes

"An object is a representation of an entity"
#### State
What the object is
Data about the object
Data fields (variables) to hold the data
- Normally **private**
#### Behaviours
What the object does
Code that interacts with the object
Methods that can be called
- Normally **public**
#### Reference Variables
To store an object, reference variables are used
"A map to where you left ... it in the computer's memory"
If you don't store an object in it, it defaults to **null**
-    Unless its a **local variable** defined inside a method, which can't be null
### Class
Blueprint for an object
#### Constructors
Special type of method, used to create objects from a class
-    This is called **instantiation**
Don't have a return type
Same name as the class
If you don't define a constructor, a **default constructor** is created
- Take no parameters
- Do nothing but create an object
- (and call the superclass constructor)
Invoke constructors with the **new** keyword

#### this
**This** keyword lets you access the **data fields** of the class
Use inside methods
```return this.size;```

# Week 9
### Inheritance
"Allows classes to **inherit** Data Fields or Methods from other classes"
Java is built on inheritance
- All classes automatically inherit from **Object**
#### Subclass
**Child Class**
A class that is derived from another class
#### Superclass
**Parent Class**
The class the subclass is derived from
Every class has one (1) direct Superclass
- Define one with **extends ObjectName**
- If you don't define one, Object is used

### Polymorphism
#### Method Overriding

#### Method Overloading
# Week 10
