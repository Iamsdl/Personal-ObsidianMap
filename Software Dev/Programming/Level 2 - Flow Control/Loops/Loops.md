# Loops
A loop makes the computer repeat the same lines of code multiple times.
## The 3 sss-es
In theory. every loop should have (whether explicit or behind the scenes) the following 3 components:
- The start = initial state/conditions when first entering the loop
- The stop = the condition to exit the loop
- The step = an instruction that (ideally) moves the loop closer to it's stop
In practice, you can write loops that are missing some components, resulting in either a loop that is not working, or a loop that is not stopping. 
There's 3 types of loops that you can write:
## The while loop
A while is a loop is defined with a boolean. When the boolean is `true` the loop is executed, when the boolean is `false` the loop is not executed. But that is not very helpful, which is why a while loop 99% of the time is defined with a [[Condition|condition]] (the result of which is a boolean).
It is generally used when the number of steps is unknown.
```C#
bool condition;
while(condition)
{
	//do stuff
}
```
### The do while loop
It is identical to the while loop, except the condition is written at the end. This makes it so the loop is executed at least once.

```C#
bool condition;
do
{
	//do stuff
}
while(condition);
```
## The for loop
A for loop is defined with [[#The 3 sss-es|a starting state, an end condition, and a step]].
It is generally used when the number of repeats is known beforehand.
```C#
//note the (start;stop;step) format
for(int i = 1; i <= 10; i++)
{
	//do stuff
}
```
It is equivalent to the following [[#The while loop|while loop]]
```C#
int i = 1;
while(i <= 10)
{
	//do stuff
	i++;
}
```
## The foreach loop
Foreach is a loop that iterates over [[Basic Data Types|collections]].
```C#
List<int> someNumbers = [1, 3, 5, 7, 9];
foreach(int number in someNumbers)
{
	//do something with the number
}
```
It is equivalent to the following [[#The for loop|for]] loop:
```C#
List<int> someNumbers = [1, 3, 5, 7, 9];
for(int i = 0; i < someNumbers.Length; i++)
{
	int number = someNumbers[i];
	//do something with the number
}
```