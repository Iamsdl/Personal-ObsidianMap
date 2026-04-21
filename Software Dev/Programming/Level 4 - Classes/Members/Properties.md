A property is a combination between a [[Fields|field]] and a [[Methods|method]]. They are a fancy C# feature made to get rid of [[Getters and Setters]].
> As a general practice, properties are used for public fields, whether there is any get/set logic or not.
# Defining a property
There's multiple ways to define a property. 
## The fully qualified way
```C#
class ExampleClass
{
	private int x;
	public int X 
	{
		get
		{
			return this.x;
		}
		set
		{
			this.x = value;
		}
	}
}
```
## The [[Lambda expressions|lamda]] way
```C#
class ExampleClass
{
	private int x;
	public int X 
	{
		get => this.x;
		set => this.x = value;
	}
}
```
## The auto [[Lambda expressions|lamda]] way
```C#
class ExampleClass
{
	public int X 
	{
		get => field;
		set => field = value;
	}
}
```
> Notice the explicit field has been replaced with the `field` keyword
## The auto-property way
```C#
class ExampleClass
{
	public int X { get; set; }
}
```

# Using a property
Since it is just a fancy field, you use it the same way you would use a [[Fields|field]]
```C#
class Program
{
	public void main()
	{
		ExampleClass ex = new ExampleClass();
		ex.X = 5;
	}
}
```