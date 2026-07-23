The problem: You start having multiple classes implementing the same interface.
The solution: Create a "Composite" class implementing the same interface the original classes are.
> This way you follow the [[Single Responsibility Principle]] because the caller should not know nor care whether the class it is calling is one, or many.
```C#
public interface INotificationService
{
	public void PushNotification(string message)
}

public class DesktopNotificationService : INotificationService
{
	public void PushNotification(string message)
	{
		// complicated code here
	}
}

public class MobileNotificationService : INotificationService
{
	public void PushNotification(string message)
	{
		// complicated code here
	}
}


public class CompositeNotificationService : INotificationService
{
	private IEnumerable<INotificationService> services;
	public void PushNotification(string message)
	{
		foreach(INotificationService service in services)
		{
			service.PushNotification(message);
		}
		
	}
}
```