**The problem**: You have an object that is always constructed the same way, but with optional features.
**The solution** (if [[What does programming even mean#Programming language|language]] permits): A constructor with optional parameters.
**The other solution**: Create a **Builder** class that knows how to construct the object. If step order matters, also create a **Director** class that uses a builder.
> Note: You can have multiple builder classes that build the same thing in different ways.
```C#
public class House
{
	public Fence Fence { get; set; }
}

public class HouseBuilder
{
	private House house;
	
	public HouseBuilder()
	{
		this.house = new House();
	}
	
	public void Reset()
	{
		this.house = new House();
	}
	
	public void WithFence()
	{
		house.Fence = new Fence();
	}
	
	public House Build()
	{
		var result = this.house;
		this.Reset();
		return result;
	}
}
```