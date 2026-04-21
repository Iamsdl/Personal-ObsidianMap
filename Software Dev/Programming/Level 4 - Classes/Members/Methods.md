A method is just a [[Classes|class]] [[Functions|function]].
>No idea why a new term was needed... nobody really cares if you say function or method really... Technically, since C# is a fully object oriented language, that means everything lives inside a class -> every function is a method.
# Defining a method
You do it just as you would do a [[Functions#Function definition|function]], except it within the [[Data and Variables#Scope|scope]] of the class.
```C#
class ExampleClass
{
	//empty constructor
	public ExampleClass() { }
	
	public ExampleMethod()
	{ 
		//do something
	}
}
```
# Invoking a method
You do is just as you would do a [[Functions#Function invocation|function]], except you have to go through [[Constructors|an instance of your class]] to reach it
```C#
class Program
{
	public void main()
	{
		ExampleClass ex = new ExampleClass();
		ex.ExampleMethod();
	}
}
```