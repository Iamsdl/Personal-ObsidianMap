**The problem**: You need to ensure that an object has only one instance (without making the class static).
The solution is the **Singleton** pattern:
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
