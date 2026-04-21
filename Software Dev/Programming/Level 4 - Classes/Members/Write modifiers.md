[[Fields]] can be altered a bit using the following keywords:
- `readonly` -> can have its value set only in the [[Constructors|constructor]]. Trying to change its value outside of a constructor will cause a compiler error
- `const` -> replaced at [[From software to hardware#Compilation|compile time]] with their values
- `volatile` -> indicates that a field might be modified by multiple threads that are executing at the same time

> Never used `volatile` in my life so here's the official docs:
> https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/volatile