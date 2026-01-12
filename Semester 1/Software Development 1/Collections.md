A special set of classes provided by [[Semester 1/Software Development 1/Java]]

Dozens of types of collection
Dynamically sized

Slower than Arrays

Store Objects
Cannot store primitives 
Use wrapper classes
- Integer
- Double
- Java does Autoboxing and Unboxing
	- Auto convert between primitive and wrapper
- Also have static data fields
	- Integer.MAX_VALUE

| Type | Description                              |
| ---- | ---------------------------------------- |
| List | Ordered list of things (close to arrays) |
| Map  | Maps keys to values (lookup table)       |
| Set  | A collection with no duplicate items     |

#### ArrayList

A -> B -> C
If you make an ArrayList of A,
B and C can be put in the ArrayList too
```
import java.util.ArrayList;

ArrayList<E> name = new ArrayList<E>();
// E = object

ArrayList<Apple> appleList = new ArrayList<Apple>();
appleList.add(new Apple("Red"));
appleList.add(new Apple("Green));
Apple apple1 = appleList.get(0); 
```

#### HashMap
If you want keys to look up things later, use this
Unordered

```
HashMap<K,V> name = new HashMap<K,V>


HashMap<String, Apple> appleMap = new HashMap<String, Apple>();
appleMap.put("Braeburn", new Apple("Red"));
appleMap.put("Granny Smith", new Apple("Green"));
Apple apple1 = appleMap.get("Braeburn");

// Keys are unique
if (appleMap.containsKey("Braeburn")) pass; 

```

#### HashSet
Mathematical set
HashMap without values

```
HashSet<E> = new HashSet<E>();

.add(E)
.size()
```