If a [[Constructors|constructor]] is responsible for creating an object of your class, the destructor is responsible for destroying it.
> In practice a destructor is not really needed, as the responsibility of memory cleanup has been moved away from the developer with the addition of [[Garbage collectors]].
> If you still need to do something when the object is destroyed, there is an additional mechanism provided through the [[Disposable]] pattern. More on that later.
# Defining a destructor
A destructor is defined similar to a constructor, with an added `~`.
```C#
public class ExampleClass()
{
	public ~ExampleClass()
	{
		//something to do when the object is destroyed
	}
}
```
# Invoking a destructor
A destructor in C# is not used by the developer directly. It is invoked by the [[Garbage collectors|garbage collector]] when it deems the object eligible to be collected. 