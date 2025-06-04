This is the most confusing aspect of beginners trying to earn programming. It is the **type** of the [[Data and Variables#Data type|data type]].
## Value types
Value types are stored on the [[Stack and Heap|stack]]. When assigning a variable from another, the value stored is copied.
The [[Data and Variables#Data type|data types]] that are value type are: [[Basic Data Types#The boolean|bools]], [[Basic Data Types#The numbers|numbers]], [[Basic Data Types#The char|chars]], [[Basic Data Types#The string|strings]], and all [[Struct|structs]].
> Strings are actually an [[Immutable|immutable]] [[#Reference type|reference type]], which makes it behave like a value type so it's more intuitive.

Example:
```C#
int x = 1; //the value of x is 1 and is stored on the stack
int y = x; //the value of y is the value of x. which is 1, and is also stored on the stack
y = 2; //the value of y becomes 2.
Console.WriteLine(x); //will output 1
Console.WriteLine(y); //will output 2
```
## Reference types
Reference types are stored on the [[Stack and Heap|heap]], and their **address** to them is in the variable on the [[Stack and Heap|stack]]. When assigning a variable from another, the **address** is the one that is copied.
The data types that are reference type are... pretty much everything else that is not a [[#Value type|value type]]... and that's [[Classes|classes]].
Will use collections to write an example (Note the snippet uses [[Loops#The for loop|the for loop]]).

```C#
List<int> list1 = [1, 2]; //list1 holds a reference (stored on the stack) which points to the actual list on numbers (stored on the heap)
List<int> list2 = list1; //list2 copies the reference from list1. This means that it is pointing to the same list of numbers on the heap
list1[0] = 3;
list2[1] = 4;

//write list1. Will outout 34
for(int i=0; i<2; i++)
{
	Console.Write(list1[i]);
}

//write list2. Will also 34 since it is referencing the same list.
for(int i=0; i<2; i++)
{
	Console.Write(list2[i]);
}
```
