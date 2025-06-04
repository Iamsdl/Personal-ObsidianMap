Sometimes, the actual [[Classes|class]], [[Functions|function]], or [[Data and Variables#Data type|type]] isn't enough to describe all the behavior you want. For this reason, **attributes** exist: they are metadata you can attach to your code.
They don’t _do_ anything by themselves — they just **describe** something, and it’s up to other code (like frameworks, libraries, or your own tools) to read them and react accordingly.
# Defining your own attribute
All attributes are just [[Classes|classes]] that [[Inheritance|inherit]] from `System.Attribute`:
```C#
public class MyTagAttribute : Attribute
{
	public string Note { get; }
	public MyTagAttribute(string note)
	{
		Note = note;
	}
}
```
# Using an attribute
You use an attribute by applying it to something else. The things you can apply it to are:
- [[Classes]]
- [[Struct|Structs]]
- [[Methods]]
- [[Properties]]
- [[Function parameters|Parameters]]
- Even [[Project|assemblies]]
```C#
[MyTag("Just a test")]
public class MyClass {}
```

But even if you've applied it, it still doesn't do anything. In order for it to actually do something you need some code that is able to read these attributes and make decisions based on them. Since attributes are also code, what you end up with is basically "code reading code". The term for this is [[Reflection]].