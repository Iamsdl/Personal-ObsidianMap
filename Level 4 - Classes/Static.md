The `static` keyword is used to denote the absence of an [[Clearing up confusing terminology|instance]]. Something still exists though, so it's better to think of it like a "single, universal instance". The members belong to the [[Classes|type]] itself.
## Static members
A static [[Members|member]] does not need an [[Clearing up confusing terminology|instance]] to be accessed, it can be accessed directly through the [[Classes|class]] name.
## Static classes
A static [[Classes|class]] cannot be [[Clearing up confusing terminology|instantiated]] -> can have only [[#Static members|static members]].
## Example
```C#
public static class ExampleStaticClass
{
	public static int x;
}

public void main()
{
	ExampleStaticClass.x = 5;
	//notice how there is no instance created first.
}
```