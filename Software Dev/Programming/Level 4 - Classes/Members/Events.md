An event is a [[#Delegate|delegate]] with added access protection: outside code can subscribe or unsubscribe, but not invoke or overwrite it.

> You still need a [[#Delegate type|delegate type]] to declare an event.
## Examples
### A publisher using delegates
```C#
public delegate void Notify();

public class Publisher {
    public Notify OnNotify; // anyone can assign freely

    public void Trigger() {
        OnNotify?.Invoke(); // invoke all subscribed methods
    }
}

public void Main()
{
	Publisher pub = new Publisher();
	pub.OnNotify = null; // wipes all subscribers!
}
```

### A publisher using proper events
```C#
public class Publisher {
    public event Notify OnNotify; // external code can't call or assign directly

    public void Trigger() {
        OnNotify?.Invoke();
    }
}

public void Main()
{
	Publisher pub = new Publisher();
	pub.OnNotify += () => Console.WriteLine("Listener 1");
	pub.OnNotify -= SomeHandler;
	
	pub.OnNotify();      // Can't invoke it
	pub.OnNotify = null; // Can't overwrite it
}
```