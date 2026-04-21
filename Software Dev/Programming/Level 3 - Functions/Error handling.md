The terminology is that a function **throws** errors (called Exceptions), and your function **tries** to run another function and **catches** the errors that are thrown.
Example:
```C#
float Divide(float x, float y)
{
	if(y == 0)
	{
		throw new Exception("Cannot divide by zero")
	}

	return x/y;
}

void Main()
{
	float x = 10;
	float y = 0;
	try
	{
		float result = Divide(x, y);
	}
	catch(Exception e)
	{
		Console.WriteLine(e.ToString());
	}
}
```
This is the most basic example of exception or error handling. There's some more points to make though"
1. You can catch multiple exceptions and treat them differently. This is done by simply chaining multiple catches. The order matters.
```C#
try{}
catch(ArgumentException e) {}
catch(NullReferenceException e) {}
catch(Exception e) {}
```

2. You can use a `finally` alongside `try-catch` to have a block of code that executes regardless if there's an exception or not.
> It is usually used to clear resources (like closing files, database connections, stopping long running [[Multithreading|threads]], etc.)
```C#
try {}
catch {} //the exception can be omitted if it's not used for anything
finally {}
```
