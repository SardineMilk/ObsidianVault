
Object-Oriented Programming (OOP) is one of the most common styles of programming


You don't write Objects, you write Classes that become Objects
#### Objects
- An object is a representation of an Entity
	- Entity is purposefully broad
#### Classes
- Blueprint for an object


#### Behaviour
- What the object does
- Methods in class
#### State
- What the object is
- Data fields (variables) in class

How do we construct Objects from Classes?
- Use a [[Constructor]]
	- A specific type of method
	- No

myApple1 and myApple2 are both instances of the Apple class
myApple1 = myApple2;
sets myApple1 to a REFERENCE to myApple2
myApple1 still exists in memory, with no way to access
Java [[Garbage Collector]] cleans dereferenced objects
- very slow



#### Class Variables
- Per object is an Instance Variable
	- Unique per object created
	- Change by object.myVariable
- Per class is a Static Variable
	- Define content in class, outside constructor
	- Static keyword
	- Change by Class.myVariable