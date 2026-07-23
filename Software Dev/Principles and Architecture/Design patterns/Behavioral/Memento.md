The Problem: You need to revert to a previous state of an object. 
For example thing text editors, or drawing/painting programs, you can hit ctrl+z at any time to undo.
The solution: Similar to [[Prototype]], the only class that knows enough to be able to revert successfully is the class itself.
```C#
public class MementoExample
{
	/// <summary>
	/// Nested class has access to outer class privates therefore it can store state.
	/// </summary>
	public class StateSnapshot
	{
		internal readonly int someStateFields;
		public StateSnapshot(MementoExample source)
		{
			someStateFields = source.SomeStateFields;
		}
	}
	
	private int SomeStateFields;
	
	public StateSnapshot CreateSnapshot()
	{
		return new StateSnapshot(this); 
	}
	
	public void RestoreFrom(StateSnapshot snapshot)
	{
		this.SomeStateFields = snapshot.SomeStateFields;
	}
}
```