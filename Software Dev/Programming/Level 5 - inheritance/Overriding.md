Overriding is applicable only to [[Methods|methods]] and [[Properties|properties]].
There are 4 keywords used in overriding.
These first 3 are the most common way of overriding behavior. The members being overridden must have the same return type, signature, and parameters.
## abstract
Has no implementation, forces overriding.
> If a class has at least one abstract member, it has to be marked abstract as well, preventing instantiation.

> An abstract class that has no implemented method is sometimes called a "purely" abstract class.
## virtual
Has implementation, overriding is optional.
## override
Marks overriding. 
> Alongside [[Members#From inside the class definition|this]], the `base` keyword can be used to access members in the base class.
## new
Hides parent member behind another one
> This keyword, while similar, is not quite an override. It hides the parent member behind another with the same name. However, the return type or parameters can be different.
## Example
```C#
public class Shape
{
	public abstract int Area()
}

public class Square : Shape
{
	public int Length { get; set; }
	
	public Square(int length)
	{
		this.Length = length
	}
		
	public override int Area()
	{
		return Length * Length;
	}
}

public class Cube : Square
{
	public Cube(int length) : base(length)
	{
		
	}
	
	public override int Area()
	{
		return base.Area() * 6;
	}
}

public class Circle : Shape
{
	public Circle(int radius)
	{
		this.Radius = radius;
	}
	public int Radius { get; set; }
	
	public override int Area()
	{
		return 3.14*Radius*Radius;
	}
}

public void Main()
{
	List<Shape> shapes = new List<Shape>();
	shapes.Add(new Square(3));
	shapes.Add(new Circle(5));
	foreach(Shape shape in shapes)
	{
		Console.WriteLine(shape.Area());
	}
}
```
