The problem: You want to extend the functionality of a class in a flexible way.
The solution: Create a "Decorator" class implementing the same interface your original class is.
> This way you follow the [[Single Responsibility Principle]] because the caller should not know nor care whether the class it is calling is the original instance, or a decorated one.
```C#
public interface IService
{
	public void DoSomething()
}

public class Service : IService
{
	private int x = 1;
	public void DoSomething()
	{
		this.x++;
	}
}

public class LoggedService : IService
{
	private IService service;
	private ILogger logger
	
	public LoggedService(IService service, ILogger logger)
	{
		this.service = service;
		this.logger = logger
	}
	
	public void DoSomething()
	{
		this.logger.Log("DoSomething() started");
		
		this.service.DoSomething();
		
		this.logger.Log("DoSomething() ended");
	}
}
```