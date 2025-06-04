Functions are normally named so they can be reused and referenced. But what if you just want a quick, one-off function to use as a [[Delegates#Delegate|delegate]]? That's what **anonymous functions** are for.
An **anonymous function** is simply a [[Functions#Function definition|function definition]] without a name.

```C#
delegate int SomeDelegateType(int x);

public void Main()
{
	SomeDelegateType d = delegate(int x) { return x + 1; };
}
```
> Note: You must explicitly declare parameter types.

> Anonymous functions are the predecessor to lambdas. Today, you should prefer lambdas unless you're working with legacy code.