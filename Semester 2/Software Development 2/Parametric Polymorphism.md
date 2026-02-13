
How can you return multiple types from a function?
Say, a string and an integer
You could make a class to hold a string and int
What if you want to change the output to a char and a float?
You would have to make a new class

### Generics
Types surrounded by angular brackets
`ArrayList<String>`


```
public class Pair<A, B> {
	private A first;
	private B second;
	
	public Pair(A first, B second) {
		this.first = first;
		this.second = second;
	}
}


public interface Stack<T> {
	public void push(T element);
	public T pop();
}

public class IntPairStack implements Stack<Pair<Integer, Integer>> {
	@Override public Pair<Integer, Integer> pop() {
	
	}
	
	@Override public void push() {
	
	}
	
}
```