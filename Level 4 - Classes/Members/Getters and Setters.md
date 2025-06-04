Getters and Setters are a particular type of [[Methods|methods]]. They are defined and invoked as any other method, but they serve a very specific purpose, that of controlling [[Fields|field]] reading and writing.
```C#
class ExampleClass
{
	private int x;
	public int GetX()
	{
		return this.x;
	}
	public void SetX(int newValue)
	{
		this.x = newValue;
	}
}
```