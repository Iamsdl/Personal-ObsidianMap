A field is just a [[Classes|class]] [[Data and Variables#Variables|variable]].
# Defining a field
You do it just as you would do a [[Data and Variables#Variable declaration|variable]], except it within the [[Data and Variables#Scope|scope]] of the class.
```C#
class ExampleClass
{
	public int x;
}
```
# Using a field
You do is just as you would do a [[Data and Variables#Assignment|variable]], except you have to go through [[Constructors|an instance of your class]] to do so.
```C#
class Program
{
	public void main()
	{
		ExampleClass ex = new ExampleClass();
		ex.x = 5;
	}
}
```