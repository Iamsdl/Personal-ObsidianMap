Constructors are a special type of [[Methods|methods]] that do not have a [[Functions#name|name]] and always [[Functions#Return type|return]] an object of your [[Classes|class]]. Their purpose is **construct an object of your class**. Other ways of saying this that you'll hear is "to create an object" or to "to [[Clearing up confusing terminology|instantiate]] an object".

# Defining a constructor
```C#
public class ExampleClass()
{
	public ExampleClass()
	{
	
	}
}
```
> Note: you can define multiple constructors -> [[Function signature|constructor overloading]].

> Note 2: C# automatically creates an empty constructor for all classes, so unless yours does something or you want to limit [[Members access modifiers|access]] to it, it can be omitted.
# Invoking a constructor
Invoking a constructor is done with the `new` keyword.
```C#
public void Main()
{
	ExampleClass myVariable = new ExampleClass();
}
```