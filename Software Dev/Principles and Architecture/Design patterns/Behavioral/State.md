State is a very similar pattern to [[Strategy]] in terms of implementation, but it differs on a fundamental level. It is modelling a [[Math/State machine|state machine]]
- A Strategy is:
	- communicated from outside
	- not aware of other strategies
	- not changed once chosen
- A State is:
	- settled on from within, may or may not be communicated to the outside world
	- aware of all other possible states
	- changes constantly
```C#
public class Character : IState
{
	private IState currentState = new IdleState(this);
	
	public void Update() { currentState.Update(); }
	public void Jump() { currentState.Jump(); }
	public void Land() { currentState.Land(); }
	
	internal void TransitionTo(IState state)
	{
		this.currentState = state;
	}
}

public interface IState
{
	public void Update();
	public void Jump();
	public void Land();
}

/// <summary>
/// Base class used to provide a default implementation.
/// It's cleaner to override relevant virtual methods than to bloat the code overriding irrelevant abstract methods.
/// </summary>
public abstract class BaseState : IState
{
	private Character character;
	
	public BaseState(Character character)
	{
		this.character = character
	}
	
	public virtual void Update() { /*nothing to do*/ };
	public virtual void Jump() { /*nothing to do*/ };
	public virtual void Land() { /*nothing to do*/ };
}

public class IdleState : BaseState
{
	public override void Update()
	{
		if(Key.IsPressed("spacebar"))
		{
			this.Jump();
		}
	}
	
	public override void Jump()
	{
		character.TransitionTo(new JumpingState(character));
	}
}

public class JumpingState : BaseState
{
	public override Update()
	{
		if(character.TouchedGround())
		{
			this.Land();
		}
	}
	
	public override void Land()
	{
		character.TransitionTo(new IdleState(character));
	}
}
```