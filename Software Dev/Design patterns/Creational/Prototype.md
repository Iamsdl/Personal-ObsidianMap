**The problem**: You need to duplicate an object. The additional problem is that in order to do that you have to know how, which implies knowing the type of the instance ([[Inheritance]]) and having access to the classes [[Members access modifiers|private]] fields.
**The solution**: Let the class do the cloning.

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