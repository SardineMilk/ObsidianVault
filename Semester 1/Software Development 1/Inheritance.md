Allows Classes to **inherit** data fields and methods from a different class
Cuts down code reuse
- fix bug in one place

#### Example:
Fruit
- Cored Fruit
	- Apple
	- Pear
- Strawberry
- Peelable Fruit
	- Orange
	- Avocado

All fruits have shared behaviour/data
Subclasses can have more specific behaviour

Fruit: colour, eaten, takeBite()
Cored Fruit: is_cored, coreFruit()
Apple: removeStalk()

#### Subclass
- A class that is derived from another class is a Subclass
- **Java Specific** - Every class is a Descendant of Object
	- Apple is a Subclass of object because it has no other Superclass defined
#### Superclass
- The class the Subclass is derived from is a Superclass
- Every class has one and only one Superclass

Relational - Cored Fruit is a Subclass of Fruit and a Superclass of Apple
Descendants - Apple is a Descendant of Fruit, it can use any functionality of Fruit 

Data Fields and [[Methods]] can be used from *any* Superclass, not just the direct parent


```
public class Fruit {
	/* code */
}

public class CoredFruit extends Fruit {
	/* core */
}

public class Apple extends CoredFruit {
	/* code */
}
```



**TODO split into notes**
Superclass 
Subclass
Inheritance
Polymorphism
Method Overriding
Scope