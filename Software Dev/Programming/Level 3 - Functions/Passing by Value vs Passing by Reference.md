Part 2 of the confusing saga. Parameters are also split into two, combined with [[Value Types vs Reference Types]], this makes for a total of 4 combinations.
# Passing by value
This is the standard way pass parameters. 
The parameter variable is assigned a **copy of the value**.
- For [[Value Types vs Reference Types#Value types|value types]], this means the **value itself is copied**.
- For [[Value Types vs Reference Types#Reference types|reference types]], this means the **address of the object is copied**.
    This is the same as passing by pointer in C++
# Passing by reference
The other way to pass parameters.
- In this case **the object is used "directly"**.
    This is the same as passing by reference in C++, note however that references in C# are not exactly the same thing as references in C++.
    >For a more in depth explanation regarding C++ references, see [[Pointer vs Reference]]

It's a weird thing to explain without seeing it in action so, and seeing it in action requires knowledge about [[Classes|classes]] so come back to these examples later.
# Examples
## 1. Value type by value
```C#
void ByVal(int x)
{
	x++;
	Console.WriteLine(x);
}

void Main()
{
	int x = 1; 
	ByVal(x); // will print 2
	Console.WriteLine(x); //will print 1, because there are now two "1" objects sitting in memory. One for the x in main, and one for the x in ByVal.
}
```
## 2. Value type by reference
```C#
void ByRef(ref int x)
{
	x++;
	Console.WriteLine(x);
}

void Main()
{
	int x = 1; 
	ByVal(ref x); // will print 2
	Console.WriteLine(x); //will print 2, because x in ByRef uses the the object itself, not a copy.
}
```
## 3. Reference type by value
```C#
class Test
{
	public int val;
}
void ByValIncrement(Test x)
{
	x.val++
	Console.WriteLine(x.val);
}

void ByValIncrement(Test x)
{
	x = new Test();
	x.val = 3;
	Console.WriteLine(x.val);
}

void Main()
{
	Test x = new Test();
	x.val = 1;
	ByValIncrement(x); // will print 2
	Console.WriteLine(x.val); //will print 2, because the same address was used.
	
	ByValChange(x) //will print 3.
	Console.WriteLine(x.val); //will print 2, because the object was changed inside the function. 	
}
```
## 4. Reference type by reference
```C#
class Test
{
	public int val;
}
void ByValIncrement(ref Test x)
{
	x.val++
	Console.WriteLine(x.val);
}

void ByValIncrement(ref Test x)
{
	x = new Test();
	x.val = 3;
	Console.WriteLine(x.val);
}

void Main()
{
	Test x = new Test();
	x.val = 1;
	ByValIncrement(ref x); // will print 2
	Console.WriteLine(x.val); //will print 2, because the same object was used.
	
	ByValChange(ref x) //will print 3.
	Console.WriteLine(x.val); //will print 3, because the object was used "directly".
}
```