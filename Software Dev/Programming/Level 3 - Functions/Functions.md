Functions are custom [[Operations, operators, and operands|operations]]. And what a custom operation is is just any piece of code you have written before, given a name for reusability. 

Say you've written a program to calculate the factorial of a number. You can take that code and create a function with it, so you can later use it to calculate the factorial of any number. 
As you've probably noticed, there's two steps to this.
# Function definition
Defining a function is a [[Instructions (statements)|declarative statement]].
A function is defined by it's [[#Return type|return type]], [[#Name|name]], [[#Parameters|parameters]] and a [[Data and Variables#Scope|scope]].
## Return type
A function may or may not return a value.
If it does, the return type is the [[Data and Variables|data type]].
If it does not, the return type is **void**, a keyword used to denote the absence of a [[Data and Variables#Data type|data type]].
## Name
The name is just that, the name, nothing special about it. There's a few restrictions regarding how to name functions but the compiler will warn you about them.
## [[Function parameters]]
## Examples:

```C#
//a function without return type
void SomeFunction()
{
	//do stuff
}
//a function with return type int
int SomeOtherFunction()
{
	return 5;
}
```
For more examples with parameters see [[Function parameters|function parameters]].
# Function invocation
Invoking (**calling**) a function is an imperative statement. It makes the computer execute the steps [[#Function definition|defined]].
It is done using (calling, get it?) the function name, and providing values for the declared parameters.
Additionally, if the function has a return type, it can be used as part of  an [[Data and Variables#Assignment|assignment]].
```C#
SomeFunction();
int someValue = SomeOtherFunction();
```
For more examples with parameters, see [[Function parameters|function parameters]].