You can **restrict** what types a [[Generics|generic]] can be by using **constraints**.
Common constraints include:
- `where T : class` – T must be a reference type
- `where T : struct` – T must be a value type
- `where T : new()` – T must have a public parameterless constructor
- `where T : BaseClass` – T must inherit from a specific base class
- `where T : Interface` – T must implement a specific interface
- `where T : unmanaged` – T must be an unmanaged type (like `int`, `float`, etc.)
# Example
```C#
public class Printer<T> where T : class
{
	public void Print(T item)
	{
		if (item == null)
		{
			Console.WriteLine("Nothing to print.");
			return;
		}
		Console.WriteLine(item.ToString());
	}
}

public void Main()
{
	Printer<string> p1 = new Printer<string>();
	p1.Print("Hello");      // prints "Hello"
	p1.Print(null);         // prints "Nothing to print"
	
	Printer<int> p2 = new Printer<int>(); // compile-time error: int is not a class
}
```