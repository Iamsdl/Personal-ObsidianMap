This is how you tell the computer to make decisions. There's 3 types:
# If
The if is literally the human language if. 
If something happens do something, otherwise do something else.
Needless to say, the answer to the question "did something happen?" is yes/no, therefore a boolean. 
But a static boolean is not very helpful, which is why an if 99% of the time is defined with a [[Condition|condition]] (the result of which is a boolean).
The if statement can have one or more `else if` and an `else` that you can add to it, as illustrated below (note that else has to be the last in the chain):
1. Simple if
```C#
if(condition)
{
	//do something
}
```

2. If with else
```C#
if(condition)
{
	//do something
}
else
{
	//do something else
}
```

3. If with else if and else
```C#
if(condition)
{
	//do something
}
else if(someOtherCondition)
{
	//do something else
}
else if(yetAnotherCondition)
{
	//do something else
}
//more can be added
else
{
	//do something else
}
```
# Switch
The switch is just another way to write the [[#If|if]]. It is supposed to be used with [[Data and Variables|variables and values]] instead of conditions. Sometimes it's easier to read/write than an if.

Note the usage of the [[Break and Continue|break]] keyword. This is an example of keyword overloading, where a keyword generally used in one context has a different function in another context. In this case the break keyword is generally used to stop loops, but here it's used to "stop a switch". You can think of the switch as a "one time loop" because of that... but it's kind of wrong so don't.
## most basic switch
```C#
int x = 5;
switch(x)
{
	case 1:
	//do something when x == 1
	break;
	case 2:
	//do something when x == 2
	break;
	default:
	//do something when none of the above cases have been met
	break;
}
```
It is equivalent to the following if:
```C#
int x = 5;
if(x == 1)
{
	//do something when x == 1
}
else if(x == 2)
{
	//do something when x == 2
}
else
{
	//do something when none of the above cases have been met
}
```
## switch with fall-through
```C#
int x = 5;
switch(x)
{
	case 1:
	case 2:
		//do something when x == 1 || x == 2
		break;
	default:
		//do something when none of the above cases have been met
		break;
}
```

It is equivalent to the following if:
```C#
int x = 5;
if(x == 1 || x == 2)
{
	//do something when x == 1 || x == 2
}
else
{
	//do something when none of the above cases have been met
}
```
## switch with tuple
```C#
int x = 5;
int y = 25;
switch ((x,y))
{
	case (1, 2):
		//do something when x == 1 && y == 2
		break;
	default:
		//do something when none of the above cases have been met
		break;
}
```
It is equivalent to the following if:
```C#
int x = 5;
int y = 25;
if(x == 1 && y == 2)
{
	//do something when x == 1 && y == 2
}
else
{
	//do something when none of the above cases have been met
}
```
## switch expressions
TODO
# The ternary operator
The ternary operator is an [[Conditional statements|if]] written on one line. As the name suggests, it is an [[Operations, operators, and operands|operator]], and since operators always return a value, the ternary operator is most used in [[Data and Variables#Assignment|assignments]].
It's structure is `condition ? value when true : value when false`.
Example:
```C#
int x = 5;
int y = x == 2 ? 10 : 15;
```

It reads like the following if:
```C#
int x = 5;
int y;
if(x == 2)
{
	y = 10;
}
else
{
	y == 15;
}
```