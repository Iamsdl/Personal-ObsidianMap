The problem: You have the steps of an algorithm clearly laid out, but they vary in implementation.
The solution: Define the steps that vary in abstract methods and implement them in inheriting classes.
```C#
public abstract class AnimalRewardRoutine
{
	public void Execute()
	{
		this.Follow();
		this.GivePaw();
		this.Speak(); //abstract
		this.Sit();
	}
	
	public void Follow() {/*follow owner*/}
	public void GivePaw() {/*shake owner's hand*/}
	public abstract void Speak();
	public void Sit() {/*wait for reward*/}
}

public class CatRewardRoutine : AnimalRewardRoutine
{
	public override void Speak(){ Console.WriteLine("Meow!") };
}

public class DogRewardRoutine : AnimalRewardRoutine
{
	public override void Speak(){ Console.WriteLine("Woof!") };
}
```