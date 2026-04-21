An enum is the simplest form of custom [[Operations, operators, and operands#Operands|operands]] — a way to group and name related [[Write modifiers|constants]] as a [[Value Types vs Reference Types#Value types|value type]].
> You can achieve the same thing with a [[Static|static]] [[Classes|class]] with [[Write modifiers|const]] fields, but an enum has the added benefit of being [[Type safety|type safe]].
# Defining an enum
```C#
public enum Day
{
	Monday;
	Tuesday;
	Wednesday;
	Thursday;
	Friday;
	Saturday;
	Sunday;
}
```
> Behind the scenes, enums are encoded as [[Basic Data Types#The numbers|ints or bytes]], starting from 0 and counting up (i.e. Monday = 0, Tuesday = 1). But this can be explicitly set by the programmer.
```C#
public enum Day
{
	Monday = 1;
	Tuesday = 2;
	Wednesday = 3;
	Thursday = 4;
	Friday = 5;
	Saturday = 6;
	Sunday = 0;
}
```


# Using an enum
As with any [[Data and Variables#Data type|type]], you use enums to create [[Data and Variables#Variable declaration|variables]].
```C#
Day x = Day.Monday;
```
