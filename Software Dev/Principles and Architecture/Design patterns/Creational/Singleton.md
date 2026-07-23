**The problem**: You need to ensure that an object has only one instance (without making the class static).

**The Solution**: Have the class hold a [[Static|static]] reference to itself

> In practice you shouldn't need to do this nowadays, cause the better option is to [[Dependency Injection|inject]] your class [[Dependency Injection Container#Object Lifetime Scope|as singleton]] instead, but in case you need to, this is how you do it.
```C#
public class SingletonExample
{
	private static SingletonExample instance;
	
	public SingletonExample Instance 
	{
		get
		{
			//only create one instance ever.
			if(instance == null)
			{
				instance = new SingletonExample();
			}
			
			return instance;
		}
	}
	
	//prevent access to the constructor from outside by 
	//explicitly adding a private one.
	private SingletonExample() { } 
}
```
