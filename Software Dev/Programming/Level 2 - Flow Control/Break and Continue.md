Break and continue are keywords used to alter the execution of a [[Loops|loop]].

`Continue` skips the code below it and begins the next iteration, while `break` exits the loop entirely. If you have nested loops, the keyword applies to the innermost loop it is used in.

Note: Using continue in a while loop with its [[Loops#The 3 sss-es|step]] at the end will result in an infinite loop because the continue skips over the step.
Note to note: This does not happen with a for loop.

To actually make a meaningful impact in the program, break and continue are always used with [[Conditional statements|conditional statements]]. Mostly if. 

Example:
```C#
for(int i = 1; i <= 10; i++)
{
	if(i == 3)
	{
		continue;
	}
	
	if(i == 5)
	{
		break;
	}
	Console.Write($"{i} ");
}
```
The result will be `1, 2, 4 `