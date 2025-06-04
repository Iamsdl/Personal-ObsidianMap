Classes are custom [[Operations, operators, and operands#Operands|operands]]. Also called custom [[Data and Variables#Data type|data types]]. Also called custom [[Object|objects]]. 
Also, classes are [[Value Types vs Reference Types#Reference types|reference types]].
They are the bread and butter of object oriented programming. Put on your seat belts because there's a lot to talk about.

First things first, a class is an abstraction of a real life object, like a tree, or a ball, or a car, or anything really. By abstraction i mean the "**idea of a tree**", there's many trees, but the **concept of tree** is only one.
The things "defining" a class are it's [[Members|members]], but more about that later.
For now we'll focus on writing the most basic, empty class.
# Defining a class
The class definition (or declaration) is a [[Instructions (statements)#Declarative statements|declarative statement]]. It's done using the `class` keyword followed by whatever name you want to give that class, and a [[Data and Variables#Scope|scope]].
Example:
```C#
class ThisIsMyClassNameForRealz
{
	
}
```
That's it, that's how you create a class.
# Using a class
You use a class the same way you would use any other [[Data and Variables#Data type|data type]]. The simplest example is being able to create a variable of your class.
```C#
int x;
ThisIsMyClassNameForRealz y;
```
