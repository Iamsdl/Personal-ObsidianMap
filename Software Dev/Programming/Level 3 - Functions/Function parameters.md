# Parameters
Parameters are optional [[Data and Variables|variables]] that are used to pass data from outside in when [[#Function invocation|calling a function]]. Their [[Data and Variables#Scope|scope]] is inside the function.
Parameters can be:
## Required
### Standard
What you'll be using most of the time:
```C#
int Add(int x, int y)
{
	return x + y;
}

int result = Add(2,3); //5
```
### Input parameters
Marked with the `in` keyword, input parameters are read only and trying to change their value from within the function will result in a compiler error.
Input parameter may have a [[#Optional|default value]].
```C#
void SomeOtherFunction(in int x)
{
	x = 5; //will show a compiler error because x cannot be changed
}

SomeOtherFunction(in 5);
```
### Output parameters
Marked with the `out` keyword, output parameters must be assigned a value before exiting the function. Forgetting to do so will result in a compiler error.
Only [[Data and Variables#Variables|variables]] can be passed to out parameters.
```C#
void SomeOtherFunction(out int y)
{
	//will also show a compiler error because y must be given a value
}

int y;
SomeOtherFunction(out y);
```
### Reference parameters
Marked with the `ref` keyword, these parameters are passed by reference.
Only [[Data and Variables#Variables|variables]] can be passed to ref parameters.
```C#
void YetAnotherFunction(ref int x)
{
	//do something
}

int x
YetAnotherFunction(ref x);
```
## Optional
Optional parameters are given a default value when the function is [[Functions#Function definition|defined]]. When the function is [[Functions#Function invocation|called]], a value can be provided to them, but if one is not provided then the default value will be used.
Optional parameters must be declared after [[#Required|required]] parameters
```C#
int Add(int x, int y = 5)
{
	return x + y;
}
```

When [[Functions#Function invocation|calling]] this function, you can provide a value for y or omit it:
```C#
Add(2,3);
Add(2); //5 will be used for y
```
## Array parameters (params)
Marked with the `params` keywords, this function parameter is [[Functions#Function definition|declared]] as an array, but used as if there were many separate parameters.
Array parameters must be declared after [[#Optional|optional]] parameters, and you can have only one.
```C#
int Sum(params int[] numbers)
{
	int sum = 0;
	foreach(int nr in numbers)
	{
		sum += nr;
	}
	return sum;
}
```
When [[Functions#Function invocation|calling]] this function, you can provide however many values, as if they were separate parameters:
```C#
Sum(1,2,3,4,5);
```