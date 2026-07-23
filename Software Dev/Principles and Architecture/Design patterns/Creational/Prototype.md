**The problem**: You need to duplicate an object. The additional problem is that in order to do that you have to know how, which implies knowing the type of the instance ([[Software Dev/Principles and Architecture/4 pillars of OOP/Inheritance|inheritance]]) and having access to the classes [[Members access modifiers|private]] fields.
**The solution**: [[Information Expert]]. Who is the most suited class to solve these problems? The class itself.
```C#
public class PrototypeExample
{
	private string somePrivateField;
	
	public PrototypeExample Clone()
	{
		return new PrototypeExample
		{
			somePrivateField = this.somePrivateField;
		}
	}
}
```
> .Net has an `ICloneable` interface for this purpose.