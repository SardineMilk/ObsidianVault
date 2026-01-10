
Exceptional Events

Almost always our/users fault

Should be handled without crashing

All [[Errors]] and Exceptions inherit from **Throwable**


### Throwable
#### Runtime Exceptions
**Unchecked Exceptions**
Programming/logic errors
e.g. array index errors
No way for java compiler to check at compile time

NullPointerException
IndexOutOfBoundsException
ArithmeticException

Dealt with by writing better code
- Check if hashmap contains key before accessing
- Don't divide by 0

**Checked Exceptions**
Outside the program's control
Input/output like file access

FileNotFoundException
IOException
ParseException

Flagged at compile time

Deal with it by:
```
public void checkFile(String fileName) throws FileNotFoundException
{
if(fileName.equals("))
	throw new FileNotFoundException();
}
```

You can also make your own exceptions
Extend exception, and put the exception logic in the constructor

But this doesnt handle them
to handle them, use

```
try 
{
	// Code
}
catch (Exception e)
{
	// Handle Exception
}
```

Better to have one catch per exception than to use generic Exception

Anything after an exception is thrown in a try block doesnt execute
So you might never close a file, causing memory leaks

You can use a finally block
```
try {}
catch {}
finally {}
```
This can get tricky with streams
so use 
Try with resources
- the cooler finally
```
try(InputStream strem = new FileInputStream(file);) 
{
	// Code
}
catch (IOException e) 
{
}

```
