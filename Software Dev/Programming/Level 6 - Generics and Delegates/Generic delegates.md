Of course, declaring [[Delegates#Delegate type|delegate types]] again and again by hand is tedious, and actually unnecessary, because what you actually need to do given all those tools until now, is to create one good [[Generics|generic]] [[Delegates#Delegate type|delegate type]].
And that's precisely what the .Net framework provides now out of the box.
# Action
`Action` is a [[Generics|generic]] [[Delegates#Delegate type|delegate type]] representing a [[Functions|function]] [[Functions#Return type|returning]] void. It supports up to ~8 parameters, specified with `<>` syntax.
```C#
public void Main()
{
	Action<string> log = Console.WriteLine;
	log("Hello world");
}
```

# Function<>
`Func` is the same as [[#Action]], except it returns a value. It also supports up to ~8 parameters, +1 more for the output.
```C#
public void Main()
{
	Func<int, string> conv = Convert.ToString;
	string result = conv(5); //"5"
}
```
# Predicate<>
Shorthand for a `Func<>` that returns [[Basic Data Types#The boolean|bool]]. Basically a [[Condition|condition]].
```C#
public bool IsPositive(int x)
{
	return x>=0;
}

public void Main()
{
	Preticate<int> condition = IsPositive;
	condition(5); //true
}
```