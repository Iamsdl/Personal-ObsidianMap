The problem: Similar to [[Template Method]], some part of your system varies in implementation, but instead of it being an isolated step in an algorithm it's the whole algorithm.
The solution: Extract the variation behind an abstraction.
```C#
public class System
{
	private IPaymentProvider paymentProvider;
	
	public System(IPaymentProvider paymentProvider)
	{
		this.paymentProvider = paymentProvider;
	}
	
	public void SomeMethod()
	{
		//do something
		paymentProvider.Pay(25);
	}
}

public interface IPaymentProvider
{
	public void Pay(double amount);
}

public class PaypalPaymentProvider : IPaymentProvider
{
	public void Pay(double amount)
	{
		//complex logic here
	}
}

public class StripePaymentProvider : IPaymentProvider
{
	public void Pay(double amount)
	{
		//complex logic here
	}
}
```