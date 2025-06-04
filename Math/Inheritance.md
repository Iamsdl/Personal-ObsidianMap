Inheritance is a feature limited only to [[Classes|classes]].
> The class that is inherited from is usually called the **base class** or **parent class** and the class that inherits is usually called the **child class**.

Inheritance enables:
- Inheriting members from the parent class.
	- This introduces [[Member Access Modifiers - Inheritance|new members access modifiers]]
- Extending the behavior of the parent class.
- **Changing** the behavior of the parent class. Feature known as [[Overriding|overriding]].

There is only one restriction when inheriting, and that is that you cannot inherit more than one class.
## Example
Inheriting a class is done with the `:` (colon)
```C#
public class Parent
{
	public int x;
}

public class Child : Parent
{

}

public void Main()
{
	Child c = new Child();
	c.x = 5; //notice how x is declared in the parent but can be used from the child
}
```