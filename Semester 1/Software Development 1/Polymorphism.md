Not good description: "Fancy term for [[Inheritance]]"

When a Subclass of a Class defines its own unique behaviours and yet shares some of the same functionality of the parent

#### Overloading [[Methods]]
- "Method signature must be unique"
- This is method overloading
- Doesnt have to be done with [[Inheritance]]
- Methods with the same name but different signatures
- Subclasses can overload methods in superclasses
- You can also do this with Constructors
	- No params vs String params
- Extends behaviour

#### Overriding [[Methods]]
- Overriding can *only* be done with Inheritance
- Fully overwrite a method, with the same name+params
- Same name, different behaviour
- Overrides behaviour
- If we want the superclass behaviour instead we use `super.method(value)`

Constructors are not Overloaded, they are Overriden
Constructors are not Inherited

By default, the Superclass's No-arg constructor is called

```
/*These all have constructors*/

public class A

public class B extends A

public class C extends B


C c = new C()

What runs:
A constructor
B constructor
C constructor

```

We can choose which constructor runs from a superclass by using the super() method call

Only put functionality in a constructor that you want to be shared by all subclasses



Superclass variables can store Subclass methods

```
A myVariable;

myVariable = newB();
```
