# Data
Data is anything that can be observed, recorded or processed. To a computer this basically means everything you give it.

Physically, all data is [[Computer (CPU)|stored in bits]], but if the computer is not told how to interpret those bits then that data is useless.
Humans give data meaning by organizing it into [[Object|objects]] and structure by organizing object into [[#Data type|types]].

In addition, any data you give the computer is going to be used in some way, which is why [[Operations, operators, and operands#Operands|data (and objects) are operands]].
# Data type
The data type, also called object type, is a label or name that tells your computer how to interpret the data.
# Variables
A variable is nothing more than a container. Think of a box, or a drawer... or a bookshelf in a library. Variables hold [[#Data|objects]]
The problem is that variables are a bit more restrictive.
## Variable declaration
To create a variable, you have to specify it's **name** and **[[#Data type|data type]]**. This process is called **variable declaration**, and in C# it looks like this: 

```C#
int x; //declaring a variable named "x" that holds an "int"
char c; //declaring a variable named "c" that holds a "char"
string someText; //declaring a variable named "someText" that holds a "string"
```
For [[Basic Data Types|collections]]
```C#
int[] numbers; //declaring a variable named "numbers" that holds an "array of ints"
List<int> moreNumbers; //declaring a variable named "numbers" that holds a "lsit of ints"
```

While it can usually be treated as a [[Instructions (statements)|declarative statement]], behind the scenes it is actually an [[Instructions (statements)|imperative statement]], because the computer is [[Computer (CPU)#RAM - Random Access Memory|allocating memory]] for your variable (building the box).
## Assignment
Variable declaration on its own is just as useful as an empty box. Fortunately now that we have the box, we can put things inside it. This is known as **assigning** a [[Data and Variables|value]] to a (declared) variable.
```C#
int x; //declaration
x = 5; //assignment
```
These two operations are so common together that combining them is a feature of most languages
```C#
int x = 5; //declaration + assignment
```
## Scope
The last thing pertaining variables is the concept of **scope**. A scope is where a variable "lives, is visible and dies".
In C#, any pair of curly brackets { } define a scope, but they exist even if your programming language does not use { } to define them.
Scopes can contain other scopes, and variables declared in parent scopes are visible in child scopes. You can't declare two variables with the same name in the same scope.
Examples:
```C#
//parent scope
{
	int x;
	int x; //will not work because another "x" is declared in the same scope
	
	//a child scope
	{
		int x; //will not work because another "x" is declared in the parent scope
		int y; //will work
	}
	
	y = 5; //will not work because no "y" is declared within this scope. Variables declared within child scopes are not visible to parent scopes.
	
	//another child scope
	{
		int y; //will work because neighbouring scopes do not see each other
		y = 5; //will work because there is an "y" declared within this scope
	}
}
```